# Pedro Grassi

Data Engineer focused on Python, SQL, APIs, AWS, Airflow, automation, and data quality.

![Python](https://img.shields.io/badge/Python-pipelines-blue)
![SQL](https://img.shields.io/badge/SQL-modeling-informational)
![AWS](https://img.shields.io/badge/AWS-data%20systems-orange)
![Airflow](https://img.shields.io/badge/Airflow-orchestration-lightgrey)

I build small data systems that are easy to run, test, and review. My portfolio uses one practical domain, SaaS billing analytics, to show the path from ingestion to reporting and platform operations.

## Portfolio Map

| Area | Repo | What to review |
| --- | --- | --- |
| Local web app | [billing-data-workbench](https://github.com/PGrassiGit/billing-data-workbench) | FastAPI UI, validation runs, profiling, reports |
| API ingestion | [api-ingestion-pipeline](https://github.com/PGrassiGit/api-ingestion-pipeline) | cursor sync, retry handling, dead-letter records |
| Warehouse modeling | [sql-elt-warehouse](https://github.com/PGrassiGit/sql-elt-warehouse) | MRR, churn, invoice collection, SQL checks |
| Orchestration | [airflow-orchestration-demo](https://github.com/PGrassiGit/airflow-orchestration-demo) | task boundaries, quality gate, retry settings |
| AWS processing | [aws-serverless-pipeline](https://github.com/PGrassiGit/aws-serverless-pipeline) | S3 zones, SQS DLQ, Lambda event handling |
| Data quality | [data-quality-contracts-lab](https://github.com/PGrassiGit/data-quality-contracts-lab) | contracts, referential checks, quarantine flow |
| Metadata | [metadata-lineage-catalog](https://github.com/PGrassiGit/metadata-lineage-catalog) | SQL lineage, data dictionary, catalog output |

## Main Signals

- I separate source data, business logic, and reporting outputs.
- I write tests for failure paths, not only happy paths.
- I keep cloud examples deployable later, but runnable locally first.
- I document tradeoffs, assumptions, and production notes.
- I avoid secrets, personal data, and account-specific values in repos.

## Suggested Review Path

1. Start with [billing-data-workbench](https://github.com/PGrassiGit/billing-data-workbench) for the interactive local app.
2. Review [sql-elt-warehouse](https://github.com/PGrassiGit/sql-elt-warehouse) for analytics modeling and metrics.
3. Open [api-ingestion-pipeline](https://github.com/PGrassiGit/api-ingestion-pipeline) for ingestion reliability.
4. Check [data-quality-contracts-lab](https://github.com/PGrassiGit/data-quality-contracts-lab) and [metadata-lineage-catalog](https://github.com/PGrassiGit/metadata-lineage-catalog) for platform thinking.
5. Use [airflow-orchestration-demo](https://github.com/PGrassiGit/airflow-orchestration-demo) and [aws-serverless-pipeline](https://github.com/PGrassiGit/aws-serverless-pipeline) to evaluate orchestration and AWS design.

## Portuguese

Sou Engenheiro de Dados com foco em Python, SQL, APIs, AWS, Airflow, automacao e qualidade de dados.

Meu portfolio usa billing SaaS como dominio unico para mostrar ingestao, modelagem, orquestracao, cloud, qualidade e metadata.
