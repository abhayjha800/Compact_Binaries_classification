# Compact_Binaries_classification
# Stellar Analysis Project

This README file provides a detailed overview of the "Stellar Analysis Project" for identifying and analyzing compact binaries or similar celestial objects, based on photometric data (e.g., magnitudes and redshifts) such as those retrieved from the Sloan Digital Sky Survey (SDSS). This document will guide you through the purpose, setup, and steps involved in running the notebook effectively.

---

## **Project Purpose**

The goal of this project is to:

1. Analyze photometric data (e.g., `u`, `g`, `r`, `i`, `z` magnitudes, and redshift) to identify stellar properties.
2. Use these features to classify celestial objects, focusing on compact binaries or other interesting classes.
3. Develop a methodology for feature extraction, visualization, and preparation for machine learning models.

This project leverages SDSS datasets and Python-based libraries to handle astronomical data processing, analysis, and visualization.

> **Note:** This project is a work in progress. We acknowledge that spectral data is essential for a more detailed and accurate analysis. Efforts are underway to acquire or simulate spectral data to enhance the study.

---

## **Features**

- **Photometric Data Analysis:** Use the provided magnitudes and redshifts to study object properties.
- **Feature Engineering:** Extract meaningful features such as color indices (e.g., `u-g`, `g-r`) for classification tasks.
- **Classification Ready:** Prepare a dataset for machine learning pipelines to classify compact binaries or similar objects.
- **Visualization:** Generate plots to explore correlations and distributions in the data.

---

## **Dependencies**

The project requires the following Python libraries and tools:

- `pandas` for data manipulation.
- `numpy` for numerical operations.
- `matplotlib` and `seaborn` for visualization.
- `scikit-learn` for machine learning tasks.
- Jupyter Notebook environment to run the code.


---

## **Step-by-Step Guide**

### 1. **Setup Environment**

Ensure you have Python 3.8+ installed. Install the dependencies listed above using `pip`.

### 2. **Input Data**

The input dataset includes the following columns:

- `obj_ID`: Unique object identifier.
- `alpha`, `delta`: Right ascension and declination (coordinates of the object).
- `u`, `g`, `r`, `i`, `z`: Photometric magnitudes in different bands.
- `class`: The class of the object (e.g., star, galaxy, quasar).
- `redshift`: The redshift of the object.

Ensure the data is saved in a CSV file and placed in the `data/` directory.

### 3. **Data Preprocessing**

- Load the dataset into a pandas DataFrame.
- Handle missing values, if any.
- Normalize or scale the magnitudes for easier analysis.

### 4. **Feature Engineering**

- Compute color indices such as `u-g`, `g-r`, `r-i`, and `i-z` to identify patterns indicative of compact binaries.
- Explore correlations between color indices and redshift.

### 5. **Visualization**

Generate visualizations to explore the data:

- Scatter plots for color indices vs. redshift.
- Histograms for the distribution of magnitudes and color indices.

### 6. **Classification Preparation**

- Label the data based on the `class` column or use clustering techniques for unsupervised classification.
- Split the data into training and testing sets.
- Export the processed dataset as a CSV file.

### 7. **Machine Learning**

(Optional)

- Train a classification model using `scikit-learn` or another library.
- Evaluate the model's performance using metrics such as accuracy, precision, and recall.

---



---

## **Trained Model Performance**

We trained a Random Forest Classifier to classify objects into `STAR`, `GALAXY`, and `QSO` (quasars) based on the photometric data. Below are the performance metrics:

```
              precision    recall  f1-score   support

      GALAXY       0.98      0.99      0.98     17845
         QSO       0.96      0.92      0.94      5700
        STAR       1.00      1.00      1.00      6455

    accuracy                           0.98     30000
   macro avg       0.98      0.97      0.97     30000
weighted avg       0.98      0.98      0.98     30000
```

---

## **Acknowledgements**

This project uses photometric data , ensure to cite the source appropriately. Refer to the [SDSS official website](https://www.sdss.org/) for citation details.

---

## **Future Work**

- Extend the analysis to include additional photometric features or external datasets.
- Incorporate machine learning models for advanced classification.
- Compare results with theoretical models or simulated data.
- Acquire or simulate spectral data for a more detailed analysis.

---

For queries or contributions, please reach out or submit issues via the GitHub repository.

Happy analyzing!

