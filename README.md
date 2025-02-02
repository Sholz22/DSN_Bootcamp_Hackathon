# Prediction Model for DSN Bootcamp Hackathon

## Overview
This repository contains a machine learning prediction model developed during the DSN Bootcamp Hackathon. The model is designed to predict "Target" using various input features from the provided dataset.

## Features
- Data preprocessing and feature engineering
- Model training and evaluation
- Performance metrics visualization
- Pre-trained model for inference
- Deployment-ready scripts

## Dataset
The model is trained on the following datasets:
- **Train Dataset.csv** – Contains training data with labeled examples.
- **Test Dataset.csv** – Contains test data for model evaluation.
- **Sample Submission.csv** – Example format for submitting predictions.
- **Variable_Definitions.csv** – Description of dataset variables.

## Installation
To run this project locally, follow these steps:
```bash
# Clone the repository
git clone https://github.com/Sholz22/DSN_Bootcamp_Hackathon
cd DSN_Bootcamp_Hackathon

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt
```

## Usage

### **Running the Notebook**
1. Ensure you have installed all dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Open Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Navigate to `DSN_Bootcamp_Hackathon.ipynb` and open it.
4. Follow the notebook’s step-by-step instructions to:
   - Load the dataset
   - Train the models (CatBoost & SVM)
   - Evaluate model performance
   - Make predictions

### **Making Predictions**
To generate predictions using the trained models within the notebook:
1. Run all necessary cells in `DSN_Bootcamp_Hackathon.ipynb`.
2. Ensure the **test dataset** is loaded correctly.
3. Execute the prediction cells to generate outputs.
4. The predictions will be saved as `predictions.csv` in the project directory.

## Model Performance

| Metric      | CatBoost      | Support Vector |
|-------------|---------------|---------------|
| Accuracy    | 0.81          | 0.82          |
| Precision   | 0.87          | 0.82          |
| Recall      | 0.91          | 1.00          |
| F1-score    | 0.89          | 0.90          |

### **Performance Analysis**
- **Support Vector Machine (SVM)** achieved slightly higher **accuracy (0.82)** compared to CatBoost (0.81), meaning it made fewer total errors.
- **CatBoost** had better **precision (0.87)** than SVM (0.82), indicating it had fewer false positives.
- **SVM** had a perfect **recall (1.00)**, meaning it identified all positive cases but at the cost of lower precision.
- The **F1-score** is almost the same for both models, showing a good balance of precision and recall.

### **Conclusion**
- If **false positives are costly**, CatBoost may be the better choice due to its higher precision.
- If **capturing all positive cases is critical**, SVM is preferable due to its perfect recall.

## Directory Structure
```
├── data
│   ├── Train Dataset.csv
│   ├── Test Dataset.csv
│   ├── Sample Submission.csv
│   ├── Variable_Definitions.csv
├── models
│   ├── output_file.pkl
├── notebooks
│   ├── DSN_Bootcamp_Hackathon.ipynb│ 
├── requirements.txt
├── README.md
```

## Contributing
Contributions are welcome! Please open an issue or submit a pull request if you’d like to improve this project.

## License
This project is licensed under the [MIT License](LICENSE).
