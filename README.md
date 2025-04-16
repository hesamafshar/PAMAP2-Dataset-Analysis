# 📁 PAMAP2-Dataset-Analysis

## 📝 Description
This project performs an exploratory analysis and basic preprocessing on the **PAMAP2 Physical Activity Monitoring Dataset**, which includes multimodal sensor data collected from different body parts during various physical activities. The purpose of this notebook is to clean, visualize, and analyze the data to build a foundation for future classification and activity recognition tasks.

---

## 📊 Dataset Overview
- **Dataset Name:** PAMAP2 Physical Activity Monitoring
- **Subjects:** 9 individuals
- **Sensors:** IMUs placed on hand, chest, and ankle
- **Data Types:** Accelerometer, gyroscope, magnetometer, heart rate, and temperature
- **Activities:** Lying, Sitting, Standing, Walking, Running, Cycling, Nordic Walking, Vacuum Cleaning, Watching TV, etc.

---

## 📓 Notebook Workflow Summary

### `PAMAP2-Dataset-Analysis.ipynb`

This Jupyter notebook includes the following stages:

1. **Importing Required Libraries**
   - `pandas`, `numpy`, `scipy`, `scikit-learn`, `matplotlib`, etc., are imported for data manipulation and visualization.

2. **Activity Mapping**
   - Activity codes in the dataset are mapped to human-readable labels such as `'sitting'`, `'walking'`, `'cycling'`, etc.

3. **Understanding MET Categories**
   - Activities are grouped by intensity (e.g., light, moderate, vigorous) using their **MET (Metabolic Equivalent of Task)** values from the dataset documentation.

4. **Loading and Merging Raw Data**
   - Sensor data files are loaded and merged into a single unified DataFrame for ease of processing.

5. **Data Cleaning**
   - Redundant columns such as invalid orientation measurements and over-saturated accelerometer readings are identified and dropped.

6. **Missing Values Handling**
   - NaN values, mostly found in heart rate readings, are imputed or discarded as necessary.

7. **Feature Scaling**
   - Features are standardized using `StandardScaler` to make them suitable for downstream ML tasks.

8. **Data Segmentation**
   - Windowing strategies are introduced (but not fully implemented in this version) for future time-series modeling.

9. **Visualization**
   - Heatmaps of feature correlations and line plots are used to understand the relationship and variance between different sensor signals.

---

## 🛠 Tools & Libraries
- **Core Tools:** `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `scipy`
- **Visualizations:** Correlation heatmaps, time-series signal plots


