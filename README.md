
<h1> Web scraping site aluguel de imóveis + PowerBI </h1>

<br>

![grafico plotly ambev](https://github.com/thiagobacelar/Imoveis_Recife_aluguel_AP/blob/master/ZApimoveis-dashbord.png)
<br>
<br>

<h1> O projeto </h1>

Com objetivo de analisar os aluguéis de imóveis, mais específico de apartamentos, em Recife, a ideia foi realizar um Web Scraping, uma extração de dados em sites, em seguida exportar os dados para o PowerBI e analisar os dados através de um dashboard. O site escolhido foi o zapimoveis.com.br, Utilizei Jupyter Notebook, Pandas, requests, geopandas e PowerBI 
para esse projeto.  

<br>
<br>

> ###  Etapas do projeto

1. #### Web Scraping
Inicialmente, criei o código em python que seria responsável por percorrer a lista de imoveis do site
utilizei BeautifulSoup e Requests para acessar o zapimoveis.com.br os itens que escolhi para extração foram 
Aluguel, Endereço, Medida m² e Quantidade de quartos. Com esses dados em mãos foi criado o dataframe dos imoveis.


2. #### Gerar localização a partir do endereço dos imóveis 
Logo após, foi necessário gerar a localização a partir do endereço dos imóveis foi utilizado o geopandas
parar converter os dados de endereço e criar uma coluna com a Localização do tipo geometry(POINT).


3. #### Exportar os dados para PowerBI
Ademais, com o dataframe finalizado, chegou a hora de exportá-lo com pandas em formato CSV para ser 
utilizado no PowerBI.


4. #### PowerBI
Já no PowerBi foi feito ETL onde tive que transformar a coluna de Localização em outras duas colunas a de 
Latitude e Longitude e modificar seus tipos para o formado aceito no powerBI. Dessa forma, foi possível criar 
o dashboard com mapa, médias e quantidade de imóveis.  


### Com a análise foi possível tirar algumas conclusões sobre aluguel de imoveis em recife, auxiliando assim uma futura tomada de decisão, segue as conclusões. 

+ Imóveis com apenas 1 quarto estão localizados em bairros mais nobres como Boa viagem, graças, aflitos, rosarinho e casa forte.
+ 45,5% dos imóveis tem 3 quartos é uma média de aluguel de R$:3.451,61 e média do metro quadrado fica em torno de 92m².
+ 38,05% dos imóveis tem 2 quartos é uma média de aluguel de R$:2.614,66 e média por metro quadrado fica em torno de 56m².
+ 9,25% dos imóveis tem 4 quartos é uma média de aluguel de R$:6.855,00 e média por metro quadrado fica em torno de 159m².
+ 7,2% dos imóveis tem 1 quarto é uma média de aluguel de R$:2.267,00 e média por metro quadrado fica em torno de 36m².
