# BTC Price Movement Prediction

This repository contains the code for predicting Bitcoin price movements using a hybrid CNN-LSTM model. The model is trained with historical price data and technical indicators to forecast future price movements.

### Project structure

```bash
│
├── data/
│     └── BTC-USD.csv
├── .gitignore
├── main.ipynb
├── README.md
└── requirements.txt
```
### Installation
Use Python version 3.10.7 for this project. For reproducibility, create and activate a virtual environment using the following commands:
```bash
python -m venv venv
.\venv\Scripts\activate
```
For further instructions, visit: https://docs.python.org/3/library/venv.html.<br>
Once the virtual environment is created and active, install the required libraries using the following command:

```bash
pip install -r requirements.txt
````

### MLflow Lifecycle Management

The project uses MLflow to record the training of the model with different parameter combinations. To create a default experiment and access the dashboard, run the following command in the terminal:

```bash
mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns --host 127.0.0.1 --port 8080
```
The dashboard can be opened by following the link in the terminal or via the local host in the browser.
When running the main.ipynb, a new experiment is created before the training process starts. The code contains the code for logging all relevant metrics for each run.