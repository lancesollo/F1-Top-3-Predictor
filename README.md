his project uses FastF1, machine learning (Gradient Boosting Regressor), and real-world F1 data (lap times, qualifying performance, weather, and team strength) to predict the top 3 drivers for the upcoming Grand Prix—specifically the 2025 Monaco GP.

📊 What This Project Does
Loads and processes Monaco 2024 lap data using FastF1.

Gathers driver sector times and aggregates clean air race pace.

Pulls qualifying results for the 2025 Canadian GP as input.

Fetches real-time weather forecasts via the OpenWeather API.

Calculates team performance scores from constructor points.

Uses historical Monaco performance for context.

Trains a Gradient Boosting Regression Model.

Predicts 2025 Monaco GP finishing times.

Outputs Top 3 podium predictions.

Visualizes feature importance and performance correlations.

🔧 Installation
1. Clone the Repository
bash
Copy
git clone https://github.com/yourusername/yourrepo.git
cd yourrepo
2. Create a Virtual Environment
bash
Copy
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
3. Install Requirements
bash
Copy
pip install -r requirements.txt
4. Set up API Key
Replace this line in the script:

python
Copy
API_KEY = "YOURAPIKEY"
With your OpenWeatherMap API key from: https://openweathermap.org/api

🧠 Technologies Used
fastf1

pandas

numpy

scikit-learn

matplotlib

requests

🧪 How It Works
FastF1 loads Monaco 2024 race session and driver lap/sector data.

Data is cleaned and converted into usable metrics (e.g., time in seconds).

Canadian GP 2025 qualifying times are merged with other metrics:

Weather forecast (rain, temperature)

Team strength (based on current constructor points)

Monaco-specific historical performance

A GradientBoostingRegressor is trained to predict average lap time.

Race finish time is predicted for each driver.

Results are ranked and plotted to highlight top 3 drivers and key performance factors.

📈 Sample Output
yaml
Copy
🏁 Predicted 2025 Monaco GP Winner 🏁
Driver  |  PredictedRaceTime (s)
------- | ------------------------
NOR     |  1500.12
PIA     |  1501.67
VER     |  1502.91

Model Error (MAE): 0.89 seconds
📌 To-Do
Add more race history for enhanced model generalization.

Improve feature engineering (driver form, tire degradation, pit strategy).

Allow track-specific adjustments (e.g., overtaking difficulty index).

Build Streamlit dashboard for interactive results.

✅ License
This project is licensed under the MIT License.

🙌 Credits
FastF1 by theoehrly

Weather Data: OpenWeatherMap

Scikit-Learn: https://scikit-learn.org

