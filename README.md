---

# Algerian Forest Fire Prediction with AWS Deployment

This project utilizes the **Algerian Forest Fire Dataset** to predict the **Fire Weather Index (FWI)**, an essential indicator for assessing wildfire risk. The application employs machine learning techniques and is deployed on **AWS Elastic Beanstalk** for scalability and accessibility.

---

## Features

- **Machine Learning Model**: Ridge Regression trained to predict FWI based on environmental factors.
- **Flask Web Application**: A user-friendly interface for entering data and viewing predictions.
- **AWS Elastic Beanstalk Deployment**: A scalable and cloud-based solution.
- **Comprehensive Preprocessing**: Data normalization using StandardScaler for improved model accuracy.
- **Data Exploration & Feature Engineering**: Detailed insights into the dataset to optimize predictive performance.

---

## Installation

1. **Clone the Repository**:
   ```bash
   https://github.com/bhanuteja-tech/ML-Lifecycle-project-1.git
   cd ML-Lifecycle-project-1
   ```

2. **Set Up Virtual Environment and Dependencies**:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Prepare the Model**:
   Ensure the trained Ridge Regression model (`ridge.pkl`) and the StandardScaler (`scaler.pkl`) are saved in the `models/` directory.

4. **Run the Flask Application**:
   ```bash
   python application.py
   ```
   Visit `http://127.0.0.1:7000` in your browser.

---

## Deployment on AWS Elastic Beanstalk

1. **Install AWS CLI and Configure Credentials**:
   ```bash
   aws configure
   ```

2. **Initialize Elastic Beanstalk**:
   ```bash
   eb init
   ```

3. **Create and Deploy Environment**:
   ```bash
   eb create forest-fire-env
   eb deploy
   ```

4. **Access Application**: Open the AWS-provided URL in your browser.

---

## Dataset

The **Algerian Forest Fire Dataset** includes key environmental features such as:

- **Temperature** (°C)
- **Relative Humidity (RH)** (%)
- **Wind Speed (Ws)** (km/h)
- **Rainfall** (mm)
- Fire Weather Index Factors:
  - **FFMC** (Fine Fuel Moisture Code)
  - **DMC** (Duff Moisture Code)
  - **ISI** (Initial Spread Index)
- **Region** and **Class Labels** for grouping.

---

## Application Workflow

1. **Input Environmental Parameters**: Users provide the input features through a web form.
2. **Data Preprocessing**: Inputs are scaled using a pre-trained StandardScaler.
3. **FWI Prediction**: The Ridge Regression model predicts the Fire Weather Index.
4. **Results Display**: The predicted FWI value is shown on the web interface.

---

## Folder Structure

```plaintext
.
├── Feature engineering, EDA.ipynb  # Notebook for data exploration and preprocessing
├── Model Training.ipynb           # Notebook for training the Ridge Regression model
├── application.py                 # Flask application code
├── models/                        # Directory for trained model and scaler
│   ├── ridge.pkl
│   └── scaler.pkl
├── templates/                     # HTML templates for the web application
│   ├── index.html
│   └── home.html
├── requirements.txt               # Python dependencies
```

---

## Key Technologies

- **Python**: For building the application and training the model.
- **Flask**: For the web framework.
- **Scikit-Learn**: Used for preprocessing and training the Ridge Regression model.
- **AWS Elastic Beanstalk**: Deployment platform for scalable cloud hosting.

---

## Acknowledgments

- **Dataset**: Thanks to the creators of the Algerian Forest Fire Dataset.
- **Community**: Gratitude to the open-source community for tools and support.

---




