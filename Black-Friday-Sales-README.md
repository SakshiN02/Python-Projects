
# 🛒 **Black Friday Sales - Exploratory Data Analysis (EDA) 📊**  

## **📢 Introduction**  
Welcome to the Black Friday Sales EDA! 🏪🛍️ This analysis dives into a dataset containing purchase behavior from a retail store, helping us uncover customer spending trends, demographic influences, and product preferences.  

Through this notebook, we will:  
✅ **Clean & preprocess data** 🧹  
✅ **Explore spending patterns** 📈  
✅ **Visualize key insights** 🎨  
✅ **Understand customer behavior** 🧐  

---

## **📂 Dataset Overview**  
The dataset consists of several important features:  

- 🆔 **User_ID** & **Product_ID** – Unique identifiers for customers and products  
- 👦 **Age**, 👩 **Gender**, 💍 **Marital_Status** – Customer demographics  
- 🏙️ **City_Category**, 🏠 **Stay_In_Current_City_Years** – Customer location & duration of stay  
- 🛍️ **Product_Category_1, 2, 3** – Product classifications  
- 💰 **Purchase** – Amount spent by the customer  

---

## **🔍 Data Preprocessing & Cleaning **  
Before jumping into the analysis, we ensured clean data by:  
✅ Handling missing values in Product_Category_2 & 3  
✅ Converting categorical data into **meaningful numerical representations  
✅ Checking for duplicates & inconsistencies  

Now, we’re ready for some data visualization magic! 🎩✨  

---

## **📊 Key Visualizations & Insights**  

### **1️⃣ Distribution of Product Categories 📦**  

fig, axes = plt.subplots(1, 3, figsize=(15, 5))
sns.histplot(df["Product_Category_1"], bins=15, kde=True, ax=axes[0], color="teal")
sns.histplot(df["Product_Category_2"], bins=15, kde=True, ax=axes[1], color="orange")
sns.histplot(df["Product_Category_3"], bins=15, kde=True, ax=axes[2], color="blue")

![Image](https://github.com/user-attachments/assets/2483adde-90f9-47ea-9cae-e597e8558a14)

The same plot is visualized using Plotly to get the ticker labels and understand it better-

![Image](https://github.com/user-attachments/assets/492bef3f-ea4c-4fc5-a02f-375a9b03ce91)

💡 **Findings:**

- Most purchases are concentrated in a few product categories** (indicating popular items).  
- Product Category 1 has the highest purchase density, followed by Category 2 & 3.  
- Some categories have minimal purchases, indicating niche products.  

### **2️⃣ Purchase Behavior by Occupation 👔💰 (Violin Plot 🎻)** 

sns.violinplot(data=df, x="Occupation", y="Purchase", ax=axes[1, 1])


![Image](https://github.com/user-attachments/assets/0891e4e7-5105-45d8-81d4-2d663a3623d4)

💡 **Findings:**  
- Different occupations have varied spending behavior.  
- Some professions have multiple peaks, indicating clusters of high & low spenders.  
- The spread of spending varies, suggesting certain occupations have a broader range of purchase values.  


### **3️⃣ Average Purchase by Gender & Marital Status 👨‍💼👩‍💼**  

sns.lineplot(data=df, x="Occupation", y="Purchase", hue="Gender", style="Marital_Status")

![Image](https://github.com/user-attachments/assets/f1c8d0f9-543f-4acc-89ca-16ac690a3792)

💡 **Findings:**  
- Males generally have higher average purchases than females.  
- Married individuals tend to spend more than singles in most occupations.  
- There’s a spike in purchase behavior for specific occupations, possibly due to income levels or spending habits. 


### **4️⃣ Purchase Trends by Stay Duration & City Category 🏙️**  

sns.barplot(data=df, x="Stay_In_Current_City_Years", y="Purchase", hue="City_Category")

![Image](https://github.com/user-attachments/assets/1bedf2a5-5bf3-4674-9083-72b7da09a813)

💡 **Findings:**  
- Customers in City Category C tend to have the highest purchases.  
- Long-term residents (4+ years) don’t necessarily spend more, indicating that newcomers and short-term residents are also significant buyers.  



## **📝 Conclusion & Business Insights 💡**  
🔹 Product Category 1 dominates sales, indicating strong customer preference.  
🔹 Occupation significantly influences spending, with certain professions showing distinct spending behaviors.  
🔹 Men & married individuals tend to make larger purchases.  
🔹 Customers in City Category C exhibit the highest purchase amounts.  
🔹 Newcomers (0-1 years in the city) contribute significantly to sales, highlighting a key target demographic.  

📢 **Business Recommendation:**  

✅ Focus marketing efforts on high-spending occupations & City C residents.

✅ Promote top-selling Product Category 1 while improving others. 

✅ Offer targeted discounts & incentives for single & short-term residents to boost spending.  

## **🎯 Final Thoughts**  
This EDA reveals crucial insights into Black Friday shopping patterns! 📊. By leveraging these findings, businesses can optimize sales strategies, tailor marketing campaigns, and enhance customer engagement.


