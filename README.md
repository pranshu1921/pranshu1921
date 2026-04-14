# Hi, I'm Pranshu Kumar Premi

I build production-grade ML and GenAI systems across AWS and Azure, focused on shipping reliable models that solve real business problems.

My work spans LLM-based systems, classical ML, data pipelines, and MLOps, with experience delivering across energy, telecommunications, and technology sectors.

**Target roles**: Data Scientist, ML Engineer, AI Engineer
**Location**: Raleigh, NC | Open to Remote and Hybrid
**Status**: Actively seeking new opportunities

---

## Credentials

- Master's in Data Analytics, Northeastern University
- 3.5+ years building production ML systems across consulting and product teams
- Deployed 9 production ML pipelines on AWS SageMaker
- Azure Data Scientist Associate
- HashiCorp Certified: Terraform Associate
- IBM Data Science Professional Certificate
- Google Data Analytics Professional Certificate

---

## Featured Projects

These repositories reflect how I design and ship real-world AI systems, not notebook demos.

---

### Agentic SQL Co-pilot

A self-correcting Text-to-SQL agent that converts natural language business questions into executable SQL, runs them against a real 9-table relational database, and automatically retries with error context when queries fail.

**Live demo**: https://huggingface.co/spaces/pranshu2230/sql-copilot

- Qwen2.5-Coder-7B via HF Inference API for SQL generation
- DuckDB in-process query engine with zero infrastructure overhead
- SQLGlot AST transformation for deterministic alias stripping and column fixing
- Self-correction loop: reads its own SQL errors and rewrites the query up to 3 times
- Data-agnostic: drop any CSV files in and the app queries them with no code changes
- Deployed via GitHub Actions to Hugging Face Spaces

Why this matters: demonstrates how to build reliable LLM-powered systems that handle failure explicitly rather than relying on happy-path-only generation.

View repository: https://github.com/pranshu1921/sql-copilot

---

### ShopAssist RAG: AI-Powered E-Commerce Assistant

Production RAG system for customer support over 150K+ product, review, and policy documents.

- LangChain-based retrieval with vector search and source-grounded answers
- Sub-10ms cached responses, cold queries under 1.5 seconds
- 85%+ retrieval accuracy on domain-specific test queries, 60-80% cache hit rate
- Evaluation harness with 15+ domain-specific test queries
- Dockerized FastAPI backend with Streamlit UI
- API cost of approximately $0.50 per 1,000 queries

Why this matters: demonstrates how to build cost-aware RAG systems that remain debuggable and transparent in production.

View repository: https://github.com/pranshu1921/shopassist-rag

---

### Fraud Detection System: XGBoost + Autoencoder Ensemble

Two-stage e-commerce fraud detection system on 590K IEEE-CIS transactions. Combines supervised and unsupervised ML to catch both known fraud patterns and novel attacks no labeled data exists for yet.

- PyTorch Autoencoder trained exclusively on legitimate transactions. Learns normal behavior unsupervised. Flags novel fraud via reconstruction error before any labeled examples of that pattern exist.
- XGBoost classifier with temporal cross-validation (not random split, which causes data leakage on fraud data), scale_pos_weight for 3.5% class imbalance, and SHAP explainability per flagged transaction.
- Logistic meta-learner ensemble combines both scores. ROC-AUC 0.91 on held-out test set.
- Great Expectations data validation, MLflow experiment tracking, Evidently AI drift monitoring, FastAPI inference endpoint, Streamlit analyst dashboard.

Why this matters: mirrors the two-stage architecture used by production fraud teams at payments companies. Demonstrates that anomaly detection and classification solve different parts of the same problem and should be combined.

View repository: https://github.com/pranshu1921/fraud-detection-xgboost-autoencoder

---

### Agentic RAG Document Search Platform

Production-style RAG system using agentic reasoning over custom knowledge bases.

- LangGraph orchestration for multi-step reasoning and tool selection
- FAISS vector store for efficient semantic search
- ReAct-style agent with deterministic source citation and Wikipedia fallback
- Modular ingestion for URLs and local documents (PDF, TXT, DOCX)
- Includes real screenshots from working system runs

Why this matters: mirrors how modern AI teams build trustworthy internal knowledge systems that can be inspected, debugged, and extended.

View repository: https://github.com/pranshu1921/Agentic-RAG-Document-Search-System

---

### Machine Learning Production Pipeline

End-to-end ML system emphasizing reproducibility, maintainability, and production correctness.

- Data ingestion, feature engineering, training, evaluation, and inference in one pipeline
- sklearn ColumnTransformer pipelines eliminate train-serve skew
- Churn classification model: 0.81 AUC on held-out test set
- FastAPI inference service with health check and prediction endpoints
- Config-driven execution via YAML, artifacts persisted to predictable locations
- CI-ready with GitHub Actions linting and smoke tests

Why this matters: shows how to take a model from notebook to production in a way teams can operate, extend, and trust.

View repository: https://github.com/pranshu1921/ml-production-pipeline

---

### Applied ML Case Studies: Churn and Fraud Detection

Business-first ML case studies that show how predictions become decisions.

- Churn modeling with cost-benefit thresholding: precision 0.74, recall 0.71 at selected operating point
- Fraud detection under class imbalance: threshold selected by expected dollar impact, preventing an estimated $18,400 in fraud loss per 10,000 transactions at a review cost of $620
- Precision-recall optimization prioritized over accuracy for imbalanced fraud data
- End-to-end pipelines producing reports, metrics, plots, and model artifacts from a single command

Why this matters: demonstrates how to translate ambiguous business problems into ML systems that drive real decisions, not just maximize a metric.

View repository: https://github.com/pranshu1921/applied-ml-case-studies

---

## What I Work On

**Generative AI and LLM Systems**
Building production RAG and agentic workflows with emphasis on evaluation, reliability, and source-grounded answers.

**Applied Machine Learning**
Designing predictive models and experiments that solve concrete business problems, from churn and fraud to operational forecasting.

**Production ML Systems**
Taking models from notebook to production through deployment, monitoring, CI/CD, and performance tuning.

**Data Engineering for ML**
Designing SQL-first pipelines, feature stores, and data quality checks that make ML systems reliable at scale.

---

## Tech Stack

**ML and AI**
Scikit-learn, XGBoost, LightGBM, PyTorch, LangChain, LangGraph, OpenAI API, Qwen, FAISS, ChromaDB, RAGAS

**Data and Analytics**
Python, SQL, R, Pandas, NumPy, Polars, Great Expectations

**MLOps and Infrastructure**
AWS (SageMaker, Glue, Lambda, S3, Athena), Azure (OpenAI, AI Search, DevOps), Apache Airflow, Terraform, Docker, GitHub Actions

**Visualization and BI**
Tableau, Power BI, Streamlit, Plotly, Matplotlib, Seaborn

---

## How I Think About AI

- Start with problem framing, not models
- Treat data pipelines as first-class systems
- Fix model errors deterministically in post-processing rather than hoping for better prompts
- Optimize for maintainability over cleverness
- Measure success using business impact
- Plan explicitly for failure modes

---

## Currently Exploring

- Advanced RAG architectures: hybrid search, reranking, query decomposition
- LLM evaluation frameworks: RAGAS, domain-specific metrics
- Fine-tuning and adapting open-source models
- Production monitoring for LLM systems: cost, latency, hallucination detection

---

## Let's Connect

**Seeking**: Data Scientist, ML Engineer, and AI Engineer roles (Remote or Hybrid)

- LinkedIn: https://www.linkedin.com/in/pranshu-kumar
- GitHub: https://github.com/pranshu1921
- Email: pranshukumarpremi@gmail.com
