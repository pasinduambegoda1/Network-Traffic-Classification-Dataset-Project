# Network-Traffic-Classification-Dataset-Project

This project focuses on analysing and classifying network traffic using a structured dataset containing flow-level network features. The dataset includes a wide range of statistical attributes extracted from bidirectional network flows, such as packet counts, payload sizes, timings (IAT), header sizes, TCP flag counts, and other behavioural indicators. These features are commonly used in Intrusion Detection Systems (IDS), anomaly detection, and machine-learning-based cyber-security applications.

---

## 📌 Project Overview

The goal of this project is to **train, evaluate, and analyse machine learning models** for network intrusion detection.  
The dataset contains labelled flows, where each entry represents a single communication flow between a source and destination.  
Each flow is described using dozens of numerical and categorical features, and the **target** column indicates whether the flow is *benign* or *malicious*.

This project involves:

- Loading and preprocessing network flow data  
- Exploratory Data Analysis (EDA)  
- Feature scaling and cleaning  
- Training ML models (e.g., Random Forest, XGBoost, Logistic Regression, Neural Networks)  
- Evaluating classification performance  
- Visualising results  

---

## 📂 Dataset Description

Each row in the dataset represents a **single network flow**, containing attributes such as:

### 🔹 Header Information
- `id.orig_p` – Source port  
- `id.resp_p` – Destination port  
- `proto` – Protocol (TCP, UDP, ICMP)  
- `service` – Service type  

### 🔹 Packet Statistics
- `fwd_pkts_tot` – Total forward packets  
- `bwd_pkts_tot` – Total backward packets  
- `fwd_data_pkts_tot` – Forward data packets  
- `bwd_data_pkts_tot` – Backward data packets  
- `fwd_pkts_per_sec`, `bwd_pkts_per_sec` – Packet rate  
- `flow_pkts_per_sec` – Total flow packet rate  

### 🔹 Payload Metrics
- `fwd_pkts_payload.min/max/avg/std`  
- `bwd_pkts_payload.min/max/avg/std`  
- `flow_pkts_payload.min/max/avg/std`  

### 🔹 Byte Throughput
- `payload_bytes_per_second`  
- `fwd_subflow_bytes`, `bwd_subflow_bytes`  

### 🔹 Timing Metrics (IAT)
Inter-Arrival Times:
- `fwd_iat.min/max/tot/avg/std`  
- `bwd_iat.min/max/tot/avg/std`  
- `flow_iat.min/max/tot/avg/std`  

### 🔹 TCP Flag Indicators
- FIN, SYN, RST, PSH, ACK, URG, CWR, ECE flag counts  

### 🔹 Window Sizes
- `fwd_init_window_size`  
- `bwd_init_window_size`  
- `fwd_last_window_size`  

### 🔹 Target Label
- `target` – The class label (e.g., *benign*, *attack type*, etc.)

---

## 🛠 Project Workflow

### 1️⃣ **Data Loading**
Using Python (pandas), the CSV/Parquet dataset is loaded for processing.  
Typical checks include:
- Missing values  
- Data types  
- Statistics per feature  

### 2️⃣ **Preprocessing**
Includes:
- Dropping duplicates  
- Handling missing values  
- Encoding categorical features  
- Scaling numerical features  
- Balancing dataset (SMOTE, undersampling if required)

### 3️⃣ **Exploratory Data Analysis**
You may visualise:
- Correlation matrix  
- Traffic distribution  
- Packet/byte distributions  
- Attack vs normal flow behaviour  

### 4️⃣ **Model Training**
Algorithms commonly used:
- Random Forest  
- XGBoost  
- Gradient Boosting  
- SVM  
- Neural Networks  
- Logistic Regression  

### 5️⃣ **Evaluation**
Metrics:
- Accuracy  
- Precision, Recall, F1 Score  
- Confusion Matrix  
- ROC-AUC  

---

## 📊 Example Use Cases

This dataset is suitable for:

- Intrusion Detection Systems (IDS)  
- Network anomaly detection  
- Behavioural traffic modelling  
- Cyber-security research  
- Feature engineering for flow-based ML models  

---

## 🧪 Example Technologies Used
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib / Seaborn  
- Jupyter Notebook  

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd project-folder
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the Jupyter notebook:
   ```bash
   jupyter notebook
   ```

4. Run the preprocessing, EDA, and ML training steps.

---

## 📁 Repository Structure

```
/project
│── data/
│   └── dataset.csv
│── notebooks/
│   └── analysis.ipynb
│── src/
│   ├── preprocessing.py
│   ├── models.py
│   ├── train.py
│   ├── config.py
│   ├── predict.py
│   ├── requirements.txt
│   └── utils.py
└──  README.md

```

---

## 📌 Summary

This project provides a complete pipeline for analysing, processing, and classifying network traffic using machine learning.  
The dataset contains rich network-flow features ideal for cyber-security research and IDS development.

If you'd like, I can also create:
✅ Jupyter Notebook  
✅ requirements.txt  
✅ Model training script  
✅ Visualisations (plots)  
Just tell me!
