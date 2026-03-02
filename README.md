🛰️ Dubai Land Cover Classification (Sentinel-2 + ANN + Random Forest)

Land cover classification of Dubai, United Arab Emirates using Sentinel-2 imagery and machine learning (Artificial Neural Network + Random Forest) in Google Earth Engine.

📌 Project Overview

This project performs supervised land cover classification over Dubai using:

Sentinel-2 Surface Reflectance imagery

Custom training polygons

Stratified balanced sampling

Artificial Neural Network (ANN) using TensorFlow

Random Forest (RF) using Earth Engine

Land Cover Classes
Class ID	0, 1, 2, 3
Land Cover Type: 0: Desert, 1: Urban, 2: Water, 3: Vegetation
🗺️ Study Area

The study area covers the Emirate of Dubai, UAE.

Boundary source: FAO GAUL 2015 Level 1

Country: United Arab Emirates

Region: Dubai

🛰️ Satellite Data

Satellite: Sentinel-2

Dataset: COPERNICUS/S2_SR_HARMONIZED

Time Period: January – June 2025

Spatial Resolution: 10 meters

Bands Used:

B2 (Blue)

B3 (Green)

B4 (Red)

B8 (NIR)

Cloud masking is applied using the QA60 band.

🧠 Methodology
1️⃣ Image Preprocessing

Filter by date and Dubai boundary

Apply cloud masking

Create median composite

Select 10m bands (B2, B3, B4, B8)

2️⃣ Training Data Preparation

Manually defined training polygons for:

Desert

Urban

Water

Vegetation

Converted polygons to label image

Stratified sampling:

800 samples per class

Total: 3,200 samples

Balanced dataset

3️⃣ Artificial Neural Network (ANN)

Model architecture:

Dense (128) – ReLU

Dense (64) – ReLU

Dense (32) – ReLU

Dropout (0.3)

Dense (4) – Softmax

Training features:

Normalized reflectance values (B2, B3, B4, B8)

Evaluation:

Train/test split (80/20)

Confusion matrix

Classification report

Test accuracy

4️⃣ Random Forest Classification (Earth Engine)

Classifier: smileRandomForest

Trees: 200

Applied to full Dubai composite

Output clipped to Dubai boundary

🎨 Visualization

RGB Composite (B4, B3, B2)

Classified Land Cover Map

Custom legend:

Yellow → Desert

Red → Urban

Blue → Water

Green → Vegetation

Visualization is performed using the geemap interactive map.

📊 Expected Outputs

ANN accuracy metrics

Confusion matrix

Classification report

Full land cover map of Dubai

Interactive map visualization

🛠️ Technologies Used

Python

Google Earth Engine API

Geemap

TensorFlow

Scikit-learn

NumPy
Pandas


<img width="773" height="446" alt="Screenshot 2026-03-02 182716" src="https://github.com/user-attachments/assets/89c05947-950e-45ea-84ec-7dbb636f6e00" />


<img width="705" height="457" alt="image" src="https://github.com/user-attachments/assets/5f0ba3dc-b6bb-4e78-9592-0fb449ba061d" />

