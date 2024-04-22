# 💸 Bank Marketing - Análise Exploratória de Dados

Este projeto será baseado no Dataset Bank Marketing encontrado na UC Irvine - Machine Learning Repository e disponibilizado por S. Moro, R. Laureano e P. Cortez, e pode ser encontrado neste [link](https://archive.ics.uci.edu/dataset/222/bank+marketing).
### 🛠️ Ferramentas utilizadas
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)

## 1.1. Os dados, o problema, e o objetivo

### Estrutura dos dados
Os dados são relacionados com campanhas direta de marketing de uma instituição bancária portugesa. A campanha de marketing foi baseada em ligações telefonicas, por vezes mais de uma para o memso cliente, para saber se o produto financeiro (termo de depósito bancário) seria aceito ou não.

|Coluna|Descrição|
|-|-|
|age|Idade|
|job|Tipo de trabalho|
|marital|Estado civil|
|education|Nível de educação|
|default|Se deu prejuízo ao banco|
|balance|Média de balanço anual|
|housing|Se possui emprestimo imobiliário|
|loan|Se possui emprestimo bancário|
|contact|Tipo de contato (celular, ou telefone fixo)|
|day_of_week|Dia do contato|
|month|Mês do contato|
|duration|Duração das ligações em segundos|
|campaign|Número de contatos feitos|
|pdays|Número de dias desde que o cliente foi contato por uma campanha anterior (-1 significa que não foi contatado)|
|previous|Número de contatos antes dessa campanha, para este cliente|
|poutcome|Resultado da última campanha (falha, sucesso)|
|y|Se o cliente aceitou essa campanha|

### O problema
Como recém chegado no time de dados, o gestor nos fez algumas solicitações a partir dos dados dessa campanha após requisição do time de marketing para otimizar as próximas campanhas:

1. Entender o perfil dos clientes do banco e identificar características que influenciam a aceitação dos produtos oferecidos;
2. Avaliar a eficácia da campanha de marketing direto para depósitos a prazo, identificando os melhores canais de contato e o perfil do público-alvo mais receptivo.

### O objetivo
Dessa forma com os dados em mãos, nosso objetivo será:
- Buscar a relação entre as variáveis, e como elas influenciam na aceitação dos produtos;
- Identificar o perfil dos clientes mais propensos a fechar negócios após as campanhas;
- Entender como e quais os fatores da campanha que influenciam na aceitação das ofertas;

## 1.2. Importação das bibliotecas e carregamento dos dados
Importei as biblitoecas pandas, numpy, matplotlib, seaborn. E então carreguei o dados através do pd.read_csv()

# 🧱 2. Entendendo os dados
Através dos métodos shape, head(), tail() e info() busquei entender a estrutura dos dados. E percebi a necessidade de tratar outliers e checar nulos e duplicatas.
# 🧹 3. Limpeza e manipulação dos dados
## 3.1. Conferindo nulos e duplicatas
O dataset não possuía dados nulos ou duplicados
## 3.2. Os outliers (ou dados extremos)
Após notar o desbalanceamento dos dados, fiz a remoção de outliers nas colunas 'balance', 'duration' e 'campaign'
# 🔍 4. Análise Exploratória de Dados
## 4.1. O perfil dos clientes
![img1]()

A grande massa dos clientes está entre 20 e 60 anos de idade.

![img2]()

Os clientes do banco em maior número estão em posições de trabalho operacionais e de gerenciamento. Outra parcela relevante está em posições de técnico e administrativas.

![img3]()