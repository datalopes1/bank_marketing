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
![img1](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img1.png?raw=true)

A grande massa dos clientes está entre 20 e 60 anos de idade.

![img2](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img2.png?raw=true)

Os clientes do banco em maior número estão em posições de trabalho operacionais e de gerenciamento. Outra parcela relevante está em posições de técnico e administrativas.

![img3](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img3.png?raw=true)

50% dos clientes do banco tem como nível de educação o segundo grau completo, somente cerca de 30% tem ensino superior. O restante está distribuido entre o nível primiário e não informado.

![img4](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img4.png?raw=true)

Entre os clientes do banco 60% são casados, o restante está distribuido entre solteiro e divorciados.

![img5](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img5.png?raw=true)

Existe um número baixíssimo de clientes inadimplentes junto ao banco, o que mostra potencial para novos emprestimos.

![img6](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img6.png?raw=true)

![img7](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img7.png?raw=true)

Mais da metade dos clientes possui financiamento de imóvel, pessoas sem este tipo de divida tem maior potencial para adquirir produtos do bancário.

![img8](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img8.png?raw=true)

Existe uma margem muito grande de pessoas sem um emprestimo contratado, o que aponta possível disponibilidade de crédito para contratar produtos bancários.

### Trabalho x Aceitação do Produto
![img8](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img9.png?raw=true)
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img10.png?raw=true)

Estudantes são os clientes com maior taxa de conversão, seguidos por aposentados, desempregados e pessoas em função de gerencia. Estudantes e desempregados tem uma capacidade de endividamento baixa, e podem no futuro se tornar inadimplentes.

### Idade x Aceitação do Produto
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img11.png?raw=true)

Consumidores mais velhos tem maior tendência de aceitar o produto bancário, especialmente aqueles entre 30 e 50 anos de idade.

### Estado Civil x Aceitação do Produto
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img12.png?raw=true)

![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img13.png?raw=true)

Apesar do maior volume maior de aceitação do produto estar entre os clientes casados, a taxa de conversão é maior entre solteiros e divorciados.

### Escolaridade x Aceitação do Produto
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img14.png?raw=true)

![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img15.png?raw=true)

A taxa de conversão é maior em indivudos com nível superior completo e com nível educacional desconhecido, o maior volume se divide em nível de superior e de ensino médio completo.

### Balanço x Aceitação do Produto
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img16.png?raw=true)

Maior balanço em conta indica maior espaço no orçamento para um investimento, é outro público que deve ser focado.

### Financiamento Imobiliário x Aceitação do Produto
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img17.png?raw=true)

![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img18.png?raw=true)

A taxa de conversão sobre pessoas sem um financiamento imobiliário é o triplo das que tem, além do volume também ser maior.

### Emprestimos x Aceitação do Produto
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img19.png?raw=true)

![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img20.png?raw=true)

Pessoas sem emprestimos, claramente, tem maior potencial para adquirir novos produtos financeiros.

### Algumas conclusões
#### O cliente mais inclinado a contratar o produto tem:

- Entre 30 e 50 anos de idade;
- Maior balanço em conta;
- É solteiro ou divorciado;
- Não emprestimos ou financiamentos imobiliários ativos;
- Tem escolaridade de nível superior ou secundária;
- É estudante, aposentado ou está em cargos de gerencia;

A partir desses pontos, o time de marketing tem uma segmentação parar criar campanhas direcionadas para estes públicos.

## 4.2. A campanha
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img21.png?raw=true)

É necessário fazer um tracking melhor dos meios de contato, o celular é a forma mais comum mas existe um grande volume desconhecido.

![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img22.png?raw=true)

![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img23.png?raw=true)

![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img24.png?raw=true)

O maior volume é de 1 ou 2 contatos feitos, mais a frente vamos buscar saber a relação entre sucesso e o número de contatos.

### Meio de Contato x Aceitação da Campanha
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img25.png?raw=true)

![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img26.png?raw=true)

A maior taxa de sucesso e volume de sucesso está nos contatos por celular.

### Mês do Contato x Aceitação da Campanha
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img27.png?raw=true)

![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img28.png?raw=true)

Os meses com as maiores taxas de sucesso em conversão são dezembro, março, outubro e setembro. A época de fim de ano parece propicia para campanhas direcionadas. Podemos pensar isso também em campanhas segmentadas para os públicos com maior porcentagem de sucesso na contratação do produto.

### Duração das Ligações x Aceitação da Campanha
![img](https://i.imgur.com/BBl4RuX.png)

Ligações que passam de 3 minutos tem maior chance de terminar uma contratação.

### Número de Contatos x Aceitação da Campanha
![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img29.png?raw=true)

![img10](https://github.com/datalopes1/bank_marketing/blob/main/doc/img/img30.png?raw=true)

### Alguns insights sobre a campanha
- É necessário treinar a equipe para melhorar o convencimento na primeira ligação. Focar nos grupos mais suscetíveis ao aceite do produto, poderá trazer melhores resultados;
- O tempo de ligação também é um fator, romper a barreira dos 3 minutos traz maior probabilidade de fechamento;
- Os meses de março, setembro, outubro e dezembro são onde se tem maior taxa de conversão, campanhas bem segmentadas combinadas com essas datas podem trazer bons resultados.

# ✅ 5. Conclusões

![img](https://camo.githubusercontent.com/8365c5e11ea829286c7975c86d2f06bd509d7714e53784345816dfe92f5e7d9f/68747470733a2f2f696d616765732e756e73706c6173682e636f6d2f70686f746f2d313631363830333134303334342d3636383261666231336364613f713d383026773d32303730266175746f3d666f726d6174266669743d63726f702669786c69623d72622d342e302e3326697869643d4d3377784d6a4133664442384d48787761473930627931775957646c664878386647567566444238664878386641253344253344)

Ao fim foi possível traçar um perfil de clientes em potencial para contratação de serviços do banco, além de buscar entender fatores que possam aumentar a efetivividade das próximas campanhas. Entender o comportamento dos consumidores e o seu perfil é excencial para auxiliar o marketing a otimizar seus resultados e diminuir seus custos, além de naturalmente aumentar os resultados comerciais.