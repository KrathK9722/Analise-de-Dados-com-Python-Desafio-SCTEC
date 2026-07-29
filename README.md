

Análise Exploratória de Dados da base Sample Superstore

Acesse o Google Colab [aqui](https://colab.research.google.com/drive/1PuaSIcAf60PJxdX2O8KOE3IO9Sh9Wye2?usp=sharing).



# Documentação do Projeto


## Identificação do projeto

Projeto: Análise Exploratória de Dados da base Sample Superstore

Autor: Arthur Henrique Kochan

Curso: Introdução ao Data Science

Tipo de entrega: Desafio Extra C2

## Objetivo do projeto

O objetivo deste projeto foi realizar uma Análise Exploratória de Dados usando a base Sample Superstore, uma base pública em formato CSV com informações de vendas de uma rede varejista.

A análise foi feita para entender o comportamento geral das vendas, do lucro, dos descontos, das categorias de produtos, das subcategorias, dos segmentos de clientes e das regiões atendidas pela empresa.

O projeto foi desenvolvido em Python, com uso de bibliotecas próprias para análise de dados e criação de gráficos.

## Arquivos do projeto

O projeto é composto pelo notebook em Python, pelo arquivo CSV da base Sample Superstore e por esta documentação em formato Markdown.

O notebook contém todo o desenvolvimento da análise, desde a importação das bibliotecas até a conclusão final. O arquivo CSV contém os dados utilizados no projeto. Esta documentação explica o que foi feito, quais decisões foram tomadas no tratamento dos dados, quais insights foram encontrados e como visualizar o projeto.

## Ferramentas utilizadas

O projeto foi desenvolvido em Python, no ambiente Google Colab.

Foram utilizadas bibliotecas como pandas para leitura, organização, tratamento e análise dos dados, matplotlib para criação das visualizações gráficas e seaborn para apoio em algumas visualizações.

A base utilizada foi a Sample Superstore, em formato CSV.

## Etapas de desenvolvimento

## 1. Importação das bibliotecas

No início do notebook foram importadas as bibliotecas necessárias para o projeto. A biblioteca pandas foi usada para manipular os dados em formato de tabela. A biblioteca matplotlib foi usada para criar gráficos. A biblioteca seaborn foi usada para apoiar algumas visualizações.

## 2. Carregamento dos dados

A base Sample Superstore foi carregada no notebook a partir de um arquivo CSV. O carregamento foi feito usando a função read_csv da biblioteca pandas.

Também foi utilizada a codificação latin1 para garantir que o arquivo fosse lido corretamente, sem erros causados por caracteres especiais.

## 3. Visualização dos dados brutos

Depois do carregamento, foi feita uma visualização inicial da base de dados. Foram observadas as primeiras linhas da tabela, o tamanho da base, os tipos de dados das colunas e algumas estatísticas gerais.

Essa etapa foi importante para entender a estrutura inicial do arquivo e saber quais tratamentos seriam necessários antes da análise.

## 4. Tratamento dos dados

Para preservar os dados originais, foi feita uma cópia da base antes das alterações. Depois disso, as colunas foram traduzidas para português, facilitando a leitura do código e das análises.

Também foram verificadas duplicações e valores nulos. Nenhum valor nulo ou duplicado foi encontrado, por isso não foi necessário remover registros da base.

As colunas de datas foram convertidas para o tipo datetime, permitindo o uso correto de funções de data da biblioteca pandas. A partir dessas datas, foram criadas colunas auxiliares como ano, mês, ano_mes e dias_para_envio.

As colunas vendas, quantidade, desconto e lucro foram verificadas para confirmar que estavam em formato numérico. Também foi feita a verificação de valores zerados. Os valores de desconto igual a zero foram mantidos porque representam vendas sem desconto. Os valores de lucro igual a zero também foram mantidos porque representam vendas sem lucro e sem prejuízo.

A coluna CEP foi convertida para texto, pois não seria usada em cálculos matemáticos, mas sim como informação de localização.

## 5. Identificação de outliers

Foi feita a análise de possíveis outliers, principalmente nas colunas de vendas e lucro. Foram observados valores muito altos de lucro, grandes prejuízos e vendas muito acima do padrão.

Esses outliers não foram removidos, pois podem representar vendas reais e pontos importantes para a análise da empresa. A decisão foi manter esses dados para não perder informações relevantes.

## 6. Validação pós tratamento

Depois do tratamento, a base foi verificada novamente. Foram conferidos os tipos dos dados, os nomes das colunas, as estatísticas gerais, o tamanho da base e as primeiras linhas da tabela tratada.

Essa etapa serviu para garantir que o tratamento foi feito corretamente e que os dados estavam prontos para a análise exploratória.

## 7. Análise exploratória

Na análise exploratória foram criadas tabelas e agrupamentos para entender melhor os dados da empresa.

Foram feitos agrupamentos por categoria, subcategoria, segmento, desconto, região e ano. Também foram feitos filtros para separar vendas com prejuízo, além de análises sobre lucro médio por desconto e prejuízo por subcategoria.

Foram analisadas vendas e lucro por categoria, vendas e lucro por segmento, vendas e lucro por região, evolução anual do lucro positivo e do prejuízo, subcategorias com maior prejuízo e relação entre desconto e lucro médio.

## 8. Visualizações gráficas

Na etapa 8 do notebook estão os gráficos criados para apoiar a análise. Os gráficos mostram visualmente os principais resultados encontrados durante a análise exploratória.

Foram criados gráficos sobre vendas e lucro por categoria, lucro positivo e prejuízo anual, vendas e lucro por região, subcategorias com maior prejuízo, lucro médio por nível de desconto, vendas e lucro por segmento e vendas por categoria dentro de cada segmento.

As explicações de cada gráfico também estão na etapa 8 do notebook, logo abaixo de cada visualização.

## 9. Conclusão

Na etapa 9 do notebook está a conclusão final do projeto. Nessa parte, são resumidos os principais resultados encontrados na análise e o que eles mostram sobre o desempenho da empresa.

## Principais decisões tomadas durante o tratamento dos dados

A primeira decisão foi copiar a base original antes de fazer alterações, evitando modificar diretamente os dados brutos.

As colunas foram traduzidas para facilitar a leitura e deixar o código mais simples de entender.

As datas foram convertidas para datetime para permitir análises por ano, mês e período.

As colunas auxiliares ano, mês, ano_mes e dias_para_envio foram criadas para ajudar nas análises temporais.

Os valores nulos e duplicados foram verificados, mas não foi necessário remover registros porque não foram encontrados problemas desse tipo.

Os valores zerados em desconto e lucro foram mantidos, pois representam situações possíveis dentro da base.

Os outliers também foram mantidos porque podem representar vendas reais, grandes lucros ou grandes prejuízos importantes para a análise.

A coluna CEP foi tratada como texto porque não representa uma medida numérica para cálculo.

## Insights do projeto

Os textos abaixo foram mantidos conforme os insights escritos no notebook.

Podemos ver no gráfico acima que a categoria de Technology é a que mais tem vendas e lucro, a categoria Furniture tem muitas vendas mas pouco lucro isso pode indicar que problemas estão ocorrendo em relação aos descontos ou precificação de produtos.

O gráfico mostra que a categoria Office Supplies, mesmo apresentando um volume de vendas menor que Technology e Furniture, possui um lucro relevante. Isso indica que essa categoria pode ter boa rentabilidade e merece atenção estratégica da empresa.

Esse resultado sugere que Office Supplies pode ser uma oportunidade para maior investimento em campanhas, estoque ou ações comerciais, já que consegue gerar lucro alto mesmo com menor volume de vendas.

No gráfico acima temos a visualização da evolução do lucro positivo e do prejuizo anual em algumas vendas, ambos subiram como consequencia de um maior volume de vendas mas podemos ver que a relação enter lucro positivo e prejuizo anual tem sido cada vez mais distante para o lado positivo, aumentando o lucro líquido anual total.

O gráfico das regiões nos permite entender qual local trás um maior volume de vendas e lucro total para a empresa, o lucro neste gráfico é o lucro total recebido entre os anos de 2014 a 2017 que são os anos apresentados nos dados originais da empresa. Com essa visualização conseguimos entender onde focar em relação a publicidade e marketing dos produtos.

Entender as subcategorias com maior prejuizo nos ajuda a encontrar problemas tanto no volume de vendas de alguns produtos quanto em relação ao próprio valor deles e o desconto sobre suas vendas, como podemos ver o item com maior prejuizo total é o mesmo com o maior desconto e a média de desconto nas vendas com prejuizo é de 48% de desconto mostrando que talvez o desconto seja uma das causas do prejuizo além do próprio volume de vendas e da precificação dos produtos.

Nesse gráfico é possivel observar melhor a relação entre desconto e lucro médio. Os descontos de 0% e 10% ainda apresentam lucro médio positivo, mas a partir de 30% o lucro médio passa a ficar negativo. As maiores perdas aparecem principalmente nas faixas de 45% e 50% de desconto, com destaque também para descontos altos, como 70% e 80%. Isso mostra que descontos maiores podem estar ligados à queda do lucro e, em alguns casos, ao prejuízo nas vendas.

Isso indica que a empresa precisa ter mais cuidado com a política de descontos, porque vender com desconto alto nem sempre significa vender melhor. Em alguns casos, o desconto pode estar reduzindo ou até eliminando o lucro total.

Agora que ja abordamos os produtos que tem um retorno negativo, a evolução anual do lucro e as regiões com maior venda, podemos observar em qual segmento o volume de vendas é maior e entender como isso está relacionado com o lucro dos produtos. Nesse gráfico acima podemos visualizar que o segmento com maior número de vendas e lucro é o Consumer, mostrando sua relevância para a empresa.

No gráfico acima é possivel ver que a categoria Technology vende mais dentro dos três segmentos analisados: Consumer, Corporate e Home Office. Mesmo que em alguns segmentos a diferença para as outras categorias não seja tão grande, ela aparece como a categoria com melhor desempenho em todos eles. Isso ajuda a entender por que, na análise geral por categoria, Technology aparece com o maior volume de vendas. Mostrando que esse resultado vem de um volume de vendas maior e mais consistente.

## Conclusão do notebook

A análise mostrou que a empresa possui lucro líquido positivo ao longo dos anos, mesmo existindo vendas com prejuízo. A categoria Technology aparece como a principal em vendas e lucro, enquanto Furniture apresenta muitas vendas, mas pouco lucro, indicando possível problema de rentabilidade.

Também foi possível observar que descontos mais altos estão ligados à queda do lucro médio, principalmente a partir de 30%. Algumas subcategorias, como Binders, Tables e Machines, concentram os maiores prejuízos, o que mostra que esses produtos precisam de mais atenção.

O segmento Consumer foi o que apresentou maior volume de vendas e lucro, mostrando sua importância para o faturamento da empresa. Além disso, Technology teve bom desempenho em todos os segmentos, o que explica seu destaque na análise geral.
As regiões com maior lucro foram West e East, indicando também regiões onde o investimento pode render um lucro ainda maior.

Com isso, a análise ajuda a entender melhor onde a empresa vende mais, onde lucra mais e onde pode estar perdendo dinheiro.

## Como executar ou visualizar o projeto

Para visualizar o projeto, abra o arquivo do notebook no Google Colab ou em outro ambiente compatível com arquivos .ipynb.

Com o notebook aberto, execute as células em ordem, de cima para baixo. Primeiro serão importadas as bibliotecas, depois os dados serão carregados, tratados e analisados. Em seguida, as tabelas e gráficos serão gerados. 

OBS: O arquivo CSV é chamado no notebook .ipynb por meio do link de um Drive público que contém o mesmo CSV original enviado junto da documentação, portanto não é necessário alterar o código ou colocar o arquivo CSV em alguma pasta específica.

A etapa 8 do notebook contém os gráficos e suas explicações. A etapa 9 contém a conclusão final do projeto. Para entender os resultados, basta executar o notebook até o final e visualizar os gráficos e os textos explicativos nessas etapas.

