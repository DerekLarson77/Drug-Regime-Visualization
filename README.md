Drug Regime Visualization

1) Two CSV files of data were merged together on Mouse ID.  The first file had characteristics about each Mouse ID.  
	The second file had various Timepoint data and Tumor Volume for each Mouse ID.
		a) Mouse_metadata.csv
		b) Study_results.csv

2) To clean the data the Mouse ID = "g989" was removed since it had multiple datapoints at the same Timepoints.

3) With the remaining 248 mice a group by was done on "Drug Regimen" to get the Mean, Median, Variance, Standard Deviation and SEM of each Regimen.

4) Two bar charts are displayed of the total count of Mouse ID for each Drug Regimen.  
	The data is identical, but one is completed using matplotlib, and the other is with pandas.

5) Two piecharts are displayed of the total count of Mouse ID for each Sex.  
	The data is identical, but one is completed using matplotlib, and the other is with pandas.

6) To obtain the Quartiles, Outliers and create Boxplots a group by on Mouse ID with maximum Timepoints was created.
	a) The max timepoints dataframe was merged with our clean dataframe to only view data at maximum timestamps.

	b) A function was created to receive the dataframe and dataframe column to calculate all of the quartiles, bounds and IQR.
		Then to return a small dataframe of only the outliers of the given data.

	c) A list of only 4 Drug Regimens (["Capomulin", "Ramicane", "Infubinol", "Ceftamin"]) was created.
		A for loop was used to append to an empty list to get the tumor volumes of each regimen.
		This list was used to create individual dataframes of each regimen and to concatinate a dataframe of all 4.
	
	d) Each individual regimen dataframe was input into the function that was created to print our stats for each Regimen.

	e) Each regimen dataframe was used again to build 4 ax boxplots in one figure to see outliers per the 4 Regimens.

7) Mouse ID = "f966" was selected to gather the tumor volumes at each timepoint and then plot a line graph.

8) A scatter plot was created for Average Tumor Volume vs Weight of only mice part of Capomulin.

9) The same scatter plot had a regression line calculated and displayed on the same graph.

	
