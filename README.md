# 🧠 Log Analysis & Detection System

This project focuses on detecting and analyzing web-based attacks through log data using both **AI-driven** and **rule-based** approaches.  
The system identifies potential threats such as **NoSQL Injection**, **Open Redirect**, and other anomalies by processing flow logs and raw HTTP requests.

## 🚀 Features
- Hybrid model combining **Rule-Based Filtering** and **AI Similarity Models**  
- Attack detection using **Sentence Transformers**, **CrossEncoder**, and **FAISS**  
- Real-time log classification into `benign` or `malicious` categories  
- Scalable for integration with live web monitoring systems  

## 🧩 Tech Stack
- **Python**, **Pandas**, **NumPy**
- **SentenceTransformers**, **FAISS**, **Scikit-learn**
- **JSON / Flow log processing**
- **Joblib** for model storage and loading

## ⚙️ Workflow
1. Parse and preprocess raw log or flow data  
2. Apply rule-based checks for known patterns  
3. Compute similarity scores using transformer models  
4. Combine both results for final classification

## 📊 Example Output
| Log | Predicted Label | Similarity Score | Decision Reason |
|-----|------------------|------------------|-----------------|
| `/index.html` | Benign | 0.23 | sim_score < 1.0 → benign |
| `/login?next=https://evil.com` | Open Redirect | 7.45 | rule matched |
| `{ "$ne": "" }` | NoSQL Injection | 7.76 | ru


Flow analysis -- Logs - zeek - flow logs - Model
