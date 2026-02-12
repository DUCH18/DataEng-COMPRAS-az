

#Azure Data Engineering Pipeline (ADF + Databricks)

Este projeto demonstra um pipeline de engenharia de dados na Azure, utilizando Azure Data Factory para ingestão de dados e Azure Databricks para transformação, seguindo o padrão Medallion Architecture (Bronze → Silver).

Os dados são extraídos de um banco relacional, armazenados inicialmente como Parquet (Bronze) e depois transformados e persistidos como Delta Tables (Silver) no Azure Data Lake Storage Gen2.
<img width="1536" height="1024" alt="ch Image Feb 12, 2026, 04_38_16 PM" src="https://github.com/user-attachments/assets/31e1fef2-0ad8-452a-92d5-fca253f8f96d" />

🏗️ Arquitetura

Fluxo do pipeline:

Fonte de Dados

SQL Server (ou outro banco relacional)

Ingestão

Azure Data Factory copia os dados para o Data Lake

Camada Bronze

Dados brutos armazenados em Parquet

Sem transformações

Processamento

Azure Databricks realiza as transformações necessárias

Camada Silver

Dados tratados e persistidos em Delta Lake

🔐 Segredos e credenciais são gerenciados via Databricks Secret Scopes.

📷 Diagrama da arquitetura
(Adicionar a imagem no repositório, por exemplo em /docs/architecture.png, e referenciar aqui)

![Arquitetura](docs/architecture.png)

🛠️ Tecnologias Utilizadas

Azure Data Factory

Azure Databricks (Spark)

Azure Data Lake Storage Gen2 (ADLS)

Delta Lake

Parquet

SQL Server (fonte de dados)

📂 Estrutura do Projeto
.
├── adf/
│   └── pipelines/
├── databricks/
│   ├── 
│   └── bronze_to_silver_transformation.ipynb
├── docs/
│   
└── README.md
