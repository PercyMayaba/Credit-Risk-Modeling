# Credit-Risk-Modeling
A comprehensive machine learning project for credit risk assessment and Expected Credit Loss (ECL) calculation using synthetic loan data. This project implements Basel-compliant credit risk frameworks including Probability of Default (PD), Loss Given Default (LGD), Exposure at Default (EAD), and Expected Credit Loss (ECL) modeling.
🎯 Objectives

    Develop predictive models for credit risk assessment

    Implement IFRS 9 ECL framework

    Create risk rating systems and stress testing scenarios

    Calculate regulatory capital requirements

    Provide comprehensive risk analytics and reporting

📁 Project Structure
text

credit-risk-modeling/
├── credit_risk_modeling.ipynb  # Main Colab notebook
├── README.md                   # Project documentation
├── synthetic_data.py           # Data generation module
├── risk_framework.py           # Risk calculation functions
└── utils/                      # Utility functions
    ├── visualization.py
    ├── model_training.py
    └── validation.py

🏦 Dataset
Synthetic Loan Data (50,000 records)

Loan Types:

    Home Loans (30%)

    Personal Loans (30%)

    Credit Cards (25%)

    Auto Loans (15%)

Key Features:

    Loan characteristics (amount, term, interest rate)

    Borrower demographics (income, age, employment)

    Credit history (score, utilization, delinquencies)

    Collateral information (LTV, property value)

    Default flags and risk parameters

🔧 Technical Implementation
Models Implemented

    Logistic Regression - Baseline model

    Random Forest - Ensemble method

    Gradient Boosting - Advanced ensemble

    XGBoost - Optimized gradient boosting

Credit Risk Framework

    PD (Probability of Default): Likelihood of borrower default

    LGD (Loss Given Default): Loss severity upon default

    EAD (Exposure at Default): Outstanding amount at default

    ECL (Expected Credit Loss): PD × LGD × EAD

📈 Key Features
1. Risk Rating System
text

AAA (PD ≤ 1%)    → Low Risk
AA  (PD ≤ 2%)    → 
A   (PD ≤ 5%)    → 
BBB (PD ≤ 10%)   → Medium Risk
BB  (PD ≤ 15%)   → 
B   (PD ≤ 25%)   → 
CCC (PD ≤ 40%)   → High Risk
Default (PD > 40%) → Default

2. Stress Testing Scenarios

    Baseline: Normal economic conditions

    Mild Recession: 1.5× PD increase

    Severe Recession: 2.5× PD increase

    Financial Crisis: 4.0× PD increase

3. Regulatory Compliance

    Basel II/III capital requirements

    Risk-weighted assets calculation

    Capital adequacy ratios

🚀 Quick Start
Prerequisites
python

!pip install pandas numpy scikit-learn matplotlib seaborn xgboost imbalanced-learn plotly

Run the Project

    Open credit_risk_modeling.ipynb in Google Colab

    Run all cells sequentially

    Review the comprehensive risk report at the end

Cell-by-Cell Execution

The notebook is organized into 20 logical cells:

    Install Dependencies - Required packages

    Import Libraries - All necessary imports

    Data Generation - Synthetic loan data creation

    Dataset Overview - Basic statistics and exploration

    EDA Visualizations - Distribution and correlation analysis

    Correlation Analysis - Feature relationships

    Feature Engineering - Creating derived features

    Class Balancing - Handling imbalanced data with SMOTE

    Feature Scaling - Standardization

    Model Training - Multiple algorithm implementation

    Model Comparison - Performance evaluation

    Feature Importance - Key risk drivers

    PD Modeling - Probability of Default calculation

    Risk Bucketing - Credit rating assignment

    ECL Calculation - Expected Credit Loss framework

    Portfolio Dashboard - Interactive risk visualization

    Stress Testing - Scenario analysis

    Capital Requirements - Regulatory capital calculation

    Model Validation - Backtesting and calibration

    Comprehensive Report - Executive summary

📊 Outputs Generated
Risk Metrics

    Portfolio-level ECL calculations

    Risk concentration analysis

    Capital adequacy ratios

    Stress testing results

Visualizations

    ROC curves and model performance

    Feature importance charts

    Risk rating distributions

    ECL analysis by loan type

    Interactive portfolio dashboard

Reports

    Model validation metrics

    Regulatory capital requirements

    Risk management recommendations

    Executive summary

🎨 Customization
Modify Loan Types
python

loan_types = ['Home Loan', 'Personal Loan', 'Credit Card', 'Auto Loan', 'Business Loan']
probabilities = [0.25, 0.25, 0.20, 0.15, 0.15]

Adjust Risk Parameters
python

# Modify risk weights for regulatory capital
risk_weights = {
    'AAA': 0.1, 'AA': 0.2, 'A': 0.4, 
    'BBB': 0.8, 'BB': 1.2, 'B': 1.8, 'CCC': 2.5, 'Default': 8.0
}

Add New Stress Scenarios
python

scenarios = {
    'Baseline': 1.0,
    'Economic Slowdown': 1.3,
    'Recession': 2.0,
    'Crisis': 4.0,
    'Custom Scenario': 1.8
}

📋 Model Performance

Typical results across different algorithms:
Model	AUC Score	Training Time	Interpretability
Logistic Regression	0.82-0.85	Fast	High
Random Forest	0.86-0.89	Medium	Medium
Gradient Boosting	0.87-0.90	Medium	Medium
XGBoost	0.88-0.91	Fast	Medium
🛠️ Technical Requirements
Python Packages

    pandas, numpy

    scikit-learn, xgboost

    matplotlib, seaborn, plotly

    imbalanced-learn

Hardware

    Minimum: 4GB RAM

    Recommended: 8GB+ RAM for full dataset

    Google Colab compatible

📚 Theoretical Framework
IFRS 9 ECL Model

    Stage 1: Performing assets (12-month ECL)

    Stage 2: Underperforming assets (lifetime ECL)

    Stage 3: Defaulted assets (lifetime ECL)

Basel Regulations

    Minimum capital requirements

    Risk-weighted assets

    Capital conservation buffers

🤝 Contributing

Feel free to:

    Add new risk models

    Enhance visualization capabilities

    Implement additional regulatory frameworks

    Improve documentation

📄 License

This project is for educational purposes. Adapt as needed for your specific requirements.
🆓 Support

For questions or issues:

    Check the notebook comments

    Review model documentation

    Validate input data formats

Note: This implementation uses synthetic data for demonstration. For production use, replace with real loan data and conduct proper model validation.
