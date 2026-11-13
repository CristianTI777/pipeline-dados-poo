# Pipeline de Dados: Fusão de Bases (JSON & CSV) com Python e POO

Pipeline de Engenharia de Dados (ETL) desenvolvido em Python utilizando Programação Orientada a Objetos (POO) para consolidar e padronizar bases de vendas provenientes da fusão de duas empresas.

## Contexto do Problema

Após a fusão entre duas empresas (**Empresa A** e **Empresa B**), a equipe de BI e Analytics precisou unificar os dados de vendas para gerar relatórios consolidados. O desafio técnico envolveu lidar com fontes heterogêneas:
* **Empresa A:** Dados extraídos em formato `.json`.
* **Empresa B:** Dados extraídos em formato `.csv`, com nomenclatura de colunas divergente.

Além da carga inicial, o pipeline foi arquitetado como uma classe reutilizável para execuções recorrentes nos meses seguintes.

## Arquitetura do Projeto

```text
pipeline_dados/
├── data_raw/               # Dados brutos originais (JSON e CSV)
├── data_processed/         # Dados tratados e consolidados prontos para BI
├── notebooks/              # Exploração e prototipagem inicial (Jupyter)
├── scripts/
│   ├── processamentos_dados.py  # Classe Dados com toda a lógica ETL
│   └── fusao_mercado_fev.py     # Script orquestrador de execução do pipeline
└── .gitignore