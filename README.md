# End-to-End Chicken Disease Classification

This project uses deep learning to classify chicken fecal images as either healthy or infected with Coccidiosis. It leverages TensorFlow/Keras for model training and prediction, and is structured for reproducibility and scalability.

## Features

- Data ingestion and preprocessing pipeline
- Transfer learning with a base CNN model
- Training, evaluation, and prediction scripts
- Experiment tracking with DVC
- Modular codebase for easy extension

## Project Structure

```
├── app.py
├── main.py
├── requirements.txt
├── setup.py
├── params.yaml
├── config/
│   └── config.yaml
├── artifacts/
│   └── data_ingestion/
│       └── Chicken-fecal-images/
├── src/
│   └── CNNclassifier/
│       ├── components/
│       ├── config/
│       ├── constants/
│       ├── entity/
│       ├── pipeline/
│       └── utils/
├── research/
│   └── *.ipynb
└── templates/
    └── index.html
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Likithsatya192/Chicken-Disease-Classification
cd Chicken-Disease-Classification
```

### 2. Install dependencies

It is recommended to use a virtual environment.

```bash
pip install -r requirements.txt
```

### 3. Prepare Data

Place your dataset in the `artifacts/data_ingestion/Chicken-fecal-images/` directory, organized by class folders (e.g., `Coccidiosis/`, `Healthy/`).

### 4. Run Training

```bash
python main.py
```

### 5. Run Prediction

You can use the prediction pipeline in `src/CNNclassifier/pipeline/predict.py` or integrate with `app.py` for a web interface.

## Configuration

- Edit `params.yaml` and `config/config.yaml` to adjust hyperparameters and paths.

## Notebooks

Exploratory and development notebooks are in the `research/` directory.

## Logging

Logs are saved in `logs/running_logs.log`.

## License

This project is licensed under the MIT License.