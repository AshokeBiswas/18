Q1. Load the flight price dataset and examine its dimensions. How many rows and columns does the dataset have?
To determine the dimensions of the dataset (number of rows and columns), we'll load the dataset and inspect it programmatically.

python
Copy code
import pandas as pd

# Assuming the dataset is named 'flight_price.csv' and is loaded into a DataFrame 'flight_data'
flight_data = pd.read_csv('flight_price.csv')

# Check the dimensions
rows, cols = flight_data.shape
print(f"The dataset has {rows} rows and {cols} columns.")
Q2. What is the distribution of flight prices in the dataset? Create a histogram to visualize the distribution.
python
Copy code
import matplotlib.pyplot as plt

# Create a histogram to visualize the distribution of flight prices
plt.figure(figsize=(10, 6))
plt.hist(flight_data['Price'], bins=20, edgecolor='black')
plt.xlabel('Price')
plt.ylabel('Frequency')
plt.title('Distribution of Flight Prices')
plt.show()
Q3. What is the range of prices in the dataset? What is the minimum and maximum price?
python
Copy code
# Calculate range, minimum, and maximum prices
price_min = flight_data['Price'].min()
price_max = flight_data['Price'].max()
price_range = price_max - price_min

print(f"Minimum Price: {price_min}")
print(f"Maximum Price: {price_max}")
print(f"Price Range: {price_range}")
Q4. How does the price of flights vary by airline? Create a boxplot to compare the prices of different airlines.
python
Copy code
import seaborn as sns

# Create a boxplot to compare flight prices by airline
plt.figure(figsize=(12, 8))
sns.boxplot(x='Airline', y='Price', data=flight_data)
plt.xticks(rotation=45)
plt.xlabel('Airline')
plt.ylabel('Price')
plt.title('Flight Prices by Airline')
plt.show()
Q5. Are there any outliers in the dataset? Identify any potential outliers using a boxplot and describe how they may impact your analysis.
python
Copy code
# Identify potential outliers using a boxplot
plt.figure(figsize=(8, 6))
sns.boxplot(x=flight_data['Price'])
plt.xlabel('Price')
plt.title('Identifying Outliers in Flight Prices')
plt.show()
Outliers are values that are significantly higher or lower than other data points. They can skew statistical analyses, affecting measures like the mean and standard deviation. Addressing outliers involves deciding whether to remove them, transform them, or analyze them separately depending on their impact and the analysis goals.

Q6. You are working for a travel agency, and your boss has asked you to analyze the Flight Price dataset to identify the peak travel season. What features would you analyze to identify the peak season, and how would you present your findings to your boss?
To identify the peak travel season, analyze features such as:

Date/Time: Look at flight prices over different months or seasons.
Destination: Prices may vary based on popular travel times for specific destinations.
Holiday or Event Data: Check if prices spike around holidays or events.
Present findings with visualizations like line plots showing price trends over time or bar plots comparing prices across months or seasons.

Q7. You are a data analyst for a flight booking website, and you have been asked to analyze the Flight Price dataset to identify any trends in flight prices. What features would you analyze to identify these trends, and what visualizations would you use to present your findings to your team?
Analyze features such as:

Time Trends: Analyze how prices change over time (months, years).
Route Analysis: Compare prices for different routes or destinations.
Airline Analysis: Investigate how prices vary among different airlines.
Visualize trends using line plots, heatmaps, or scatter plots to show correlations between variables and identify patterns in flight prices.

Q8. You are a data scientist working for an airline company, and you have been asked to analyze the Flight Price dataset to identify the factors that affect flight prices. What features would you analyze to identify these factors, and how would you present your findings to the management team?
Analyze features such as:

Airline: Compare prices across different airlines.
Route/Distance: Analyze prices based on flight distance or specific routes.
Time Factors: Explore how prices vary by time of day, day of the week, or season.
Present findings using statistical summaries, regression models, or interactive dashboards to highlight factors influencing flight prices and provide actionable insights for pricing strategies.

These steps provide a comprehensive approach to analyzing and presenting insights from the Flight Price dataset across various scenarios and stakeholder needs.






