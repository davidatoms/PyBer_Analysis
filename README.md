# PyBer Analysis
###### Written by: David Adams
###### Written on: February 3, 2021

###### Module 5

### Overview of the Analysis:
PyBer, and the CEO, asked me to analyze specific data from different cities and present the findings. By using Python, MATPLOTLIB, and Jupyter Notebook, I was able to create easy-to-understand scatter plots and graphs that place a lot of data in a visually-appealing way. Using these tools to visualize data can help understand the business on a large scale and even cut the data down to a smaller scale. For example, we can compare business data in the urban, suburban, and rural city types or we can focus on one city and compare the functions of the business. 

The dataframe was compiled by city data and ride data. Each have a specific city that allowed me to connected the two CSVs together. By doing so, we can see two sides of the business--the user-side and the producer-side (PyBer's side).

The process was to first import the Matplotlib and import the dependencies. I then had to get the data for the analysis. After that, the data needed to be prepped and groomed in order to present the data with the visualization tools. 

When this data is shown in graphs, charts, tables, etc, it can be seen from a distance and the viewer can get a bigger picture of what is happening. In data science, I believe that creating these dataframes and then inputting actions by a CEO or the management team to increase revenue, or account for external factors like a pandemic, could be the beginning to a better-performing company with evidence of data.

### Results of the Analysis:
The number one deliverable was to find the total rides for each city type. I took that to mean finding the total ride counts for each city. See the total rides for each urban city. This data can be passed down to those in charge of those cities and even narrow down the business specifics in a certain city. 

```
# Get the total rides for each urban city
urban_ride_count_by_city = urban_cities_df.groupby(["city"]).count()["ride_id"]
urban_ride_count_by_city.head()
```

After reviewing the code, I realized that I needed to find the count for each type of city. I reviewed Module 5 and found that I could calculate the total rides for each city type by the code written below:

```
# Get the total rides for each city type
ride_count_by_type = pyber_data_df.groupby(["type"]).count()["ride_id"]
ride_count_by_type
```

This printed out the total rides for each city type by summing the rides from each city within a certain city. Now that I have both, I could deepen the analysis for the CEO by comparing the total rides within a city to the total of rides for that city type. This can be on hand if the CEO asks or used in another way to test business practices in a certain area. It can also be presented to area managers or city managers depending on how PyBer is strucutured.

Lastly, the chart shows the first quarter plus one month by rides in certain cities. Comparing city types and the fare it brings can allow us to understand where the business opportunity is hot and how customers are using PyBer. 

![PyBer Q1 Analysis by City Type](/Resources/PyBer_Challenge.png)

### Summary of the Analysis:
Urban cities had the greatest fares. It remained steady throughout the first quarter. There were 1625 rides in the given time. This shows that the multiple of rides is what increases the fare amount. In order to test this hypothesis, I would need to further test the number of rides to the city type and see if there is a correlation coeffiecient close to 1. This would show a strong relationship between the number of rides and the fare amount received.

Suburban and rural rides were significant less. I believe that the number of miles to travel is a significant factor in traveling with PyBer. In a further study, I would like to compare an external data source for people owning cars in urban, suburban, and rural areas. By doing so, I believe i can see a relationship between the demand for using PyBer's service.

This challenge is the beginning of understanding the data for PyBer on a macro-level. In order to increase my usefulness at PyBer, I would recommend a further study to analyze more data to better understand PyBer's business and the story the data tells. By doing so, I can present it to the CEO or other key founders and brainstorm different decisions that could increase revenues and business possibilities.
