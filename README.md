# Modelo de IA - Previsão de score de crédito
 
# Objetivo

Este projeto foi desenvolvido como parte de um intensivo de Python, com foco na criação de um modelo de previsão com Inteligência Artificial. O objetivo principal é prever ,com base no comportamento de clientes anteriores, como será o comportamento de novos clientes de um banco a partir do score de crédito, sendo ele Ruim, Ok ou Bom. Com essas informações, o banco poderá definir o perfil do cliente com a ajuda do modelo de IA e tomar as decisões a partir dele.

**Enunciado** → Você foi contratado por um banco para conseguir definir o score de crédito dos clientes. Você precisa analisar todos os clientes do banco e, com base nessa análise, criar um modelo que consiga ler as informações do cliente e dizer automaticamente o score de crédito dele: Ruim, Ok, Bom.

# Como funciona

Primeiramente, o código recebe um arquivo da base de dados de 100 mil clientes do banco, contendo informações relevantes como salário anual, número de contas, dias de atraso, dívida total, score de crédito, entre outros. Após isso, ele prepara a base de dados para a inteligência artificial, transformando todas as colunas de textos em números usando a função LabelEncoder, uma vez que o modelo de classificação não funciona com textos. Com isso, separamos as informações em dados de treinos e dados de testes, onde a gente usa os dados das colunas que a gente quer prever, que no caso é o score de crédito, e os dados das colunas que queremos usar para fazer a previsão, que são todas com exceção da coluna score de crédito e id do cliente. Por fim, fazemos o treinamento da IA e implementamos o modelo para prevermos o score de crédito de novos clientes do banco.

# Modelos usados

Para este projeto, usei apenas dois modelos, o de Árvore de decisão (Random Forest Classifier) e o KNN (KNeighbors Classifier), porém, pode-se usar mais. Após o treinamento da IA com esses dois modelos, calculei a acurácia de cada um, o modelo de Árvore de decisão teve uma acurácia de aproximadamente 83%, enquanto o modelo KNN teve uma acurácia de aproximadamente 74%. Portanto, escolhi implementar o de Árvore de decisão para fazer a previsão.

Para fazer o teste, peguei um novo arquivo de base de dados contendo informações de 3 novos clientes do banco, sem o score de crédito, e implementando o modelo, a IA previu que um deles seria ruim, e os outros dois bons.

# Detalhes

- Lembre-se de deixar os arquivos das bases de dados na mesma pasta do arquivo do código para o Python reconhecer, os arquivos são “clientes.csv” e “novos_clientes.csv”.
- As ferramentas usadas foram pandas e scikit-learn, para instalar use no terminal: pip install pandas numpy scikit-learn.
- Lembre-se também, este é apenas um modelo de previsão, nunca nenhum modelo terá uma acurácia de 100% e acertará em todas as previsões.
