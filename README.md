# Machine Learning Workflow Assignment

## Task 1: Label and Data Leakage Identification

* **Label:** The column `repeat_purchase_flag` is the label because it represents the specific outcome the model is being trained to predict.
* **Data Leakage:** The column `discount_used_on_repeat_order` would introduce data leakage because it contains information about the repeat purchase event itself, which would not be available at the time of prediction.

---

## Task 2: Critical ML Workflow Steps

Before training a complex Gradient Boosting model, the following two steps must be completed:

### 1. Exploratory Data Analysis (EDA)
**Why it matters:** EDA allows the analyst to understand the distribution of data, detect outliers, and identify class imbalances. For instance, if only 2% of customers repeat purchase, the model might simply learn to predict "0" every time unless we address the imbalance discovered during EDA.

### 2. Feature Scaling and Data Splitting
**Why it matters:** Splitting the data into Training and Testing sets ensures we can evaluate the model on unseen data to check for overfitting. Furthermore, scaling ensures that features with large numerical ranges (like `avg_order_value`) do not disproportionately influence the model compared to smaller ranges (like `order_count`).
