Car Price Prediction Project 
Overview: 
The Car Price Prediction project uses machine learning to predict the selling price of a car based on 
several input features, such as the car’s name, year, current price, kilometers driven, fuel type, seller 
type, transmission, and the number of previous owners. The core of the solution is a Voting Regressor 
model, which combines predictions from multiple regression algorithms to generate a more accurate 
and robust price estimate. This model is trained on a dataset from Kaggle that contains historical car 
data, enabling it to make reliable predictions for new cars based on their characteristics. 
Technical Flow: 
Input: 
The application accepts user input in the form of a web form, where the user provides details about the 
car. The required input fields are: 
Car Name: The name of the car (text input). 
Year: The manufacturing year of the car (numeric input). 
Present Price: The current market value of the car (numeric input). 
Kms Driven: The total kilometers the car has been driven (numeric input). 
Fuel Type: The type of fuel the car uses (options: Petrol or Diesel). 
Seller Type: Whether the car is being sold by an individual or a dealer (options: Individual or Dealer). 
Transmission: The type of transmission (options: Manual or Automatic). 
Owner: The number of previous owners (numeric input). 
These inputs are collected from the user on the web interface and sent to the backend Flask application. 
Processing: 
1. Data Preprocessing: Once the inputs are received, the application processes the data. This includes 
encoding categorical variables (e.g., Fuel Type, Seller Type, Transmission) into numerical values that the 
model can understand. 
2. Model Inference: The processed data is passed to the Voting Regressor model, which is pre-trained on 
the Kaggle dataset. The model uses the input features to estimate the predicted car price. The Voting 
Regressor aggregates predictions from multiple base regression models to enhance the accuracy of the 
final output. 
3. Prediction Generation: The Voting Regressor generates a predicted price based on the input data and 
the trained model's internal algorithms. If the model encounters a situation where the predicted price is 
unrealistic (e.g., a negative value), the application will flag this as an issue. 
Output: 
The output is a predicted car selling price, which is displayed on the web interface for the user to view. If 
the model predicts a negative price, a message will inform the user that the car cannot be sold due to an 
unrealistic price. The output is presented in a user-friendly format, clearly showing the predicted price or 
an error message if applicable. The result is presented as text on the web page, making it easy for users 
to understand and use the prediction for decision-making.  
This process ensures that the application works seamlessly to predict car prices based on user-provided 
features, leveraging a robust machine learning model to deliver accurate, real-time predictions.
