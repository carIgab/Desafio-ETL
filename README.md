# Projeto ETL: Análise de Vendas de Produtos

Este projeto demonstra um fluxo de trabalho completo de **ETL (Extract, Transform, Load)** utilizando Python e a biblioteca Pandas. O objetivo é processar uma base de dados de vendas em formato Excel, extrair insights estratégicos e exportar os dados limpos para um formato compatível com bancos de dados modernos (JSON).

## 🚀 Tecnologias Utilizadas

* **Python 3.x**: Linguagem principal.
* **Pandas**: Biblioteca para manipulação e análise de dados.
* **Openpyxl**: Engine para leitura de arquivos Excel.
* **JSON**: Formato de saída para persistência em bases de dados NoSQL.

## 📋 Etapas do Processo

### 1. Extração (Extract)
Os dados são lidos a partir de um ficheiro Excel (`planilha_vendas_produtos.xlsx`). Esta planilha contém informações detalhadas sobre transações, incluindo clientes, lojas, produtos, quantidades e valores.

### 2. Transformação e Limpeza (Transform)
Nesta fase, os dados brutos são refinados:
* **Remoção de Colunas Irrelevantes**: Eliminamos as colunas `ID` e `CVM do Produto`, que são identificadores técnicos não necessários para a análise de negócio.
* **Tratamento de Dados Ausentes**: Remoção de linhas com valores nulos para garantir a integridade dos cálculos.

### 3. Análise de Dados (Insights)
O script realiza agregações para responder a perguntas de negócio fundamentais:
* **Cliente Destaque**: Identifica quem gastou o maior valor total.
* **Performance por Loja**: Determina qual unidade teve o maior faturamento.
* **Produto Líder**: Identifica o produto que gerou a maior receita bruta.

### 4. Carga (Load)
Os dados transformados são convertidos para o formato **JSON (orientado a registos)**. Este formato é o padrão para integração com APIs e inserção em bancos de dados como MongoDB ou Firebase.

## 📊 Exemplo de Saída da Análise

Ao executar o script, o sistema gera um resumo no terminal semelhante a este:

> **Melhor Cliente:** Daniel Oliveira | Total Comprado: R$ 42,335.76  
> **Melhor Loja:** Loja Web | Faturamento Total: R$ 81,700.96  
> **Produto Líder:** Fogão 4 Bocas | Receita Gerada: R$ 42,406.71  

## 🛠️ Como Executar

1. Instale as dependências necessárias:
   ```bash
   pip install pandas openpyxl
