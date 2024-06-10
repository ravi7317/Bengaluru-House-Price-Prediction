Bengaluru House Price Prediction - README
Project Overview
This project aims to predict house prices in Bengaluru, India, using various regression techniques. The dataset contains information about the house's area, location, size, price, and other features. By cleaning the data and applying machine learning models, we can build a predictive model to estimate the price of houses based on the provided features.

Dataset
The dataset used in this project is bengaluru_house_prices.csv, which contains the following columns:

area_type: The type of the area (e.g., Super built-up Area, Plot Area, etc.)
availability: Availability status of the house
location: Location of the house
size: Size of the house (e.g., 2 BHK, 3 BHK)
society: Society name
total_sqft: Total area in square feet
bath: Number of bathrooms
balcony: Number of balconies
price: Price of the house in Lakhs
Project Steps
Data Loading and Initial Exploration:

Load the dataset and inspect its shape and columns.
Display initial records to understand the data structure.
Data Cleaning:

Drop unnecessary columns (area_type, society, balcony, availability).
Remove rows with missing values.
Extract the number of bedrooms (bhk) from the size column.
Convert the total_sqft column to numeric values, handling ranges and invalid entries.
Feature Engineering:

Create a new column price_per_sqft by dividing the price by total square feet.
Simplify the location column by grouping less frequent locations into a single category called other.
Outlier Detection and Removal:

Remove data points where the ratio of total area to BHK is below a threshold (e.g., 300 sqft per BHK).
Remove outliers in price_per_sqft using mean and standard deviation.
Remove outliers in bhk prices.
Data Visualization:

Plot scatter charts to visualize the relationship between total area and price for different BHK categories.
Plot histograms to visualize the distribution of price_per_sqft and number of bathrooms.
Model Building:

Encode the location column using one-hot encoding.
Split the dataset into training and testing sets.
Train a Linear Regression model and evaluate its performance using cross-validation.
Model Tuning:

Use GridSearchCV to find the best parameters for Linear Regression, Lasso, and Decision Tree models.
Evaluate and compare model performance to select the best model.
Prediction Function:

Implement a function to predict house prices based on location, total area, number of bathrooms, and BHK.
Dependencies
To run the project, ensure you have the following libraries installed:

pandas
numpy
matplotlib
scikit-learn
install these libraries using pip:
pip install pandas numpy matplotlib scikit-learn
Running the Project
Load the Dataset:
Place the bengaluru_house_prices.csv file in the working directory.

Execute the Code:
Run the provided code in a Python environment (e.g., Jupyter Notebook, PyCharm).

Prediction:
Use the predict_price function to estimate house prices based on input parameters:
predict_price('location', total_sqft, bath, bhk)
predict_price('1st Phase JP Nagar', 1000, 2, 2)
predict_price('1st Phase JP Nagar', 1000, 3, 3)
predict_price('Indira Nagar', 1000, 2, 2)
predict_price('Indira Nagar', 1000, 3, 3)
Project Structure
Data Cleaning and Preparation:

Dropping unnecessary columns
Handling missing values
Feature extraction and conversion
Outlier Detection and Removal:

Removing anomalies based on area and price
Removing outliers in BHK pricing
Model Training and Evaluation:

Linear Regression model
Cross-validation and GridSearchCV for hyperparameter tuning
Model comparison
Visualization:

Scatter plots
Histograms
Contact
For any questions or suggestions, please contact Ravi Verma at ravikurmi8313@gmail.com
