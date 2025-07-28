# 📊 Stock Prediction Portal

An interactive web application for stock price prediction using LSTM deep learning models. The project is built with a Django REST API backend and a React (Vite) frontend, enabling users to enter stock tickers and visualize predicted price trends.

> ⚠️ This project is developed for **educational purposes**, inspired by a course taught by [Rathan Kumar on Udemy](https://www.udemy.com/). The implementation, structure, and features are customized and extended based on personal learning and experimentation.

---

## 🚀 Features

- 📉 Fetch historical stock data using `yfinance`
- 🧮 Compute technical indicators (like moving averages)
- 🧠 Train an LSTM model on time series stock data
- 📈 Predict and visualize future stock prices
- 🌐 RESTful API built with Django REST Framework
- ⚛️ React (with Vite) frontend for interactive UI
- 📊 Charting actual vs predicted values

---

## 🧰 Tech Stack

| Layer        | Tech                     |
|--------------|--------------------------|
| **Frontend** | React + Vite, Axios, Tailwind CSS |
| **Backend**  | Django, Django REST Framework |
| **ML Model** | LSTM using Keras/TensorFlow |
| **Data**     | yfinance, Pandas, NumPy, Scikit-learn |
| **Charts**   | Matplotlib or Plotly |

---

## 📁 Project Structure

```
stock-prediction-portal/
├── backend-drf/           # Django REST API
│   ├── ml_model/          # LSTM model logic
│   └── ...
├── react-frontend/        # React (Vite) frontend
│   ├── src/
│   └── index.html
├── notebooks/             # (Optional) Jupyter exploration
└── README.md
```

---

## ⚙️ Installation & Setup

### 🐍 Backend – Django API

```bash
cd backend-drf
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

Server will start at `http://localhost:8000`

---

### ⚛️ Frontend – React (Vite)

```bash
cd react-frontend
npm install
npm run dev
```

Frontend will run on `http://localhost:5173` and should connect to the Django API at port `8000`.

---

## 🧠 LSTM Model Overview

```text
Input Sequence (100 days) →
  LSTM Layer (128 units) →
  LSTM Layer (64 units) →
  Dense Layer (25 neurons) →
  Dense Layer (1 neuron)
```

- **Loss Function**: Mean Squared Error (MSE)  
- **Optimizer**: Adam  
- **Training**: Typical setup with 50 epochs (can be tuned)

---

## 📈 Sample Outputs

- Prediction charts comparing actual vs predicted prices
- Evaluation metrics like MSE, RMSE, R²
- Time series plots for stock movement

---

## 📌 Disclaimer

This project is intended **purely for learning and experimentation**. It **should not** be used for financial advice or real-world investment decisions. Stock prediction is highly uncertain and influenced by countless factors beyond historical data.

---

## 👨‍🏫 Acknowledgements

This project was heavily inspired by the [Stock Prediction Web App](https://www.udemy.com/) tutorial by **Rathan Kumar** on Udemy. The code has been adapted, extended, and customized for personal learning purposes.

---

## ✨ Possible Future Improvements

- Add sentiment analysis from financial news
- Integrate real-time data streaming
- Deploy via Docker + CI/CD
- Save trained models and re-load them via API
