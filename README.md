# 🏠 Real Estate Price Prediction with Web Scraping and Machine Learning

## 📌 Project Overview
This project aims to predict house prices by leveraging real estate data scraped from the platform [Zingat](https://www.zingat.com/). Data from four major cities in Turkey—**Istanbul**, **İzmir**, **Ankara**, and **Antalya**—was extracted using Python and web scraping libraries such as `BeautifulSoup` and `selenium`. The data includes detailed features like the house's size, age, location, and additional attributes, providing a rich dataset for predictive modeling.

The analysis focuses on understanding the regional trends in real estate prices and building accurate predictive models for estimating house sale prices.

---

## 🛠️ Tools and Libraries
- **Python Libraries**: `BeautifulSoup`, `selenium`, `pandas`, `numpy`, `scikit-learn`, `tensorflow`, and `matplotlib`.
- **Web Scraping**: Collected house data from Zingat, including price, size, location, and detailed features.
- **Machine Learning Techniques**: Regression models (Linear, Ridge, Lasso), Gradient Boosting, XGBoost, and Deep Learning.
- **Deep Learning Framework**: TensorFlow/Keras for building and training advanced predictive models.


---

## 📊 Dataset Description
The dataset comprises house listings and their respective features. Below are the main attributes used for prediction:

| Column Name              | Description                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------|
| **Fiyat**                | Price of the house (in Turkish Lira).                                                         |
| **İlan Tarihi**          | Listing date of the property.                                                                 |
| **Net m²**               | Usable area in square meters.                                                                 |
| **Brüt m²**              | Gross area in square meters.                                                                  |
| **Oda Sayısı**           | Number of rooms (e.g., 2+1: 2 bedrooms, 1 living room).                                       |
| **Banyo Sayısı**         | Number of bathrooms.                                                                          |
| **Binadaki Kat Sayısı**  | Total number of floors in the building.                                                       |
| **Bulunduğu Kat**        | Floor of the house (e.g., "Ara Kat" = middle floor).                                          |
| **Bina Yaşı**            | Age of the building.                                                                          |
| **Isıtma Tipi**          | Heating system type (e.g., "Kombi (Doğalgaz)").                                               |
| **Kira Getirisi**        | Monthly rental income (in Turkish Lira).                                                      |
| **Kullanım Durumu**      | Occupancy status (e.g., "Boş" = empty).                                                       |
| **Krediye Uygun**        | Mortgage eligibility.                                                                         |
| **Şehir**                | City where the house is located (Istanbul, İzmir, Ankara, Antalya).                           |

---

## 🧠 Predictive Modeling
### Goal
To build a model that accurately predicts house prices based on the given features.

### Results
The following models were tested, with **Deep Learning** achieving the highest performance:

| Model                    | \( R^2 \) Score | RMSE (₺)      | MAE (₺)       |
|--------------------------|-----------------|---------------|---------------|
| **Gradient Boosting**    | 0.848216        | 4,613,445     | 2,856,061     |
| **Lasso Regression**     | 0.831928        | 4,854,683     | 3,283,675     |
| **Linear Regression**    | 0.831927        | 4,854,690     | 3,283,684     |
| **Ridge Regression**     | 0.830090        | 4,881,151     | 3,290,025     |
| **XGBoost Regressor**    | 0.812019        | 5,134,160     | 2,690,256     |
| **Decision Tree**        | 0.709215        | 6,385,557     | 3,166,481     |
| **Extra Trees Regressor**| 0.677541        | 6,724,351     | 3,074,977     |
| **K-Nearest Neighbors**  | 0.546021        | 7,978,675     | 4,144,365     |
| **Elastic Net**          | 0.447074        | 8,805,342     | 5,177,581     |

**Deep Learning Model Performance**:
- \( R^2 \): **0.855**
- RMSE: **₺4.51M**
