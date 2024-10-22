# Vehicle Price Prediction

## Objective
The goal of this project is to develop a machine learning model that predicts the price of vehicles based on various features such as mileage, make, year, and other specifications. This project demonstrates the use of regression algorithms to predict continuous values.

## Dataset
The dataset contains various features of vehicles, including technical specifications and sale prices. The objective is to predict the price of a vehicle based on these features.

### Features:
- **make**: Manufacturer of the vehicle (e.g., Toyota, BMW)
- **model**: Specific model of the vehicle
- **year**: Year of manufacture
- **engine**: Engine specifications, including size and type
- **fuel_type**: Type of fuel used (e.g., Petrol, Diesel, Electric)
- **mileage**: Fuel efficiency in miles per gallon (MPG)
- **transmission**: Type of transmission (Automatic/Manual)
- **drivetrain**: Type of drivetrain (FWD, RWD, AWD)
- **vehicle_type**: Type of vehicle (Sedan, SUV, etc.)
- **price**: Target variable, representing the sale price of the vehicle in USD.

## Approach
### Data Preprocessing:
- **Handling Missing Values**: Checked for missing values and handled them accordingly.
- **Encoding Categorical Features**: Categorical features like `make`, `model`, `fuel_type` were encoded to numerical values for the machine learning models.
- **Feature Scaling**: A **StandardScaler** was used to normalize the feature values.

### Exploratory Data Analysis (EDA):
- Visualized the relationships between features like mileage, year, engine size, and price using plots to understand data trends and distributions.
- Analyzed the correlation between vehicle attributes and price to select the most important features.

## Modeling
The **Gradient Boosting Regressor** was used for predicting vehicle prices due to its effectiveness in handling complex relationships.

### Grid Search:
Performed grid search on Gradient Boosting Regressor to fine-tune hyperparameters, including:
- `n_estimators`
- `learning_rate`
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`
- `subsample`
- `max_features`

### Model Evaluation:
- **Mean Squared Error (MSE)**: 27,891,770.44
- **R-Squared (R²)**: 0.8989
- **Root Mean Squared Error (RMSE)**: 5279.46

## Running the Vehicle Price Prediction System
1. Clone the repository and ensure that you have all the dependencies installed.
2. Load the saved **gradient_boosting_model.sav** file.
3. Run the provided notebook or script to input the vehicle features.
4. The system will output the predicted price based on the provided features.

## Deployment
The final model is saved as a pickle file (`gradient_boosting_model.sav`). The model can be loaded and used in any deployment environment, such as a Flask or Django web app.

## Screenshots
If applicable, include screenshots of the EDA and prediction outputs.
