<div align="center">

## 💳 Credit Card Fraud Detection — Streamlit + scikit‑learn

Detect potentially fraudulent credit card transactions using a trained Logistic Regression model, wrapped in a friendly Streamlit UI. The project includes data processing, model training, an interactive prediction app, Dockerization, and CI/CD examples.

[Run the App](#-quick-start-local) • [Model Training](#-model-training) • [Docker](#-docker) • [CI/CD](#-cicd)

</div>

---

### ✨ Summary

This project demonstrates an end‑to‑end ML workflow for tabular fraud detection: data preparation and balancing, model training and evaluation, artifact export, and a production‑ready Streamlit interface for real‑time predictions.

---

### 🚀 Features

- Interactive Streamlit app with 9 user inputs and instant prediction
- Logistic Regression classifier trained on the credit card dataset
- Class balancing via undersampling + train/test split
- Exported model (`models/logistic_regression_model.pkl`) and report artifacts
- Dockerized image for portable deployment (works locally or on ACR)
- Example GitHub Actions workflows for training and deployment

---

### 🧩 Tech Stack

- **App/UI**: Streamlit
- **ML**: scikit‑learn, pandas, numpy, seaborn, matplotlib
- **Sampling**: imbalanced‑learn
- **Packaging/Runtime**: Python 3.11, Docker
- **CI/CD**: GitHub Actions (examples in `.github/workflows/`)

---

### 📁 Project Structure (high level)

```
.
├─ app.py                         # Streamlit app
├─ data/
│  ├─ raw_data/creditcard.csv     # Original dataset (not committed)
│  └─ processed/processed_data.csv
├─ models/
│  └─ logistic_regression_model.pkl
├─ artifacts/
│  ├─ classification_report.jpeg
│  └─ heatmap.jpeg
├─ src/
│  ├─ data_prep.py                # undersampling + heatmap
│  ├─ model.py                    # train/test split + training + saving
│  ├─ load_data.py                # helper to load data (if used)
│  └─ feat_eng.py                 # placeholder for future features
├─ notebooks/
│  └─ credit-card-fraud-detection.ipynb
├─ Dockerfile
├─ requirements.txt
└─ setup.py
```

---

### 🛠️ Quick Start (Local)

1) Create and activate a virtual environment, then install deps:

```bash
python -m venv .venv
.venv\\Scripts\\activate  # Windows
pip install -r requirements.txt
```

2) Train the model (expects `data/raw_data/creditcard.csv`):

```bash
python src/data_prep.py   # creates processed CSV + heatmap artifact
python src/model.py       # trains + saves model + report artifact
```

3) Run the Streamlit app:

```bash
streamlit run app.py
```

Open `http://localhost:8501`.

---

### 📊 Using the App

- Provide the 9 inputs shown in the UI (Amount, Transaction Time, Location Score, Merchant Type, Card Usage, Risk Factor, Account Age, Spending Pattern, Alert Count).
- Click Predict Transaction to get Fraud / Not Fraud.
- The app auto‑aligns inputs to the model’s expected feature size to avoid shape errors.

---

### 🧪 Model Training

Key steps implemented in `src/`:

- `data_prep.py`
  - Loads dataset, applies RandomUnderSampler, saves processed CSV, and correlation heatmap.
- `model.py`
  - Splits data, trains Logistic Regression, evaluates, saves model and a classification report image.

Artifacts are written to `models/` and `artifacts/`.

---

### 🐳 Docker

Build and run locally:

```bash
docker build -t fraud-app:latest .
docker run --rm -p 8501:8501 fraud-app:latest
```

Push to Azure Container Registry (ACR) example:

```bash
docker login <your-registry>.azurecr.io
docker tag fraud-app:latest <your-registry>.azurecr.io/cc:latest
docker push <your-registry>.azurecr.io/cc:latest
```

---

### 🔄 CI/CD

Example GitHub Actions workflows live in `.github/workflows/`:

- `train-deploy.yml` — run training and publish artifacts/images
- `main_creditcard.yml` — example for build/test/deploy pipeline

Edit these to match your registry, secrets, and environment.

---

### 🖼️ Screenshots

Add images to `artifacts/` or `public/` and reference here, e.g.:

```html
<img src="artifacts/classification_report.jpeg" alt="Classification Report" width="700" />
```

---

### 🧰 Requirements

See `requirements.txt`. Recommended Python ≥ 3.11.

---

### 🤝 Contributing

PRs are welcome! Please keep changes focused and include a short description and, when relevant, screenshots of UI changes.

---

### 📄 License

This project is released under the MIT License. See `LICENSE` if present.

---

### 📬 Contact

Maintainer: Your Name

- GitHub: https://github.com/your‑github
- LinkedIn: https://www.linkedin.com/in/your‑profile
- Email: you@example.com

If you want me to personalize the links, send me your details and I’ll update this file.

