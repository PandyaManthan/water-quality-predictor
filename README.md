# Water Quality Pollutants Predictor

A Streamlit web application that predicts water pollutant levels based on year, station ID, and month.

## Features

- Predicts pollutant concentrations for 9 different water quality parameters
- Compares predictions against safety thresholds
- Displays water quality safety percentage
- Detailed information about pollutant significance

## Pollutants Predicted

- NH₄ (Ammonium)
- BSK5 (Biochemical Oxygen Demand)
- Suspended Solids
- O₂ (Dissolved Oxygen)
- NO₃ (Nitrate)
- NO₂ (Nitrite)
- SO₄ (Sulfate)
- PO₄ (Phosphate)
- Cl (Chloride)

## Local Installation

1. Clone the repository:
```bash
git clone https://github.com/PandyaManthan/water-quality-predictor.git
cd water-quality-predictor
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the app locally:
```bash
streamlit run app.py
```

The app will automatically download the trained model files from Google Drive on first run.

## Deployment on Streamlit Cloud

### Prerequisites
- GitHub account
- Streamlit Cloud account (free)

### Steps

1. **Ensure code is pushed to GitHub**
   - This repository is already on GitHub at: https://github.com/PandyaManthan/water-quality-predictor

2. **Deploy on Streamlit Cloud**
   - Go to [share.streamlit.io](https://share.streamlit.io)
   - Click "New app"
   - Connect your GitHub account
   - Select:
     - Repository: `PandyaManthan/water-quality-predictor`
     - Branch: `main`
     - Main file path: `app.py`
   - Click "Deploy"

3. **Your app will be live at:**
   - `https://water-quality-predictor-[random-id].streamlit.app`

## How It Works

The application uses a trained machine learning model to predict water pollutant levels based on:
- **Year**: The year of prediction
- **Station ID**: The water quality monitoring station
- **Month**: The month of the year

The model outputs predictions for 9 different pollutants, which are then compared against safety thresholds to provide a water quality safety percentage.

## Model Files

Model files are stored in Google Drive and automatically downloaded on startup:
- `pollution_model.pkl` - The trained machine learning model
- `model_columns (1).pkl` - Feature column names used by the model

## Technologies Used

- **Streamlit** - Web application framework
- **Pandas** - Data manipulation
- **NumPy** - Numerical computation
- **Scikit-learn** - Machine learning library
- **Joblib** - Model serialization

## License

MIT License - see LICENSE file for details
