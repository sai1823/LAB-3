# LAB-3
Map in Python


We first read in the India shapefile and state capitals data from the provided file paths using GeoPandas' read_file() function. 
We then merge the two dataframes based on the state names using the merge() method.
Since the population column in the state capitals data is read in as a string, we convert it to a numeric type using pd.to_numeric() function from pandas.
Finally, we plot the merged data as a bubble map using the plot() method in GeoPandas. 
The column parameter is set to 'Population' to use the population data in the state capitals data for the bubble sizes. 
The legend_kwds parameter is used to set the label for the legend. 
The cmap parameter is used to set the color map for the bubbles, and the edgecolor parameter is used to set the color of the borders of the state polygons. 
The alpha parameter sets the transparency level of the bubbles to 50%. 
The markersize parameter is set to the population divided by 50,000 to scale the size of the bubbles based on population.
Finally, the set_axis_off() method is called to remove the axis labels and ticks from the plot.

In the connection graph code reads in the "Flightschedule.csv" file into a pandas dataframe, creates a geodataframe of the Indian states using a shapefile, filters the flights dataframe to only include Go Air domestic flights in India, merges the flights dataframe with the states geodataframe based on the state name, and finally plots the connection graph of Go Air domestic flights in India using geopandas.

