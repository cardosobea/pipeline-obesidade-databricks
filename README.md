# Pipeline de Dados - Análise de Obesidade

Projeto desenvolvido para a Sprint de Engenharia de Dados da Pós-Graduação em Ciência de Dados e Analytics da PUC-Rio.

## Objetivo

Construir um pipeline de dados em ambiente Cloud utilizando o Databricks para coletar, armazenar, transformar e analisar dados relacionados a hábitos alimentares, estilo de vida e níveis de obesidade.

## Dataset

Foi utilizado o Obesity Dataset, obtido na plataforma Kaggle.

A base utilizada possui:

- 1.610 registros
- 15 variáveis
- Informações demográficas
- Hábitos alimentares
- Atividade física
- Estilo de vida
- Classificação de obesidade

O arquivo original está disponível na pasta:

`data/`

## Arquitetura

O pipeline foi desenvolvido utilizando a Arquitetura Medalhão:

### Bronze

Tabela:

`bronze_obesidade_raw`

Responsável pelo armazenamento dos dados brutos, sem transformações.

### Silver

Tabela:

`silver_obesidade_tratada`

Nesta camada foram realizadas:

- Tradução dos códigos numéricos para valores descritivos;
- Padronização das categorias;
- Padronização dos níveis de consumo de líquidos;
- Padronização dos meios de transporte;
- Criação da variável `faixa_etaria`;
- Criação da variável `nivel_atividade`;
- Criação da variável `nivel_uso_tecnologia`;
- Validações de qualidade dos dados.

### Gold

Foram criadas dez tabelas analíticas:

- `gold_fastfood_obesidade`
- `gold_atividade_fisica`
- `gold_consumo_vegetais`
- `gold_historico_familiar`
- `gold_historico_vs_habitos`
- `gold_meio_transporte`
- `gold_tempo_tecnologia`
- `gold_consumo_agua`
- `gold_faixa_etaria`
- `gold_perfil_obesidade`

Essas tabelas foram utilizadas para responder às perguntas de negócio relacionadas aos fatores associados à obesidade.

## Notebooks

O projeto está dividido nos seguintes notebooks:

### 01_validacao_bronze

Responsável pela validação dos dados carregados na camada Bronze.

### 02_silver_obesidade

Responsável pelas transformações, padronizações e criação da camada Silver.

### 03_gold_obesidade

Responsável pela criação das tabelas analíticas da camada Gold.

## Tecnologias utilizadas

- Databricks Free Edition
- SQL
- Delta Lake
- Git
- GitHub

## Documentação

A documentação completa do desenvolvimento, arquitetura, transformações, consultas, resultados e análises está disponível na pasta:

`documentacao/`

## Principais resultados

As análises indicaram associações relevantes entre obesidade e fatores como:

- consumo de fast food;
- frequência de consumo de vegetais;
- histórico familiar;
- faixa etária;
- consumo de líquidos;
- meio de transporte.

Os resultados representam associações observadas no conjunto de dados e não relações de causalidade.

## Autora

Ana Beatriz Cardoso da Silva

Pós-Graduação em Ciência de Dados e Analytics - PUC-Rio
