# IPL-ScorePro

This project is a web application built using Flask, allowing users to predict the first innings score in an Indian Premier League (IPL) cricket match based on various features. The application uses a machine learning model trained on historical IPL data to make predictions.

## Features

- **User Authentication:** Users can register and log in to the system. User authentication is handled securely, and passwords are encrypted before storage.

- **Score Prediction:** The core functionality of the application is predicting the first innings score in an IPL match. Users can input details such as batting and bowling teams, overs, runs, wickets, runs in the last 5 overs, and wickets in the last 5 overs to receive a predicted score range.

- **Machine Learning Model:** The prediction is powered by a Linear Regression machine learning model trained on historical IPL data. The model takes various factors into account to make accurate score predictions.

- **Database Integration:** User registration details are stored in a MySQL database. The database is also utilized to check for existing accounts during registration.

## How to Use

1. **User Registration/Login:**
   - Users can register for an account by providing a username, email, and password.
   - Existing users can log in using their email and password.

2. **Score Prediction:**
   - After logging in, users can navigate to the prediction page.
   - Select the batting and bowling teams, enter details such as overs, runs, wickets, runs in the last 5 overs, and wickets in the last 5 overs.
   - Click the "Predict" button to receive a predicted score range.

3. **Machine Learning Model Update:**
   - The application includes a machine learning model (`first-innings-score-lr-model.pkl`) that can be updated with new data. The model is trained on historical IPL data from the `ipl.csv` file.

## Requirements

- Python 3.x
- Flask
- Flask-MySQLdb
- scikit-learn
- pandas
- numpy

## How to Run

1. Clone the repository to your local machine.
   ```bash
   git clone https://github.com/your-username/ipl-score-prediction.git
   cd ipl-score-prediction
   ```

2. Install the required dependencies.
   ```bash
   pip install -r requirements.txt
   ```

3. Update the MySQL configuration in `app.py` with your database details.

4. Run the application.
   ```bash
   python app.py
   ```

5. Open your web browser and go to [http://localhost:5000/](http://localhost:5000/) to access the application.

## Machine Learning Model Update

1. If you have new data, update the `ipl.csv` file with the relevant information.

2. Run the Jupyter notebook `model_training.ipynb` to retrain the machine learning model.

3. Save the trained model using pickle.
   ```python
   filename = 'first-innings-score-lr-model.pkl'
   pickle.dump(regressor, open(filename, 'wb'))
   ```

4. Replace the existing `first-innings-score-lr-model.pkl` with the newly generated model in the Flask application.

## Contributing

Feel free to contribute to this project by opening issues, providing feedback, or submitting pull requests. Your contributions are welcome!

Your output of index page will look similar to this : 

[IPL-Output.webm](https://github.com/Ganesh-balaji-22/IPL-ScorePro/assets/145870375/56530d6f-9fc8-42aa-bb76-7fc8b35ccc6e)





