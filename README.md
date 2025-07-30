

# Signal Strength Mapping, Prediction & Coverage Gap Detection Using ML

This project uses real-world telecom (UMTS,LTE) signal data to:

-  Visualize signal strength geographically
-  Predict signal strength at new locations using Machine Learning
-  Detect coverage gaps or dead zones to assist RAN planning

---

##  Project Overview

| Component                  | Purpose                                                                 |
|---------------------------|-------------------------------------------------------------------------|
| Signal Heatmap            | Map real signal values on an interactive map                            |
| ML Prediction Model       | Predict signal strength at any lat/lon using regression                 |
| Coverage Gap Detection    | Identify low-signal clusters using DBSCAN or threshold-based logic      |
| Reverse Geocoding         | Convert lat/lon to human-readable location names                        |

---

##  Tools & Technologies

| Tool / Library     | Purpose                                |
|--------------------|----------------------------------------|
| Python             | Core language                          |
| Pandas, NumPy      | Data processing                        |
| scikit-learn, XGBoost | ML models (regression, clustering)   |
| Folium, Plotly     | Interactive geospatial visualizations  |
| Geopy, Nominatim   | Reverse geocoding                      |
| Jupyter / Colab    | Notebook interface                     |

---

## 📁 Folder Structure

```
📦 signal-strength-mapping-ml/
├── data/                # UMTS raw dataset
├── notebooks/           # Jupyter notebooks for EDA & ML
├── src/                 # Python modules for mapping, modeling
├── outputs/             # Saved models, plots, maps
├── reports/             # Summary slides or write-ups
├── requirements.txt     # Python dependencies
├── README.md            # This file
```

---

## 🗂️ Dataset

- Format: CSV (uploaded)
- Features:
  - latitude, longitude, altitude
  - signal (target)
  - CELL_ID, Network_Type, MCC, MNC
  - timestamp1, timestamp2

> Optional: Convert timestamps to readable format and add location names using reverse geocoding.

---

##  Machine Learning Approach

- Model: RandomForestRegressor / XGBoost
- Input: latitude, longitude, altitude (+ optional cell/network info)
- Target: signal (RSSI / dBm)
- Evaluation: R² score, RMSE, actual vs predicted visualization

---

##  Coverage Gap Detection

- Method: DBSCAN or threshold-based clustering
- Goal: Highlight weak-signal or no-signal zones
- Output: Geospatial cluster map of gaps

---

##  Map Outputs

- Heatmap: Real signal distribution (Folium)
- Prediction Map: Predicted signal strength
- Coverage Gap Map: DBSCAN-based clusters of poor coverage

---

##  How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/signal-strength-mapping-ml.git
   cd signal-strength-mapping-ml
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

---

##  Outcomes

-  Signal strength visualized across locations
-  Model that predicts signal at unknown coordinates
-  Dead zone detection for network planning
-  Human-readable location names for better insights

---

##  License

This project is licensed under the [MIT License](LICENSE).

