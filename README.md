## **Australia Rain Prediction Classifier**

### **Project Goal**

This project is my first deep dive into building an **AI/ML prediction model** end-to-end. The main goal here is to take weather data and build a machine learning classifier that can predict whether it will **rain tomorrow** in a few specific Australian cities.  
This project was a great way for me to practice:

* **Data Cleaning and Feature Engineering** (especially dealing with dates, seasonality, and missing values).  
* **Preventing Data Leakage** (a critical step for time-series/sequential data like weather\!).  
* Setting up a robust **Scikit-learn Pipeline** with a ColumnTransformer.  
* Comparing the performance of two common models: **Logistic Regression** and **Random Forest**.

### **Project Status (Important Note\!)**

The current notebook is a work in progress. I've focused on getting the data cleaned and features ready. I'm currently working on finalizing the modeling, including fixing a look-ahead bias (data leakage) issue and running the final Grid Search Cross-Validation.  
**I will update this README once the model training and final evaluation sections are complete.**

### **Technology Used**

* **Language:** Python  
* **Core Libraries:**  
  * pandas (Data manipulation)  
  * numpy (Numerical operations)  
  * scikit-learn (Modeling, Pipelines, and Evaluation)

### **How to Run the Notebook**

1. **Clone this repository:**  
``` 
   git clone https://github.com/zaidmaroof/AustraliaRainPrediction.git  
   cd AustraliaRainPrediction
```
2. **Get the data:**  
   * I've included the required AusWeather.csv file in this repository for easy, offline running.  
3. **Install dependencies:**  
``` 
   pip install requirements.txt
```
4. **Launch Jupyter Notebook** and open Australia\_Rain\_Prediction.ipynb.

### **Key Steps in the Notebook**

1. **Data Loading and Cleanup:** Dropped external dependencies and removed rows with missing data (a temporary step to simplify the project).  
2. **Focus Area:** Filtered the data to focus only on three nearby locations (Melbourne, MelbourneAirport, Watsonia) to build a highly localized model.  
3. **Feature Engineering:**  
   * Extracted month and year from the Date column.  
   * Created a custom Season feature, correctly mapping the Southern Hemisphere's seasons (e.g., Summer is Dec/Jan/Feb).  
4. **Pipeline Setup:** Defined a ColumnTransformer to handle my numeric and categorical features separately (scaling numbers, one-hot encoding categories).

### **Results**

Compared Random Forest Regression with Logistic Regression. I will further improve Feature selection, data leakage, missing values and maybe explore more models.