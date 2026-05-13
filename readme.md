🌞 Energy Forecasting using ML & Deep Learning
📌 Overview

This project focuses on time-series forecasting of solar power generation (GC) using both:

Traditional Machine Learning models
Deep Learning models

The goal is to compare performance and efficiency of different approaches and understand:

❓ Do deep learning models always outperform classical ML methods?

🚀 Key Highlights
📊 Dataset size: ~7 million rows
⚡ Models implemented:
Random Forest
XGBoost
LSTM (Deep Learning)
🧠 Feature engineering:
Lag features (short-term & long-term)
Rolling statistics
Time-based features
🔥 GPU acceleration for deep learning
🏗️ Project Structure
📂 Minor Project
│
├── 📁 processed_data/
│   └── final_dataset.csv
│
├── 📁 models/
│   ├── random_forest.pkl
│   ├── xgboost.pkl
│   └── lstm.pt
│
├── 📁 results/
│   ├── rf_feature_importance.png
│   └── evaluation_metrics.csv
│
├── 01_preprocessing.ipynb
├── 02_models_comparison.ipynb
└── README.md
⚙️ Installation
🔹 Requirements
pip install pandas numpy scikit-learn xgboost torch matplotlib
📊 Feature Engineering

Key features used:

⏱️ Time features:
hour, day, month, weekend, season
🔁 Lag features:
GC_lag_1, GC_lag_48, GC_lag_336
📉 Rolling features:
3-day and 7-day averages
⚡ System feature:
generator capacity
🤖 Models Implemented
1️⃣ Random Forest
Baseline model
Fast but limited for time-series
2️⃣ XGBoost 🔥 (Best Performer)
Gradient boosting model
Handles non-linearity efficiently
GPU-compatible
3️⃣ LSTM (Deep Learning)
Sequence-based model
Captures temporal dependencies
Requires more computation
📈 Results
Model	RMSE	MAE	R²
Random Forest	0.26	0.14	0.50
XGBoost	🔥 0.03	0.007	0.99
LSTM	~0.5–0.8	—	—
🧠 Key Insights
XGBoost significantly outperforms LSTM
Feature engineering transforms time-series into tabular problem
Deep learning is not always superior

✅ Tree-based models are highly effective for structured time-series data

⚡ Performance
Model	Training Time
Random Forest	Moderate
XGBoost	⚡ Fast
LSTM	🐢 Slow (GPU required)
🖥️ GPU Usage
GPU used for LSTM training
Achieved 10–30× speedup after CUDA setup
🔮 Future Work
Hybrid models (XGBoost + LSTM)
Transformer-based forecasting
Weather data integration
Multi-step forecasting
📚 Research Contribution

This project demonstrates:

🔥 Tree-based models can outperform deep learning for structured time-series forecasting.

👨‍💻 Author

Anmol Rajpoot
B.Tech CSE, IIIT Bhopal

⭐ Acknowledgements
Scikit-learn
XGBoost
PyTorch
📌 How to Run
Run preprocessing:
01_preprocessing.ipynb
Train & compare models:
02_models_comparison.ipynb
🚀 Final Note

This project bridges machine learning, deep learning, and time-series analysis, providing practical insights into model selection for real-world datasets.