## Customer Segmentation
app link - https://customersegmentation-d9yyj4bnwkceuleruiypft.streamlit.app/

This project performs **Customer Personality Analysis** to identify and understand customer segments using **unsupervised machine learning**. The goal is to help businesses tailor marketing strategies, optimize targeting, and personalize experiences for different customer groups.

---

## 📌 Objective

- Analyze customer behavior based on demographics, spending habits, and campaign responses.
- Use clustering (K-Means) to identify distinct customer groups.
- Build an interactive **Streamlit dashboard** to visualize and explore these segments.

---

## 🗂️ Dataset

The dataset used is the **Customer Personality Analysis** dataset, which contains information about:
- Demographics (age, education, marital status)
- Spending on different product categories
- Campaign responses
- Purchase behavior and recency

---

## 🛠️ Features Engineered

| Feature | Description |
|--------|-------------|
| `Age` | Derived from `Year_Birth` |
| `Customer_Tenure` | Number of days since joining (`Dt_Customer`) |
| `Total_Children` | Sum of `Kidhome` and `Teenhome` |
| `Total_Spend` | Total monetary amount spent across all product categories |
| `Income` (imputed) | Missing values filled using median |

---

## 🔍 Data Preprocessing

- Removed irrelevant or constant columns: `ID`, `Z_CostContact`, `Z_Revenue`
- Imputed missing values (e.g., `Income`) using the median
- Converted categorical variables (`Education`, `Marital_Status`) using one-hot encoding
- Scaled numerical features using **StandardScaler**

---

## 🤖 Clustering

- Applied **K-Means Clustering** on the processed dataset
- Number of clusters is configurable via the UI
- Segments represent groups with similar purchasing behavior and demographic profiles

---

## Cluster Profiling & Final Insights
After training and analyzing the clustering model, four distinct customer segments were identified and profiled:

# Cluster 0: Mature Families with Teenagers
Definitely parents

Family size ranges from 2 to 4

Many are single parents

Most have teenagers at home

Tend to be older

# Cluster 1: High-Income Couples or Singles
Not parents

Small families (maximum 2 members)

Slight majority are couples

Spans all age groups

Characterized by high income

# Cluster 2: Young Families with Kids
Mostly young parents

Small families (up to 3 members)

Typically have young kids, not teenagers

Tend to be younger in age

# Cluster 3: Large, Lower-Income Families
Definitely parents

Families have between 2 to 5 members

Most have teenagers at home

Tend to be older

Represent a lower-income segment

## 📊 Streamlit Dashboard
![Screenshot 2025-05-29 175607](https://github.com/user-attachments/assets/44536219-827f-495e-a9db-4f165c617d49)

![Screenshot 2025-05-29 175652](https://github.com/user-attachments/assets/07d63bdc-0f5c-4927-b699-7a73c6e748a0)

![Screenshot 2025-05-29 175843](https://github.com/user-attachments/assets/ce5370f3-d72f-4e23-bcde-eabbf89cd710)



### ▶️ Run the App Locally

```bash
pip install -r requirements.txt
streamlit run streamlit_app.py
