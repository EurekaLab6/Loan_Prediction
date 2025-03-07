# Loan Prediction Based on Customer Behavior

- Build a model to help the creditor team to filter potential customers and prevent defaults.
- Extraction feature to optimizing the learning process of model.
- Train model with 5 different algorithms, and choose 1 for next hyperparameter tuning.
- Handle imbalanced class with Combining oversampling and undersampling (hybrid techniques).
  
# Problems
- In this case, **the acceptable default threshold is 5% based on Bank Indonesia Circular Letter No 6/23/DPNP 2004**, but in reality, **the default rate recorded reached 12.3%**.

# Purpose
Reduce the default rate to 5% based on the threshold that has been set.

# Dataset
- **Id:** User identity (object)
- **Income:** Monthly income Rupee currency (float)
- **Age:** Customer's age
- **Experience:** Customer's overall work experience
- **Married/Single:**
    - **Single:** Unmarried
    - **Married:** Married
- **House_Ownership:**
    - **Rented:** Renting
    - **Owned:** Private house
    - **Norent_noown:** Homeless
- **Car_Ownership:**
    - **Yes:** Have a Car
    - **No:** Don't have a car
- **Profession:** User's (obj) profession
- **City:** City of user (obj)
- **State:** State (obj)
- **Current_Job_Yrs:** Current job tenure (int)
- **Current_House_Yrs:** Home ownership status in years (int)
- **Risk_Flag (Target):**
    - **0:** Low default potential
    - **1:** High default potential

# Exploratory Data Analysis
   1. Distribution City of Risk Flag
    ![1](https://github.com/user-attachments/assets/f3ff4bb1-cdaf-41a3-97b3-d9f63e83ad33)

   2. Distribution income of Risk Flag
    ![2](https://github.com/user-attachments/assets/dc5ea1b6-e37d-49b0-bfdb-9f5eba8c287b)

   3. Distribution Age of Risk Flag
    ![3](https://github.com/user-attachments/assets/722c51aa-788f-43e9-9ed8-cc4a24680764)

   4. Distribution Profession of Risk FLag
    ![4](https://github.com/user-attachments/assets/fafbc925-8e25-43ea-89eb-f6a7f6555707)

   5. Distribution Experience of Risk Flag
    ![5](https://github.com/user-attachments/assets/7a0882be-ffaf-44ed-9eb2-ae2489949589)

## Summary of EDA
The Loan Prediction dataset is used to identify default patterns. The analysis showed that creditors who are single, have no assets, have low income, or have limited work experience have the highest risk of default. Certain professions, such as police, and domicile location, such as Bhubaneswar City and Manipur state, were also significant factors. Based on these findings, we recommend the development of flexible loan categories based on the economic class of the creditor, financial literacy training, and cooperation with local institutions to minimize the risk of default. In addition, adjustments to credit limits, interest rates, as well as community-based support are proposed to improve the success of the loan program.

# ML Modeling
Before train the model, split the data into train set & test set (size is 20%). Trained the model with 5 different algorithm and evaluated them with **Recall**. The reason is to **reduce** False Negative. This is for good filtering potential customers, and in the end, creditors can prevent defaults made by prospective customers in the future. The model was trained  with:
   - **Decision Tree**
   - Random Forest
   - XGBoost
   - KNN
   - Logistic Regression

# Model Evaluation

The table below shows a comparison of the performance of some tested *machine learning* algorithms.

| Algorithm             | Recall (Train) | Recall (Test) | Accuracy (Train) | Accuracy (Test) |
| --------------------- | -------------- | ------------- | ---------------- | --------------- |
| **Decision Tree**     | **1.00**       | **0.86**      | **0.95**         | **0.86**        |
| Random Forest         | 1.00           | 0.81          | 0.95             | 0.88            |
| XGBoost               | 0.85           | 0.70          | 0.89             | 0.88            |
| KNN                   | 0.18           | 0.09          | 0.65             | 0.85            |
| Logistic Regression   | 0.27           | 0.27          | 0.63             | 0.79            |

**Explanation:**

- **Recall:** Measures the ability of the model to find all true positive examples.
- **Accuracy:** Measures how often the model predicts correctly.
- **Train:** Model performance on training data.
- **Test:** Model performance on test data.

**Conclusion:**
Based on the table above, the **Decision Tree** algorithm is the best choice for this *dataset*.


Below to see how the model works:
- **Streamlit App:**
[Streamlit](https://final-riskmodelapp-eurekalab.streamlit.app/)
