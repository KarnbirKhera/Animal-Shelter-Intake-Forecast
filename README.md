# Animal Shelter Intake Forecasting

## Overview
Predicting daily animal shelter intake to help shelters optimize staffing, resources, and capacity planning. This project uses 9+ months of real shelter data combined with weather patterns to forecast future intake trends.

**Goal:** Experiment with and build a forecasting model to help animal shelters prepare for high-intake periods. Allow shelter staff to easily query model using an NLP/GenAI interface.

## Why This Matters
Animal shelters operate with limited resources. Unexpected intake surges can lead to overcrowding, staff burnout, reduced care quality and potentially more euthinizations. Accurate forecasts allow shelters to:
- Schedule staff proactively
- Prepare intake spaces
- Coordinate with other shelters and foster networks
- Plan resource allocation

## Data Collection
- **Duration:** 03/15/2025 - Present (260+ days of continuous data)
- **Method:** Automated daily web scraping + AccuWeather API
- **Features:** Shelter census, animal demographics, weather conditions, temporal patterns

### Key Learning: Production Monitoring
My Selenium scraper failed silently for 2 months—a critical lesson in building robust data pipelines with proper logging and alerts.

## Data Structure
The `data/raw/` directory contains daily snapshots in the format `animal_data_YYYYMMDD.csv`.

**Columns:**
- `Date`: Collection date (YYYY-MM-DD)
- `NumOfAnimals`: Daily shelter census
- `average_temp`: Temperature (°F) via AccuWeather API
- `Precipitation`: Binary (1 if ≥50% chance of rain)
- `MonthsInCare`: Animal's shelter duration
- `AgeInMonths`: Animal age
- `Season_*`: One-hot encoded seasons
- `DayOfWeek_*`: One-hot encoded weekdays
- `Species_*`: One-hot encoded species (varies by day)

## Project Status
- [x] Data collection pipeline (9+ months)
- [x] Raw data repository
- [ ] Data consolidation and cleaning
- [ ] Exploratory data analysis
- [ ] Baseline models (ARIMA, SARIMA, Prophet)
- [ ] Advanced forecasting (XGBoost and neural methods such as TimeGPT, TFT and LTSM)



## Tech Stack I intend to learn/use in this project
**ML & Modeling**
- [X] NumPy (Data Manipulation)
- [X] Pandas (Data Manipulation
- [X] Scikit-Learn (ML Library)
- [ ] PyTorch (Deep Learning)
- [ ] Prophet & SARIMA (Seasonal Time Series models)
- [ ] Neural network based models (TimeGPT, TFT and LSTM)
- [ ] MLFLow (Experiment tracking)
- [ ] SHAP (Model explainability)

**Data Collection & Engineering**
- [X] Selenium, Playwright (Web Scraping)
- [X] AccuWeather API (Weather API)
- [ ] PostgreSQL (Database)

**Backend**
- [X] Django (used in past projects, can use if needed)
- [ ] FastAPI
- [ ] Redis (If sever side caching is needed, will look into if needed)

**Frontend**
- [X] React (used in past projects, can use if needed)
- [X] Matplotlib
- [ ] Streamlit (Dashboard for model)


**LLM Integration**
- [ ] LangChain + OpenAI (Allows for simple NLP query model predictions)
- [ ] LangSmith (Monitor/Debug LLM calls)

**DevOps & Infrastructure**
- [X] Docker
- [X] AWS
- [ ] PyTest
- [ ] GitHub Actions
- [ ] Evidently AI/AWS Model Monitor

**Misc**
- [ ] Kubernetes (mainly to learn how to use for industry practice, not necessarily required for this project due to cost restraint and project size)
- [ ] Databricks (mainly to learn how to use for industry practice, not necessarily required for this project due to cost restraint and project size)




## Development Timeline ##

**Phase 1: Data Collection March - Dec 2025**
- [X] Built automated scraping pipeline with Selenium (March 2025)
- [X] Integrated AccuWeather API for weather features (March 2025)
- [X] Collected 200+ days of continuous shelter data stored in S3 (as of Decemeber 2025)
- [X] Learned Playwright, Pandas, NumPy and Scikit-learn (December 2025)
- [ ] Rebuilt data scraping pipeline using Playwright, PyTest and GitHub Actions for robust data collection

**Phase 2: Model Development (Winter 2026)**
- [X] Sklearn pipelines, L1/L2 Regularization, Standardization/Normalization, Boosting/Bagging, Confusion Matrix, Cross-validation, Linear Regression, Decision Trees, Random Forest, K-means (December 2025 coursework)
- [x] Learning Deep Learning/Pytorch through Winter 2026 coursework
- [ ] Experiment with baseline models (SARIMA, Prophet)
- [ ] Experiment with XGBoost and neural network forecasting (LSTM, TimeGPT, TFT)
- [ ] Document experimentation using MLFlow
- [ ] SHAP for understanding feature importance & model interpetability

**Phase 3: Deployment & Integration (Spring 2026)**
- [ ] FastAPI for model endpoints
- [ ] PostgreSQL for data storage
- [ ] Streamlit dashboard for animal shelter staff
- [ ] Unit testing with PyTest
- [ ] CI/CD with GitHub Actions

**Phase 4 LLM Interface (Summer 2026)**
- [ ] LangChain + OpenAI integration (Simple NLP query model predictions)
- [ ] LangSmith (Monitor LLM calls)
- [ ] Natural language query interface
- [ ] Guardrails AI (LLM output validation)

  **Optional LLM Integration for Complex Histoical Queries**
  - [ ] Vector Database for RAG
  - [ ] OpenAI Embeddings
  - [ ] Historical Data Indexing 

**Phase 5: Production (Fall 2026)**
- [ ] Production deployment to AWS
- [ ] Production monitoring and alerts
- [ ] Evidently AI/AWS Model Monitor (Model drift detection)
- [ ] Reading, understanding and applying research paper techniques to improve model accuracy
      






*Motivated by firsthand experience volunteering with shelter animals*
