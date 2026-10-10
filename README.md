# Airbnb Rental Price Prediction App

A Streamlit web application that predicts the price of an Airbnb listing based on key property attributes such as room type, number of guests accommodated, bathrooms, cancellation policy, cleanliness, and review score.

The app loads a pre-trained machine learning model and provides a simple user interface for generating rental price estimates in real time.

## Features

- Predict Airbnb listing prices from user input
- Simple and interactive Streamlit UI
- Supports the following input fields:
  - Room type
  - Number of guests accommodated
  - Bathrooms
  - Cancellation policy
  - Cleaning fee
  - Instant bookability
  - Review score rating
  - Bedrooms
  - Beds
- Displays predicted rental price in USD

## Tech Stack

- Python
- Streamlit
- Pandas
- NumPy
- scikit-learn
- XGBoost
- Joblib

## Project Structure

```bash
rental-price-prediction-app/
├── app.py
├── rental_price_prediction_model_v1_0.joblib
├── requirements.txt
└── README.md
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/AbhayPadda/rental-price-prediction-app.git
cd rental-price-prediction-app
```

2. Create and activate a virtual environment (optional but recommended):
```bash
python -m venv .venv
source .venv/bin/activate   # On macOS/Linux
.venv\Scripts\activate      # On Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Running the App

Start the Streamlit app with:

```bash
streamlit run app.py
```

Then open the URL displayed in the terminal (typically `http://localhost:8501`).

## How It Works

The app:

1. Loads a trained model from `rental_price_prediction_model_v1_0.joblib`
2. Collects user-provided listing information through a Streamlit form
3. Converts the input into a DataFrame
4. Passes the data to the trained model
5. Returns the predicted rental price

## Example Inputs

The app asks for inputs like:

- `Room Type`: Entire home/apt, Private room, Shared room
- `Accommodates`: Number of guests
- `Bathrooms`
- `Cancellation Policy`
- `Cleaning Fee Charged`
- `Instantly Bookable`
- `Review Score Rating`
- `Bedrooms`
- `Beds`

## Requirements

The project dependencies are listed in `requirements.txt` and include:

```txt
pandas==2.2.2
numpy==2.0.2
scikit-learn==1.6.1
xgboost==2.1.4
joblib==1.4.2
streamlit==1.43.2
```

## License

This project does not currently include a license file. If you plan to share or distribute it publicly, consider adding an appropriate open-source license.

## Notes

This app is intended as a simple demonstration of using a trained machine learning model in a Streamlit interface for rental price estimation. It can be extended with additional features such as:

- More listing attributes
- Better model tuning
- Deployment to cloud hosting
- API-based prediction service
- Improved UI/UX and charts
