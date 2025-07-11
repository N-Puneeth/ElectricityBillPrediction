**IGNITERS HACKATHONS 2025**
-------------------------

# ⚡ AI & ML Hackathon – Day 11 Resources

This repository contains the dataset and starter notebook for the **Electricity Bill Prediction Challenge** (Day 11 of the AI/ML Hackathon).

Participants are expected to build a machine learning regression model to predict monthly electricity bills based on appliance usage,tariffs, energy provider, and location data.

---

## 📁 Contents

- `electricity_bill_dataset.csv` — Clean dataset with over 45,000 records of electricity usage across cities and companies
- `Electricity_Bill_Starter_Notebook.ipynb` — Starter notebook to help you begin your analysis, preprocessing, model building, and evaluation

---

## 🧪 How to Use

You may choose **either of the following methods** to load the dataset into your notebook:

---

### ✅ Option 1: Load directly from GitHub (Recommended for Google Colab)

```python
import pandas as pd

url = "https://raw.githubusercontent.com/sharad00004/AI-ML-HACKATHON-Datasets/main/electricity_bill_dataset.csv"
df = pd.read_csv(url)
df.head()
```

> 🔹 Best for Google Colab users  
> 🔹 No need to download or upload the file manually  
> 🔹 Just run the code and get started

---

### 💾 Option 2: Download and load manually

1. Click on the file: [`electricity_bill_dataset.csv`](https://github.com/sharad00004/AI-ML-HACKATHON-Datasets/blob/main/electricity_bill_dataset.csv)
2. Click **Download**
3. Place the file in the same folder as your Jupyter notebook
4. Use the following code:

```python
import pandas as pd

df = pd.read_csv("electricity_bill_dataset.csv")
df.head()
```

> 💡 Use this if you are running the notebook locally (e.g., via Anaconda)

---

## 📢 Note

- This repo is part of the **AI/ML Hackathon** and should only be used for educational and competition purposes.
- The dataset is simulated and anonymized.

---

Good luck, and happy modeling! 🚀
