mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns --host 127.0.0.1 --port 8080

.\venv\Scripts\activate

# BTC Price Movement Prediction

Dieses Repository enthält den Code für die Vorhersage der Bitcoin-Preisbewegung unter Verwendung eines hybriden CNN- LSTM-Modells. Das Modell wird mit historischen Preisdaten und technischen Indikatoren trainiert, um die zukünftige Preisbewegung vorherzusagen.

### Projektstruktur

```bash
│
├── src/
│ ├── data/
│     └── BTC-USD.csv
├── main.ipynb
├── .gitignore
├── README.md
└── requirements.txt
```
### Installation

Die verwendete Python-Version ist 3.10.7. Für die Reproduzierbarkeit erstelle eine virtuelle Umgebung und installiere die benötigten Bibliotheken mit den folgenden Befehlen:

```bash
Unter Windows: `python -m venv venv`
source venv/bin/activate
pip install -r requirements.txt
````

### MLflow Lifecycle Management

Das Projekt verwendet MLflow um das Training des Modells mit unterschiedlichen Parameter-Kombinationen aufzuzeichnen. Um Zugriff auf das Dashboard zu erhalten, führe den folgenden Befehl im Terminal aus:

```bash
mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns --host 127.0.0.1 --port 8080
```
Beim Ausführen der main.ipynb wird vor dem Trainingsprozess ein neues Experiment angelegt und die relevanten Metriken geloggt. 

