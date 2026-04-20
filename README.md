# 🍽️ TasteOrbit: Restaurant Insights & Quality Prediction

## About this project

This project started as a way to explore how data can help us understand what makes a restaurant well-rated.

Using a Zomato dataset from Bengaluru, I looked at how factors like location, cuisine, cost, and number of votes relate to restaurant ratings. I also built a simple machine learning model to predict whether a restaurant is likely to be rated highly or not.

---

## Dataset

I used the Zomato Bangalore Restaurants dataset from Kaggle:

https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants

The dataset includes:

* Restaurant name
* Location
* Cuisines
* Approx cost for two people
* Ratings
* Number of votes

---

## What I tried to do

Instead of predicting exact ratings, I simplified the problem:

* Rating ≥ 4 → **Good (1)**
* Rating < 4 → **Not Good (0)**

This turns the problem into a classification task.

---

## How I approached it

### Data Cleaning

* Converted ratings like "4.1/5" into numeric values
* Removed commas from cost and converted it to float
* Dropped duplicates and handled missing values

---

### Feature Engineering

* Extracted a **main cuisine** from the cuisines column
* Converted categorical columns (location, cuisine) using **one-hot encoding**

---

### Data Splitting

The dataset was split into:

* 60% training
* 20% validation
* 20% testing

---

### Scaling

Used **StandardScaler** to bring all features to a similar scale.

---

### Models Used

* Logistic Regression
* Decision Tree

Logistic Regression gave more stable and consistent results.

---

## Results

* Validation Accuracy: ~85.7%
* Test Accuracy: ~85.5%

The scores are very close, which suggests the model generalizes well.

---

## Evaluation

I evaluated the model using:

* Confusion Matrix
* Precision, Recall, F1-score

These metrics helped understand how well the model predicts both good and not-good restaurants.

---

## 📊 Business Insights

From the analysis, a few useful patterns can be observed:

* Restaurants with **more votes tend to have higher ratings**, suggesting visibility and customer engagement matter.
* **Higher cost does not guarantee better ratings** — mid-range restaurants can perform just as well.
* Some **locations consistently show higher average ratings**, indicating that area plays a role in performance.
* The impact of cuisine exists, but **ratings across popular cuisines are fairly similar** overall.

👉 Overall, a combination of **good location, reasonable pricing, and strong customer engagement** seems to be linked with better-rated restaurants.

---

## What I learned

* Real-world data requires proper cleaning before modeling
* Encoding categorical variables is important for ML models
* Splitting data correctly helps avoid misleading results
* Accuracy alone is not enough — other metrics matter too

---

## Limitations

* Ratings are used as a proxy for quality, not actual business success
* The data is limited to Bengaluru
* Other factors like service, ambience, etc. are not included

---

## Future Improvements

* Try models like Random Forest or XGBoost
* Perform hyperparameter tuning
* Analyze feature importance
* Build a simple application using this model

---

## Final Thoughts

This project gave me a complete understanding of the machine learning workflow — from cleaning raw data to building and evaluating a model.

---

## Author

Meghna K
