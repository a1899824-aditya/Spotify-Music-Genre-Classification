# 🎵 Spotify Music Genre Prediction – Classification Models in R

This project aims to classify the genre of Spotify songs using various audio features like speechiness, danceability, tempo, and popularity. Developed as the final project for the Data Taming (MATHS 7107) course, it applies machine learning models to a cleaned and preprocessed version of the Spotify dataset.

---

## 📁 Dataset

- **spotify.csv** (not provided here but assumed): Contains features for 5000+ songs such as:
  - `release_date`, `popularity`, `tempo`, `speechiness`, `danceability`, `genre`, and more

---

## 🎯 Objective

- Clean and preprocess Spotify song data
- Predict the song’s genre (e.g., rock, hip-hop, pop) based on audio features
- Compare performance across multiple classification models

---

## 🛠 Tools & Packages

- **R**, **RMarkdown**
- **tidymodels**, **themis**, **dplyr**, **ggplot2**
- **models used**:  
  - Linear Discriminant Analysis (LDA)  
  - k-Nearest Neighbors (KNN)  
  - Random Forest (RF)

---

## 🔄 Preprocessing Steps

- Extracted release year from `release_date`
- Removed high-missing or redundant columns (`track_id`, `mode`, etc.)
- Used `step_normalize`, `step_downsample`, and `step_date` for feature prep
- Handled class imbalance using `themis::step_downsample`

---

## 📊 Model Evaluation

| Model   | Accuracy | Sensitivity | Specificity | AUC   |
|---------|----------|-------------|-------------|-------|
| LDA     | ~0.67    | Varies by class | Medium    | ~0.70 |
| KNN     | ~0.72    | Medium         | Medium     | ~0.73 |
| RF      | **~0.81** | **High**     | High        | **0.85** ✅

- **Random Forest** performed best across all metrics and was selected as the final model

---

## 📈 Visualizations

- Genre distribution across release years  
- Popularity vs Speechiness by genre  
- Model ROC curves and confusion matrices  
- Prediction vs Actual genre performance  

---

## 🧠 Key Learnings

- Random Forest is robust for multi-class classification on structured audio features  
- Audio metadata like speechiness and danceability are highly informative for genre prediction  
- Proper preprocessing (e.g., downsampling, scaling, date handling) significantly improves model performance

---

## 📄 Report

See `Final_report.pdf` for full model details, EDA plots, evaluation, and appendix.

---

## 👤 Author

Aditya Venugopalan Nediyirippil  
GitHub: [a1899824-aditya](https://github.com/a1899824-aditya)

---

## ✅ Future Work

- Integrate audio previews using Spotify API  
- Build genre clustering models  
- Explore deep learning (e.g., LSTM, CNN on waveform/lyrics)
