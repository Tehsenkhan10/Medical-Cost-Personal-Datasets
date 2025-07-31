# Medical-Cost-Personal-Datasets
🧠 Medical Cost Prediction with Regression Target Balancing and ML Models
This project focuses on predicting medical insurance charges using the Medical Cost Personal Dataset. The primary challenge in this dataset is the highly skewed distribution of the target variable charges, which requires preprocessing and balancing. Multiple target transformation techniques were applied to improve prediction performance, followed by three machine learning regression models.
📁 Dataset
Source: Kaggle - Medical Cost Personal Datasets
Target Variable: charges – actual medical expenses incurred.
Features:
age, sex, bmi, children, smoker, region
🛠️ Preprocessing
Label Encoding: Categorical columns (sex, smoker, region) converted to numeric.
Feature Scaling: age, bmi, and charges scaled using StandardScaler.
Skew Analysis: Initial histogram showed strong right skew in charges.
⚖️ Target Balancing Techniques
Applied 10 different transformations to reduce skewness and rebalance rare, high-cost values:
#	Technique	Description
1	Log Transform	Compresses high values
2	Square Root	Gentle skew reduction
3	Box-Cox	Adapts transformation to data
4	Yeo-Johnson	Handles zero and negative values
5	Winsorization	Clipping extreme outliers
6	Quantile (Uniform)	Uniform distribution mapping
7	Quantile (Normal)	Normal (bell-shaped) distribution
8	Binning	Discretizes target into levels
9	SMOGN	Synthetic oversampling for regression
10	KDE Resampling	Manual oversampling based on target split
Each technique was visualized using histogram and KDE plots for interpretability.
🤖 Machine Learning Models Used
Three regression models were trained and evaluated using the preprocessed dataset:
1. Linear Regression
Simple and interpretable
Sensitive to skew and outliers
2. Random Forest Regressor
Ensemble-based model
Robust to non-linearities and skew
3. Support Vector Regressor (SVR)
Effective in high-dimensional spaces
Performs best on scaled features
📊 Evaluation Metrics
All models were evaluated using:
MAE (Mean Absolute Error)
MSE (Mean Squared Error)
R² Score (Explained Variance)
Results were compared across different target transformations.
🔍 Insights
Target transformations significantly improved model performance, especially for linear regression.
Random Forest showed consistent performance across original and transformed targets.
SMOGN and Quantile Normalization provided well-balanced target distributions.

