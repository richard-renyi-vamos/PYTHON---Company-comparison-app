CHATGPT CONVERSATION

**********

create a PYTHON code that compares 10 companies based on 10 different metrics
ChatGPT said:
Here’s a Python script that compares 10 companies based on 10 different metrics. It generates random data for demonstration, but you can replace it with real data. The script visualizes the comparison using a heatmap and bar charts. 🚀📊🐍

Compare Companies

Answer in chat instead
This script:

Creates a DataFrame with random performance scores for 10 companies across 10 metrics.
Prints the table with rounded values.
Displays a heatmap for easy visualization.
Generates bar charts for each metric to compare companies.
Let me know if you need modifications, like reading data from a file! 🚀📈

***********

import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Define companies and metrics
companies = [f"Company {i+1}" for i in range(10)]
metrics = [f"Metric {i+1}" for i in range(10)]

# Generate random performance scores (replace with real data if available)
data = np.random.rand(10, 10) * 100  # Random values between 0 and 100

# Create DataFrame
df = pd.DataFrame(data, index=companies, columns=metrics)

# Display the DataFrame
print("Company Comparison Table:")
print(df.round(2))

# Heatmap visualization
plt.figure(figsize=(12, 6))
sns.heatmap(df, annot=True, cmap="coolwarm", fmt=".2f", linewidths=0.5)
plt.title("Company Comparison Heatmap")
plt.xticks(rotation=45)
plt.yticks(rotation=0)
plt.show()

# Bar chart for each metric
for metric in metrics:
    plt.figure(figsize=(10, 4))
    sns.barplot(x=df.index, y=df[metric], palette="viridis")
    plt.title(f"Comparison based on {metric}")
    plt.xticks(rotation=45)
    plt.ylabel("Score")
    plt.show()
