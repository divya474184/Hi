## Run from terminal:

docker build -t creditcard.azurecr.io/cc:latest .

docker login creditcard.azurecr.io

docker push creditcard.azurecr.io/cc:latest

<div align="center">

# 💳 Credit Card Fraud Detection 🕵️‍♀️

**Credit Card Fraud Detection** is a machine learning project built to identify fraudulent transactions using predictive analytics. It uses multiple ML models, feature engineering, and performance evaluation techniques to ensure reliable fraud prediction. The project is containerized with Docker and ready for cloud deployment via Azure Container Registry.

[Portfolio](https://your-portfolio-link.com) • [GitHub](https://github.com/divyaagarwal7/Credit-Card-Fraud-Detection)

</div>

---

<p align="center">
  <a href="https://github.com/divyaagarwal7/Credit-Card-Fraud-Detection"><img src="https://img.shields.io/github/last-commit/divyaagarwal7/Credit-Card-Fraud-Detection?style=flat-square" alt="last commit"></a>
  <a href="https://github.com/divyaagarwal7/Credit-Card-Fraud-Detection"><img src="https://img.shields.io/github/languages/top/divyaagarwal7/Credit-Card-Fraud-Detection?style=flat-square" alt="languages"></a>
  <a href="https://github.com/divyaagarwal7/Credit-Card-Fraud-Detection/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" alt="license" /></a>
  <img src="https://img.shields.io/badge/version-1.0.0-success?style=flat-square" alt="version" />
</p>

---

## ✨ Summary

This project aims to detect fraudulent credit card transactions using machine learning models such as Logistic Regression, Random Forest, and XGBoost. It demonstrates how data preprocessing, feature scaling, and model evaluation can be used to build a robust fraud detection system. The dataset used is highly imbalanced, and techniques like SMOTE are employed to handle class imbalance effectively.

---

## 📦 Highlights & Use Cases

- Real-world application of machine learning in finance and cybersecurity.  
- Demonstrates data preprocessing, EDA, and model optimization.  
- Suitable for deployment on cloud (Azure, AWS, GCP) using Docker containers.  
- Perfect for portfolios or research demonstrating applied ML workflows.

---

## 🚀 Features

- 📊 Exploratory Data Analysis (EDA) & visualization of transaction patterns  
- ⚙️ Feature engineering & data balancing with SMOTE  
- 🤖 Multiple ML models: Logistic Regression, Random Forest, XGBoost  
- 📈 Model evaluation: accuracy, precision, recall, F1-score, ROC-AUC  
- 🧠 Fraud probability prediction for new transactions  
- 🐳 Containerized deployment with Docker  
- ☁️ Azure Container Registry integration for scalable cloud hosting

---

## 🧩 Tech Stack

**Language:** Python  
**Libraries:** NumPy, Pandas, Scikit-Learn, Matplotlib, Seaborn, XGBoost  
**Environment:** Jupyter Notebook / Python Script  
**Containerization:** Docker  
**Deployment:** Azure Container Registry  
**Version Control:** Git & GitHub

---

## 📁 Project Structure

```
/CreditCard-Fraud-Detection
│
├── data/                      # Dataset files (CSV)
├── notebooks/                 # EDA and training notebooks
├── src/                       # Source code (preprocessing, model, utils)
├── models/                    # Saved trained models (.pkl)
├── Dockerfile                 # Docker configuration
├── requirements.txt           # Python dependencies
├── app.py                     # Flask or Streamlit inference app
├── README.md                  # Project documentation
└── LICENSE                    # License file
```

---

## 🛠️ Quick Start (Local)

1. **Clone the repository**
```bash
git clone https://github.com/divyaagarwal7/Credit-Card-Fraud-Detection.git
cd Credit-Card-Fraud-Detection
```

2. **Create a virtual environment & install dependencies**
```bash
python -m venv venv
source venv/bin/activate  # for macOS/Linux
venv\Scripts\activate     # for Windows
pip install -r requirements.txt
```

3. **Run the application**
```bash
python app.py
```

4. **Access locally**
```
http://localhost:5000
```

---

## 🧪 Model Workflow

1. **Data Preprocessing**  
   - Handle missing values and scaling.  
   - Address class imbalance using SMOTE.  

2. **Model Training**  
   - Train multiple classifiers (Logistic Regression, Random Forest, XGBoost).  
   - Tune hyperparameters using GridSearchCV.  

3. **Evaluation Metrics**  
   - Accuracy, Precision, Recall, F1-Score, ROC-AUC.  

4. **Prediction & Deployment**  
   - Export best model (`model.pkl`).  
   - Deploy as API using Flask or Streamlit.  

---

## 🐳 Docker Deployment

### Build & Push Docker Image
```bash
docker build -t creditcard.azurecr.io/cc:latest .
docker login creditcard.azurecr.io
docker push creditcard.azurecr.io/cc:latest
```

### Run Locally
```bash
docker run -p 5000:5000 creditcard.azurecr.io/cc:latest
```

---

## 📊 Example Output

**Model Comparison:**

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---------------------|----------|------------|---------|-----------|----------|
| Logistic Regression | 0.95     | 0.93       | 0.90    | 0.91      | 0.97     |
| Random Forest       | 0.98     | 0.96       | 0.95    | 0.95      | 0.99     |
| XGBoost             | 0.99     | 0.98       | 0.97    | 0.97      | 0.99     |

---

## ✅ Testing & Quality

- Tested using train/test split and k-fold cross validation.  
- Verified against overfitting using learning curves and ROC plots.  
- Code formatted with Black and PEP8 compliance.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository  
2. Create your branch: `git checkout -b feature/new-feature`  
3. Commit changes: `git commit -m "Added new feature"`  
4. Push and open a Pull Request  

---

## 📄 License

This project is licensed under the **MIT License** — see [LICENSE](LICENSE).

---

## 📬 Contact

**Divya Agarwal** — Developer & Maintainer  
- GitHub: [https://github.com/divyaagarwal7](https://github.com/divyaagarwal7)  
- LinkedIn: [https://linkedin.com/in/divyaagarwal7](https://linkedin.com/in/divyaagarwal7)  
- Email: divyaagarwal@example.com  

---

<div align="center">
Made by <b>Divya Agarwal</b> 💻
</div>
