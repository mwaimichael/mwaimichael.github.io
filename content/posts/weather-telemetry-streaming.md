---
title: "Real-Time Weather Telemetry Streaming Pipeline"
date: 2026-05-15
draft: false
tags: ["Apache Kafka", "Python", "Tkinter", "ETL"]
summary: "An end-to-end data pipeline streaming real-time weather metrics through a containerized Kafka cluster to a custom analytical GUI dashboard."
---

### General Overview
The aim of this project is to develop a Multiple Linear Regression Model to accurately predict the sale prices of houses in King County. Through careful data analysis and exploratory data analysis techniques, we will preprocess and clean the dataset to create a data frame for regression modeling. By analyzing key features such as square footage, number of bedrooms, location(waterfront or not), and more, we aim to uncover valuable insights that influence house prices.


### 🏗️ Architecture Overview
Instead of just writing script files, this project builds a robust event streaming application that pulls weather status data directly from regional APIs using city-name queries and routes it through an event broker.

```text
[Weather API] ──> [Kafka Producer (Python)] ──> [Kafka Broker] ──> [Kafka Consumer] ──> [Tkinter GUI]
```


```python
producer.send('weather-telemetry', value=json.dumps(weather_payload).encode('utf-8'))
```

## Run the Project
To run the project, run the following code on the main.py file.
```python
# Run this cell without changes

# Set up plots
fig, (ax1, ax2) = plt.subplots(ncols=2, figsize=(16, 5))

# Create variables for easier reuse
value_counts = heroes_df["Publisher"].value_counts()
top_5_counts = value_counts.iloc[:5]

# Plot data
ax1.bar(value_counts.index, value_counts.values)
ax2.bar(top_5_counts.index, top_5_counts.values)

# Customize appearance
ax1.tick_params(axis="x", labelrotation=90)
ax2.tick_params(axis="x", labelrotation=45)
ax1.set_ylabel("Count of Superheroes")
ax2.set_ylabel("Count of Superheroes")
ax1.set_title("Distribution of Superheroes by Publisher")
ax2.set_title("Top 5 Publishers by Count of Superheroes");
```
