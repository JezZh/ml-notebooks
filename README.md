# ML Notebooks

A portfolio of machine learning and computer vision notebooks covering time-series forecasting, classification, image segmentation, and image reconstruction. Each notebook is self-contained and runnable in Google Colab or a local Jupyter environment.

## Notebooks

| Notebook | Task | Techniques | Frameworks |
|---|---|---|---|
| [Air Quality Forecasting](air-quality-forecasting.ipynb) | Multivariate time-series forecasting | Deep learning (LSTM, Sequential), EarlyStopping | TensorFlow / Keras |
| [Energy Consumption Forecasting](energy-consumption-forecasting.ipynb) | Univariate time-series forecasting | LSTM, EDA, anomaly analysis, MinMaxScaler | TensorFlow / Keras |
| [Jellybean Color Segmentation](jellybean-color-segmentation.ipynb) | Color-based image segmentation | RGB / HSV / LAB color spaces, K-Means clustering | OpenCV, scikit-learn |
| [Logistic Regression Evaluation](logistic-regression-model-evaluation.ipynb) | Binary classification | Logistic regression, confusion matrix, precision-recall, ROC-AUC | scikit-learn |
| [Milk Production Forecasting](milk-production-time-series-forecasting.ipynb) | Univariate time-series forecasting | ARIMA, SARIMAX, model stability analysis, MAE / MSE / MAPE | statsmodels |
| [Missing Pixel Reconstruction](missing-pixel-image-reconstruction.ipynb) | Image inpainting | Patch-based dataset, custom CNN | PyTorch |
| [SMS Spam Classification](sms-spam-classification.ipynb) | Text classification | CountVectorizer, TF-IDF, logistic regression, F1 evaluation | scikit-learn |
| [Titanic Survival Prediction](titanic-survival-prediction.ipynb) | Tabular classification | SVC, GridSearchCV, 5-fold cross-validation, pipeline preprocessing | scikit-learn |

## Getting Started

### Run in Google Colab (recommended)

Open any notebook directly in Colab — most notebooks download their datasets automatically at runtime. The air-quality notebook is the exception; see [Data Notes](#data-notes) below.

### Run locally

**Requirements:** Python 3.9+

```bash
git clone https://github.com/jezZh/ml-notebooks-work.git
cd ml-notebooks-work
pip install -r requirements.txt
jupyter notebook
```

**`requirements.txt`**

```
numpy
pandas
matplotlib
seaborn
scikit-learn
statsmodels
tensorflow
torch
torchvision
opencv-python
jupyter
```

## Data Notes

- Most notebooks fetch public datasets directly at runtime (Titanic CSV, SMS Spam Collection zip, milk production CSV).
- **Air Quality Forecasting** expects preprocessed CSV splits (`air_quality_train.csv`, `air_quality_val.csv`, `air_quality_test.csv`) uploaded to `/content/` when running in Colab. These are derived from the [UCI Air Quality dataset](https://archive.ics.uci.edu/dataset/360/air+quality).
- Large datasets and generated model outputs are not committed to this repository.

## License

MIT
