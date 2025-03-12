# House-Price-Prediction-Model

This project implements a complete **Machine Learning (ML) pipeline** using **ZenML** and MLOps principles to predict house prices based on various features. The model is deployed using **Streamlit**, allowing users to interact with the prediction system through a simple web interface.

## Key Features
- **End-to-End ML Pipeline**: Covers data preprocessing, model training, evaluation, and deployment.
- **ZenML Integration**: Implements modular, reproducible, and scalable ML workflows.
- **Real-time Predictions**: The trained model is deployed using Streamlit for user-friendly interaction.
- **MLOps Practices**: Automated data processing, model tracking, and deployment using ZenML.

## Technology Stack
- **Machine Learning Framework**: Scikit-learn for model training and evaluation.
- **Pipeline Management**: ZenML for managing ML workflows.
- **MLOps Tools**: Docker for containerization, ZenML for model tracking, and Streamlit for UI deployment.
- **Backend Framework**: Streamlit for serving the model.
- **Web Server**: Uvicorn (for API integration, if needed).

## Problem Overview
This project aims to predict house prices based on various attributes, such as:
- **Location**
- **Number of Bedrooms & Bathrooms**
- **Size (Square Feet)**
- **Year Built**
- **Neighborhood & Other Features**

## ML & MLOps Workflow
### 1. Data Processing
- Load and clean the dataset.
- Handle missing values and categorical encoding.
- Feature scaling for better model performance.

### 2. Model Training
- Train multiple models using Scikit-learn.
- Evaluate models using metrics like RMSE, MAE, and R².
- Use ZenML to track experiments and store trained models.

### 3. Prediction Pipeline
- The trained model is integrated into a **Streamlit web app**.
- Users can input house details and get real-time price predictions.

### 4. Deployment & MLOps
- The model and application are packaged using Docker.
- CI/CD pipelines can be integrated to automate deployment.
- The Streamlit app is deployed for interactive use.

## Installation

### Clone the repository:
```bash
git clone https://github.com/yourusername/House-Price-Prediction-ZenML.git
cd House-Price-Prediction-ZenML
```

### Install dependencies:
```bash
pip install -r requirements.txt
```

### Set up ZenML:
```bash
zenml init
zenml stack set <your_stack_name>
```

### Train the model:
```bash
python src/train.py
```

### Run the Streamlit app:
```bash
streamlit run app.py
```

### Alternatively, run it in a Docker container:
```bash
docker build -t house-price-prediction .
docker run -p 8501:8501 house-price-prediction
```

### Access the application at:
[http://localhost:8501](http://localhost:8501)

## Project Structure
```
📂 House-Price-Prediction-Model
│── app.py             # Streamlit app for predictions
│── analysis/          # Exploratory Data Analysis (EDA) scripts
│── config/            # Data validation and pipeline configurations
│── src/
│   ├── components/    # Data ingestion, transformation, validation, and model scripts
│   ├── pipeline/      # ML pipelines using ZenML
│   ├── train.py       # Model training script
│   ├── predict.py     # Prediction script
│── templates/         # HTML templates (if applicable)
│── static/            # Static files for UI
```

## MLOps Features
### Model Training Pipeline
- Uses ZenML for structured and reproducible ML workflows.
- Automates data preprocessing, model training, and evaluation.

### Model Deployment (Streamlit)
- Provides an interactive UI for users to input house details.
- Returns real-time price predictions.

### Dockerization
- The entire application is containerized using Docker.
- Ensures smooth deployment across different environments.

This project follows a structured **ML & MLOps** approach, ensuring scalability, reproducibility, and efficiency in house price prediction. 🚀
