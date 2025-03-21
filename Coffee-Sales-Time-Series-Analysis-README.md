#☕ Coffee Sales Analysis 📊

Welcome to the Coffee Sales Analysis project! In this analysis, we explore the daily sales performance of two coffee machines, using data manipulation, cleaning, and visualization techniques. The goal is to compare the sales trends of the two machines and gain valuable insights into their performance over time.

#🔍 Project Overview

This project involves the following steps:

#Data Loading 📥:

The raw CSV files containing sales data from two coffee machines are loaded into Pandas DataFrames.

#Data Cleaning 🧹:

The datetime column is converted into proper datetime objects, and set as the index for time-based analysis.
Missing values in the 'card' column of Machine 1 data are filled with "NA" for consistency.

#Resampling ⏳:

The data is resampled to a daily frequency, aggregating sales ('money') for each day to identify overall sales patterns.
Data Merging 🔗:

The daily sales of Machine 1 and Machine 2 are combined into a single DataFrame to facilitate easy comparison.

#Visualization 📈:

A Plotly interactive line chart is created to visually compare the daily sales of both machines. Hover functionality allows users to see exact sales values for each date.

#📚 Key Libraries Used

Pandas: For data manipulation and cleaning 🧑‍💻.

Matplotlib: For basic plotting (though Plotly takes center stage here) .

Plotly: For interactive, visually engaging charts 🎨.

#🖼️ Output

The final output is an interactive line chart that displays the combined daily sales for both machines.

Hover over the data points to see details such as the exact sales value for each date.
The chart allows for easy comparison of the sales performance between Machine 1 and Machine 2.
⚙️ Requirements
To run the code, you’ll need the following Python libraries:

pandas

matplotlib

plotly

You can install the required libraries with pip:

bash

Copy

Edit

pip install pandas matplotlib plotly

#📅 Dataset
The dataset used in this project contains two CSV files, one for each coffee machine, with the following columns:

datetime: The timestamp of the transaction ⏰.

money: The amount of money earned from the sale 💸.

card: The type of card used for payment 💳.

#🚀 Future Enhancements

Predictive Analytics 🔮: Use machine learning to predict future sales based on trends.

Detailed Insights 🧐: Add more granular analysis, such as peak sales times, customer preferences, or regional performance (if available).

Automated Reports 📑: Generate automated reports and dashboards for business stakeholders.

Here's a snap of our Time Series Line Chart-
![Image](https://github.com/user-attachments/assets/6d1d0d23-e165-458d-814d-9b4b3a1b43fe)

You can hover the cursor over each point to get it's value. 

#Coffee Sales Analysis
displaying Coffee-Sales-Time-Series-Analysis-README.md
