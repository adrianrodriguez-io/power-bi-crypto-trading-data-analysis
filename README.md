# Power BI Crypto Trading Data Analysis

Hi, 

This is a project in wich you will find a Power BI visualization based on crypto trading data. For checking it out the live Power BI visualization click <a target='_blank' href='https://adrianrodriguez-io.github.io/power-bi-crypto-trading-data-analysis/'>HERE</a> .

## Challengue

The goal of this project was to develop a data visualization about crypto trading market data for analyzing trends and relations between measured traded crypto currencies. The project has been documented in a functional document, created for the ideation of the data workflow and Power Bi visualization as well as the final result of the Power BI developed (see functional section below or download the Crypto market analysys functional document (PDF) ).

### 1. Ingesting and load data
It was needed to pull data from a crypto exchange public API endpoints wich was done using python. Some challlengues was that the data originally is in json format so it was needed to make some transformations in order to structure that in order to store that into csv format. Mainly pandas, numpy and igraph python libraries were used. Some tweeks into the data was to use pandas library to create an index for the different cryptos traded in order to visualize that as a network graph using igraph python library. I used pandas to join different dataframes created along the ingest-load script as well as using pandas rank method for having an index for every crypto currency. Having an index id for every crypto in the data was needed because igraph python library requires to configure the graph using indexes instead of categorical values like names. 

### 2. Visuals
Basically I wanted to see trends on number of transactions and volume traded for a given period as well as visualize the network graph of relations between cryptos traded. I choosed Power Bi as the data visualization tool, as you can see in the Functional document of the projects. At the beginning I tried to develop a power bi python visual using igraph library but it seems that it dosent work or have some bug. So instead of having a python visual I used a power bi visual call Network Navigator Visual wich is convenient for the prupouse of the analysis. 

## Insights

In the Power BI we can find that there are some differences in transactions by day and volume traded. Crypto market is huge, there are millions of transactions done and there are a lot of crypto currencies to take into account, Bitcoin or Ethereum are not the only cryptos currencies traded, instead, there are a bunch of other cryptos. These days (date: 2022-09-25) the main currency to take into account for trading cryptos is the USD, wich is the one in wich cryptos are traded. USD is the currency wich is mainly converted for the most of transactions as fiat currencies are mainly the destination of trades. We can see as well that EUR and GBP are other currencies in the scoreboard by number of transactions. Bitcoin and Etherum have suffered depreciation of their values, as well as the rest of cryptos, mainly due to the bear scenario of the market. 

## Files

### 1. Functional project.pdf 
PDF containing different slides about the ideation and initials stages of the project.

### 2. Ingest-load.ipynb 
You can find an ingest and load jupyter notebook using python for ingesting crypto data from a crypto exchange pulled from its public API endpoints. This script generates three datasets wich are stored into csv. 1. vertexs.csv > contains a table for all crypto currencies available. 2. currencypairs.csv > a relation of all pairs of crypto currencies that can be traded. And 3. OHLC_trades.csv > this contain data about prices and volumes for all pairs of cryptos traded in different dates. 

### 3. graph-visualization.ipynb
This is a jupyter notebook using python for visualizating an igraph visualization in order to see the network of all crypto currencies traded (cryptos trades dataset can be filtered previuosly in ingest-load.ipynb).

### 4. index.html (pbi-crypto-data-analysis)
This is an embebeded Power Bi in the repository in wich you can see different charts and graph visualizations. For checking it out the live <a target='_blank' href='https://adrianrodriguez-io.github.io/power-bi-crypto-trading-data-analysis/'>Power Bi please click here</a>.

## Functional project

### A. Data Visualization (Power BI)
<br>
<img width='600'  src='https://github.com/adrianrodriguez-io/power-bi-crypto-data-analysis/blob/main/images/Data%20visualization.png'></img>

### B. Data model
<br>
<img width='600'  src='https://github.com/adrianrodriguez-io/power-bi-crypto-data-analysis/blob/main/images/Data%20Model.png'></img>

### C. Data workflow
<br>
<img width='600'  src='https://github.com/adrianrodriguez-io/power-bi-crypto-data-analysis/blob/main/images/Data%20workflow.png'></img>

### D. Graph
<br>
<img width='600'  src='https://github.com/adrianrodriguez-io/power-bi-crypto-data-analysis/blob/main/images/Graph.png'></img>
