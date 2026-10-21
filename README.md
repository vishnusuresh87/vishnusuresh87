

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=170&section=header&text=Vishnu%20Suresh&fontColor=ffffff&fontSize=46&fontAlignY=38&desc=Data%20%2F%20Analytics%20Engineer&descSize=18&descAlignY=60" alt="Vishnu Suresh - Data / Analytics Engineer" />

**Modern data stack · Lakehouse · Warehouse modelling · Cloud native pipelines **

![Status](https://img.shields.io/badge/Status-Open%20to%20work%20(UK)-2ea44f?style=flat-square)
![MSc](https://img.shields.io/badge/MSc-Data%20Science%2C%20Surrey-1f6feb?style=flat-square)
![Cert](https://img.shields.io/badge/Certified-Azure%20Databricks%20Data%20Engineer-ff3621?style=flat-square&logo=databricks&logoColor=white)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/YOUR-LINKEDIN-USERNAME)
<[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-0f2027?style=for-the-badge&logo=githubpages&logoColor=white)](https://vishnusuresh87.github.io)
-->
<
[![Email](https://img.shields.io/badge/Email-Say%20hello-ea4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:vishnusuresh87@gmail.com)
-->

</div>

---

## 👋 About

I build data pipelines that turn raw, messy sources into trusted, documented, tested datasets that analysts and models can use without asking questions.

My first "SQL" was balancing branch ledgers. I spent ten years at **Punjab National Bank**, starting in branch operations and forex and finishing as **Data Engineer – ETL & Data Integration** in the Data Analytics Wing, working on enterprise ETL with Oracle, IBM DataStage and SQL.
I then completed an **MSc in Data Science at the University of Surrey** and now build cloud-native pipelines on the modern data stack.

That combination is my edge: I understand what a number means to the business that produces it, and I know how to move it reliably at scale.

---

## 🚀 Featured projects

| Project | What it demonstrates | Stack | Links |
|---|---|---|---|
| **[EconPulse Analytics](https://github.com/vishnusuresh87/econpulse-analytics)** | Automated ELT of World Bank and FX data, with incremental dbt models, sensor-based orchestration and a real-exchange-rate dashboard | Airbyte · Snowflake · dbt · Airflow · Streamlit | [Repo](https://github.com/vishnusuresh87/econpulse-analytics) |
| **[Spark E-Commerce Recommendation Pipeline](https://github.com/vishnusuresh87/spark-ecommerce-recommendation)** | Medallion lakehouse on Databricks with Unity Catalog governance, RFM segmentation and ALS recommendations, tested with pytest | Databricks · PySpark · Delta Lake · MLflow | [Repo](https://github.com/vishnusuresh87/spark-ecommerce-recommendation) |
| **[Cancer Recurrence Platform](https://github.com/vishnusuresh87/cancer-recurrence-platform)** | A data-to-model-to-app system: dbt warehouse, survival model, four microservices and a React client | dbt · PostgreSQL · Redis · Docker · React | [Repo](https://github.com/vishnusuresh87/cancer-recurrence-platform) |
| **[Biomedical NER with PubMedBERT](https://github.com/vishnusuresh87/NLP-token-classification)** | Fine-tuning a transformer for token classification, with error analysis and a deployed inference app | PubMedBERT · Hugging Face · Streamlit | [Repo](https://github.com/vishnusuresh87/NLP-token-classification) · [Live app](https://nlp-token-classification-biomedical-ner.streamlit.app/) |

<details>
<summary><b>EconPulse: how the pipeline fits together</b></summary>

```mermaid
flowchart LR
    A[World Bank API] --> C[Airbyte]
    B[Open Exchange Rates API] --> C
    C --> D[(Snowflake RAW)]
    D --> E[dbt STG<br/>flatten + dedupe]
    E --> F[dbt INT<br/>rolling volatility]
    F --> G[dbt MARTS<br/>PPP + risk tiers]
    G --> H[Streamlit dashboard]
    I{{Airflow DAG<br/>06:00 UTC}} -. triggers + sensors .-> C
    I -. dbt run + test .-> E
```

</details>

<details>
<summary><b>Lakehouse pipeline: Bronze → Silver → Gold → ML</b></summary>

```mermaid
flowchart LR
    A[Raw CSVs<br/>UC Volume] --> B[(Bronze<br/>strict schemas)]
    B --> C[(Silver<br/>cleaned + identity resolved)]
    C --> D[(Gold<br/>KPIs + RFM features)]
    D --> E[KMeans<br/>5 segments]
    D --> F[ALS<br/>top-10 recs]
    E --> G[MLflow +<br/>UC Model Registry]
    F --> G
```

</details>

---

## Tech stack

| Area | Tools |
|---|---|
| **Warehouse & Lakehouse** | ![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white) ![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white) ![Delta Lake](https://img.shields.io/badge/Delta%20Lake-00ADD4?style=flat-square&logo=delta&logoColor=white) ![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat-square&logo=googlebigquery&logoColor=white) |
| **Transform & Orchestrate** | ![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white) ![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white) ![Airbyte](https://img.shields.io/badge/Airbyte-615EFF?style=flat-square&logo=airbyte&logoColor=white) ![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apachespark&logoColor=white) |
| **Languages** | ![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Shell](https://img.shields.io/badge/Shell-4EAA25?style=flat-square&logo=gnubash&logoColor=white) |
| **ML & NLP** | ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white) ![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white) ![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black) |
| **Cloud & DevOps** | ![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white) ![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) |
| **Enterprise & Legacy ETL** | ![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white) ![IBM](https://img.shields.io/badge/IBM%20DataStage-052FAD?style=flat-square&logo=ibm&logoColor=white) |
| **Serving & Apps** | ![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) |

---



## What I'm focused on

- **Data modelling:** dimensional design, medallion layers, incremental strategies
- **Modern data stack:** dbt, Airflow, Airbyte, Databricks, open table formats
- **Data quality:** tests, freshness checks, reconciliation (a habit from banking)
- **Currently studying:** GCP Professional Data Engineer
- **Also exploring:** agentic AI, deep learning and LLMs

---

## 🤝 Let's talk

I'm looking for **Data Engineer / Analytics Engineer** roles in the UK, and I'm happy to collaborate on open-source ETL, BI and ML projects.

- [LinkedIn](https://www.linkedin.com/in/vishnusuresh87/)

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,100:0f2027&height=90&section=footer" alt="" />
</div>
