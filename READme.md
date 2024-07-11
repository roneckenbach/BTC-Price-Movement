# BTC Price Movement Prediction

This repository contains the code for predicting Bitcoin price movements using a hybrid CNN-LSTM model. The model is trained with historical price data and technical indicators to forecast future price movements.

### Project structure

```bash
│
├── src/
│ ├── data/
│     └── BTC-USD.csv
├── .gitignore
├── main.ipynb
├── README.md
└── requirements.txt
```
### Installation
Use Python version 3.10.7 for this project. For reproducibility, create a virtual environment.
```bash
python -m venv venv
.\venv\Scripts\activate
```
 For further instructions, visit: https://docs.python.org/3/library/venv.html.<br>
Once the virtual environment created and active, install the required libraries using the following command:

```bash
pip install -r requirements.txt
````
If the installation using the requirements.txt file does not work, use this command:
```bash
pip install pandas numpy seaborn matplotlib scikit-learn tensorflow mlflow ta

```


### MLflow Lifecycle Management

The project uses MLflow to record the training of the model with different parameter combinations. To access the dashboard, run the following command in the terminal:

```bash
mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns --host 127.0.0.1 --port 8080
```
When running the main.ipynb, a new experiment is created before the training process. The code contains the code for logging all relevant metrics for each run.


