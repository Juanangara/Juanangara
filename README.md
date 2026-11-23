### Hey! I'm Juan Sebastian

I'm a Computer Scientist, a 2026 graduate of Universidad Nacional de Colombia. I like building software that works for real: clear to understand, easy to change and reliable when many people use it.

In my graduation internship I built a platform that gathers restricted lists of people and companies from 245 public sources in different countries. It runs every day on Azure, handles more than 7 million records and replaced an external provider.

---

### Projects

- **[xm-demand-forecast](https://github.com/Juanangara/xm-demand-forecast)**: day-ahead hourly forecast of Colombia's electricity demand, built on 26 years of data from the grid operator (XM). It is validated walk-forward with no information leakage (1.64 % error against 3.37 % for "same hour last week" and 2.25 % for a classical MSTL model, with significance tests), has prediction intervals whose calibration I measured (my first method turned out overconfident), a FastAPI service in Docker, drift monitors tested by injecting failures, and CI. A development log records what did not work.
- **[newsroom-agents](https://github.com/Juanangara/newsroom-agents)**: a team of agents (researcher, summarizer, fact-verifier, editor) that writes news reports where every claim carries a verbatim quote from its source. Runs open models on a free GPU; evaluated against hand-labelled data, with a development log of what worked and what did not (including a judge model that did not help).
- **[rama-queue](https://github.com/Juanangara/rama-queue)**: large-scale search over Colombia's court-case API with RabbitMQ, PostgreSQL and Redis, with a live dashboard.
- **[norma-rag](https://github.com/Juanangara/norma-rag)**: a local RAG over Colombian data-protection law, with hallucination measurement for a small model.
-   **[tokenscope](https://github.com/Juanangara/tokenscope)**: a low-latency LLM inference service with overload protection, observability and prompt drift detection. It runs on a laptop CPU with one `docker compose` command.
-   **[geotrack](https://github.com/Juanangara/geotrack)**: live location tracking with PostGIS: geospatial events, proximity queries and a live map.
-   **[kaggle-competitions](https://github.com/Juanangara/kaggle-competitions)**: Kaggle solutions built around honest validation, each with a write-up of what did and did not help.
    -   **[Titanic](https://github.com/Juanangara/kaggle-competitions/tree/main/titanic)**: machine learning model that predicts which Titanic passengers survived (tabular classification). It uses gradient boosting with engineered features (titles, family size, deck) and imputation computed only on the training data. Cross-validation said 0.846 and the public score was 0.77990. A second version with extra features scored worse (0.76315), which is within the noise of a 418-row test set, so I kept the first and did not tune against the leaderboard.
    -   **[LLM Classification Finetuning](https://github.com/Juanangara/kaggle-competitions/tree/main/llm-classification)**: language-model classifier that predicts which of two chatbot answers a user prefers, trained on Chatbot Arena data. I compared hand-made text features, sentence embeddings with LightGBM (1.00436 public log loss) and a LoRA fine-tune of Qwen2.5-1.5B, and wrote down what did and did not help.
    -   **[Predicting Soil Grain Size Distributions from Images](https://github.com/Juanangara/kaggle-competitions/tree/main/Geotechnical-Resilience-Project)**: computer vision pipeline that predicts a soil sample's grain-size distribution (the curve a laboratory takes days to measure) from a few photographs. It combines multi-scale texture features with a physical bound measured by segmenting particles with SAM. Validation holds out whole groups of near-identical samples: error drops from 102 for the mean curve to about 46, and the public score is 50.67 (lower is better). DINOv2 embeddings and a coverage calibration were tested and discarded.

---

### Technologies I work with

-   **Languages:** TypeScript, Python, JavaScript, SQL
-   **Data and ML:** scikit-learn, LightGBM, PyTorch, Hugging Face (LoRA fine-tuning, 4-bit inference), sentence-transformers, llama.cpp, pandas, Pydantic, MLflow, statsforecast
-   **Backend:** FastAPI, Django, REST APIs
-   **Databases and messaging:** PostgreSQL (PostGIS, pgvector), MySQL, Redis, RabbitMQ
-   **Infrastructure and testing:** Docker, Azure, GitHub Actions, Prometheus, Grafana, pytest

---

### Contact

-   **Email:** sebasangarit@gmail.com
-   **LinkedIn:** [juan-sebastian-villarreal-angarita](https://www.linkedin.com/in/juan-sebastian-villarreal-angarita-10498b232/)
