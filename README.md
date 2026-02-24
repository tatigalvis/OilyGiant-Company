🛢️ OilyGiant – Oil Well Location Optimization
📌 Project Overview

You work for OilyGiant Mining Company, and your task is to identify the best region to develop new oil wells.

Using historical data from three regions, this project builds a machine learning model to:

Predict the volume of oil reserves in new wells

Estimate potential profit

Analyze financial risks using the Bootstrapping technique

Select the region with the highest expected profit and acceptable risk level

The final recommendation is based on profitability, confidence intervals, and probability of losses.

📂 Dataset Description

The dataset contains oil samples from three different regions.

Each dataset includes:

id – unique well identifier

f0, f1, f2 – geological features

product – volume of reserves (target variable)

The objective is to predict product and determine which region maximizes profit.

🔍 Project Workflow
1️⃣ Data Preparation

Loaded datasets for three regions

Checked for missing values and duplicates

Verified data types

Removed non-informative columns (e.g., id)

Defined features and target variables

2️⃣ Model Training and Validation

For each region, the following steps were performed:

2.1 Data Splitting

Split into 75% training and 25% validation

Used a fixed random_state for reproducibility

2.2 Model Training

Trained a Linear Regression model

Generated predictions for validation data

2.3 Performance Metrics

Saved:

Predictions

True target values

Evaluated:

Average predicted reserves

RMSE (Root Mean Squared Error)

2.4 Model Evaluation

Compared regions based on:

Prediction accuracy

Stability of predictions

Average reserve volume

💰 Profit Calculation Preparation
Key Business Assumptions

Budget for 200 wells development

Revenue per thousand barrels

Total investment budget

All key financial parameters were stored in separate variables.

Break-even Analysis

Calculated the minimum volume of reserves required for a well to be profitable:

Break-even volume
=
Budget
Revenue per unit
Break-even volume=
Revenue per unit
Budget
	​


Then compared this threshold with the average predicted reserves in each region.

Findings:

Some regions showed higher average reserves but also higher uncertainty.

Others were more stable but slightly lower in volume.

📈 Profit Calculation Function

A custom function was created to:

Select the top 200 wells with highest predicted reserves

Sum actual reserve volumes for those wells

Calculate total revenue

Subtract development budget

Return final profit

This allowed objective comparison between regions.

🔁 Risk Analysis – Bootstrapping

To evaluate uncertainty and financial risk:

Used Bootstrapping with 1000 samples

Sample size: 500 wells per iteration

Selected top 200 wells per sample

Calculated profit distribution

For each region, computed:

✅ Average profit

✅ 95% Confidence Interval

✅ Probability of loss (negative profit)

Loss probability was expressed as a percentage.

📊 Results Summary
Region	Avg Profit	95% CI	Risk of Loss
Region 1	...	...	...
Region 2	...	...	...
Region 3	...	...	...

(Replace with your actual results)

🏆 Final Recommendation

Based on:

Highest average profit

Acceptable 95% confidence interval

Loss probability below risk threshold

👉 Recommended Region: Region X

This region provides the best balance between profitability and financial risk.

🛠️ Technologies Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib

Bootstrapping (resampling method)

📈 Skills Demonstrated

Regression Modeling

Model Evaluation (RMSE)

Business Metric Translation

Risk Analysis

Bootstrapping Simulation

Financial Decision Modeling

Data-Driven Decision Making
