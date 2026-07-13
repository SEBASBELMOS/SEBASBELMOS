# ⚡ Hi, I'm Sebastian

**Data & AI Engineer** building dashboards, ETL pipelines, automation workflows and practical AI systems, and explaining them clearly. Currently finishing my Data & AI Engineering degree at UAO.

I like turning messy data, unclear processes and complex technical ideas into **clean insights, reliable systems and simple explanations**. Alongside my technical work, I teach Spanish online to international students, which has sharpened how I communicate, structure ideas and explain technical concepts to any level.

🌐 **See it all live: [sebasbelmos.github.io](https://sebasbelmos.github.io)**

<p align="left">
  <a href="https://sebasbelmos.github.io">
    <img src="https://img.shields.io/badge/Portfolio-C9A24B?style=for-the-badge&logo=githubpages&logoColor=black" alt="Portfolio">
  </a>
  <a href="https://www.linkedin.com/in/sebasbelmos/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="https://www.youtube.com/channel/UCeYaQhjA-N6YVd6RNTdhBeA">
    <img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube">
  </a>
</p>

---

## 💻 What I Do

- Build **ETL pipelines and star-schema data warehouses** with **Python, SQL, PostgreSQL and Apache Airflow**.
- Design **Power BI & Looker Studio dashboards** and KPI reports for decision-making.
- Build **data pipelines** and apply practical ML/statistics concepts from university and portfolio projects.
- Build **AI orchestration and automation workflows** with **n8n, Claude Code, Cursor, ChatGPT and prompt engineering** to reduce manual, repetitive work.
- Use **multi-agent workflows** with documentation and human-in-the-loop review to prototype, debug and document faster.
- Explain technical ideas clearly, a teaching habit I bring to docs and dashboards.

---

## 🚀 Featured Projects

### GeoVision-CLIP Cali
**[🌐 Live App](https://analiticalastdance-geovision-cali-frontend.hf.space)** · **[📑 API Docs](https://analiticalastdance-geovision-cali-api.hf.space/docs)** · **[💻 Code](https://github.com/SEBASBELMOS/GeoVision-CLIP-Cali)**

> *A live web map that forecasts air pollution across the city of Cali, days ahead.*

End-to-end GeoAI system that estimates air pollution (**NO₂, SO₂, O₃**) across ~**380 km²** of Cali, Colombia. The pipeline combines RemoteCLIP + sparse autoencoders, a bidirectional ConvLSTM and 3D ST-Kriging residual correction over a **1,920-cell grid**, with T+1 / T+3 / T+7 day forecasts and uncertainty quantification. University final project, built by a **team of 3**.

**My role:** the **data engineering** (ingesting 5 satellite/ground sources into Zarr/Parquet, with an MD5-verified manifest of **74,439 files / 108 GB**), software architecture, FastAPI backend (15 REST endpoints), React + Leaflet frontend (1,920 cells rendered on canvas), Docker multi-stage build, pytest suite, DevOps, documentation and Hugging Face Spaces deployment, with hands-on exposure to the geospatial, statistical and ML components.

**Highlights**
- **R² = 0.807** (spatial LOO-CV for SO₂ + O₃, after residual correction).
- Processed **93.1 GB of Sentinel-2 imagery**; fully reproducible (SEED=42, MD5-verified).
- Live public **API + SPA** on Hugging Face Spaces, with **26/26 backend tests passing**.

**Tech:** Python · PyTorch · RemoteCLIP · ConvLSTM · PyKrige · FastAPI · React · TypeScript · Leaflet · Docker · Hugging Face Spaces

---

### [Spotify Analytics ETL Pipeline](https://github.com/SEBASBELMOS/spotify-analytics-etl-pipeline)
> *Turned 114k+ messy music records into clean dashboards on song and award trends.*

Production-ready ETL pipeline integrating **114,000+ Spotify tracks** and **4,810 Grammy records** into a unified analytics platform. Automated extraction, cleaning and transformation with **Apache Airflow** (daily scheduling, monitoring, error handling), deployed on **GCP** with Docker and PostgreSQL. Reduced duplicate records by **28.6%** and generated **81,941 enriched entries**, surfaced through Power BI dashboards.

**Tech:** Python · Apache Airflow · PostgreSQL · GCP · Docker · Power BI

---

### [Global Happiness Prediction Pipeline](https://github.com/SEBASBELMOS/world-happiness-ml-pipeline)
> *A model that predicts how happy a country is from its economic and social data.*

End-to-end ML pipeline predicting national happiness scores across **164 countries** (World Happiness Report 2015–2019). Evaluated four regression models and selected **Random Forest (R² = 0.8639, RMSE = 0.415)**, with a real-time **Apache Kafka** streaming architecture processing predictions at sub-second latency and PostgreSQL audit trails capturing inputs and outputs.

**Tech:** Python · scikit-learn · Apache Kafka · PostgreSQL · Docker · Pandas

---

### [LinkedIn Job Postings ETL](https://github.com/SEBASBELMOS/LinkedIn-Jobs-Posting)
> *Turned 123k+ job postings into clean dashboards on hiring trends, skills and salaries.*

End-to-end data engineering pipeline over **123,000+ job postings**: ingestion from Kaggle, cleaning, and a **star-schema data warehouse** (fact + dimension tables) in **PostgreSQL** (cloud-deployable on GCP, AWS RDS or Supabase). The ETL is orchestrated with **Apache Airflow** (raw → cleaned → analytics layers) and surfaced through Power BI dashboards on job trends, salaries and company patterns.

**Tech:** Python · Pandas · PostgreSQL · Apache Airflow · Star Schema · Power BI

---

### [Data-Driven Hiring ETL](https://github.com/SEBASBELMOS/data-driven_hiring_analysis)
> *Analysed 50k job applicants to reveal who gets hired and why.*

ETL and analytics workflow over **50,000 candidate records**: SQLAlchemy-based ingestion into PostgreSQL, EDA, and a cleaned analytics dataset. Surfaced data-quality issues and a selective hiring funnel (**~13% hired**), with insights by seniority, technology and geography.

**Tech:** Python · SQLAlchemy · PostgreSQL · Poetry · Pandas · Power BI

---

### [Higher Education Graduates in Colombia](https://lookerstudio.google.com/reporting/fbf76da4-9963-4152-937b-44ca32ae93b8/page/p_uounofjj1c)
> *An interactive dashboard showing what and where Colombians graduate.*

**[Live Looker Studio dashboard](https://lookerstudio.google.com/reporting/fbf76da4-9963-4152-937b-44ca32ae93b8/page/p_uounofjj1c)** on official **SNIES / datos.gov.co** data, analysing Colombian higher education graduates from **2016 to 2020** by field of knowledge, education level and department. ([source repo](https://github.com/SEBASBELMOS/colombia-graduates-dashboard))

**Tech:** Looker Studio · SNIES / datos.gov.co · Data Visualisation

---

### [Abodi ML · Legal-Term Risk Predictor](https://github.com/SEBASBELMOS/abodi_ml)
> *Flags court cases at risk of missing legal deadlines, so lawyers don't.*

End-to-end **MLOps** module for **Abodi**, a real Colombian LegalTech app. An **XGBoost** classifier flags judicial processes at risk of legal-term expiry: the deadlines lawyers can't afford to miss. Trained on **synthetic data** (modelled on Colombian judicial business rules), it reaches **F1 = 0.89 / AUC-ROC = 0.91** and ships with the full stack: **MLflow** tracking + model registry, **FastAPI** serving, **Docker Compose**, **Prometheus + Grafana** monitoring and **GitHub Actions** CI/CD. Designed to plug into Abodi's backend as a future production feature.

**Tech:** Python · XGBoost · scikit-learn · FastAPI · MLflow · Docker · Prometheus · Grafana · GitHub Actions

---

### More projects & contributions
- **[DeutschLernen](https://github.com/SEBASBELMOS/deutschlernen):** Full-stack AI web app for learning German: Express backend, vanilla-JS frontend, LLM-powered chat & correction, AssemblyAI voice input and a Leitner spaced-repetition system.
- **[Sports Data API (Neo4j)](https://github.com/SEBASBELMOS/sports-graph-api):** Node.js REST API on a Neo4j graph database, **+40% query efficiency**.
- **Datathon del Pacífico:** *finalists*, analysing Cali's MIO public-transport data for operational efficiency.
- **JurisIntel (LegalTech, volunteer):** NLP pipelines for legal-document analysis, case-monitoring automation and an AI legal chatbot.
- **[F1 Lap Time Analysis](https://github.com/SEBASBELMOS/F1-Analysis-Project):** Streamlit dashboard on 2023 Monza GP telemetry.

---

## 🧰 Core Stack

**Core Data & Analytics:** Python · Pandas · NumPy · SQL · PostgreSQL · ETL · Apache Airflow · Data Warehousing (Star Schema) · Data Cleaning · Dashboarding · Documentation

**Business Intelligence:** Power BI · Looker Studio · KPI Reporting · Dashboard Design · Data Storytelling

**Hands-on Exposure:** Machine Learning · Statistics · Deep Learning · Geospatial Data · Remote Sensing · React · TypeScript · Node.js · Neo4j · Apache Kafka · Docker

**Backend, Frontend & Deployment:** FastAPI · GCP · AWS · GitHub · Hugging Face Spaces

**AI Orchestration & Automation:** n8n · Claude Code · Cursor · ChatGPT · Prompt Engineering · Multi-agent workflows

---

## 🗣️ Teaching & Communication

I teach Spanish online to international students in English, Spanish and beginner-friendly German. It's made me good at breaking complex ideas into clear steps, adapting to different levels and communicating across cultures: the same skills I bring to documentation, dashboards and client-facing work.

---

## 🧠 Currently Sharpening

- Data modelling, SQL and analytics workflows.
- Production habits: testing, documentation, deployment and maintainability.
- Practical ML/statistics understanding from university and portfolio projects.
- AI orchestration workflows: using multi-agent systems, documentation and human-in-the-loop review to plan, prototype, debug and ship faster.

---

## 🤝 Open to Collaborate On

Data analytics & BI dashboards · ETL and data pipelines · workflow automation · AI orchestration productivity tools · data projects with practical ML/statistics components · geospatial data visualisation · educational content around data, AI and technology.

---

## 🌍 Languages

- **Spanish:** Native
- **English:** C2 (EF SET)
- **German:** A2, currently learning

---

## 📫 Contact

Happy to connect if you're into data, automation, AI tooling, education or collaboration.

**Portfolio:** [sebasbelmos.github.io](https://sebasbelmos.github.io)  
**LinkedIn:** [linkedin.com/in/sebasbelmos](https://www.linkedin.com/in/sebasbelmos/)  
**YouTube:** [YouTube Channel](https://www.youtube.com/channel/UCeYaQhjA-N6YVd6RNTdhBeA)
