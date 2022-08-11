# challenge_titanic
Desafio do titanic para classificação se tal pessoa morreria ou sobreviveria 

Foi utilizado as bibliotecas pandas e numpy, foi feito um pre-processamento dos dados.
Inicialmente foi utilizado o LabelEncoder, importado da biblioteca sklearn.preprocessing para converter em valores númericos os valores presentes nas colunas 'Name', 'Sex', 'Ticket', 'Embarked'. Uma ressalva é necessária, foi analisado apenas os Sobrenomes dos nomes presentes na coluna respectiva.
Foi aplicado o 'OneHotEncoder', presente também no sklearn.preprocessing, afim de diminuir o peso referente para a máquina, aplicado as colunas 'PClass', 'SibSp', 'Parch', 'Embarked'.
Logo após, foi feitao, utilizando o ScalerEncoder para aproximar os limites dos valores entre (-1, 1), afim de não 'enganar' o treinamento do máquina com um possuindo maior peso do que o outro. Dessa forma, foi aplicado tal biblioteca na 'Age', 'Sobrenome', 'Ticket' e 'Fare'.
Ao aplicar o método Random Forest, com o número de estimadores igual a 100 consegui a maior precisão de 0.77751.
