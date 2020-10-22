<p align="center">
  <img width="948" height="250" src="https://github.com/leslievazquez/The_Power_of_Plots/blob/main/Pymaceuticals/Resources/big_data_concept.jpg">
</p>

<h1 align ="center"><span>The Power of Plots</span></h1> 
 
*What fun would data be without a story to tell?*

The purpose of this data analysis is to demonstrate different plots that can be created through pandas and Matplotlib based on the following scenario: 

>	The company, Pymaceuticals, Inc. specializes on developing pharmaceuticals to treat cancer. Pymaceuticals began screening potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. The company recently conducted an animal study to compare the performance of their drug of interest, Capomulin, versus the other treatment regimens. Pymaceuticals’ executive team requested an analysis of the data collected from the animal study. 

Two .csv files were provided for this data analysis: `Mouse_metadata.csv` and `Study_results.csv`. Both files were combined using the `pd.merge()` method. 

There was one mouse identified (‘g989’) that had duplicate timepoints in the data. This mouse ID was expelled from the combined data, and it was not included in the analysis. A total of 248 mice were used. 

A summary statistics table was generated to calculate the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen. 

This data analysis contains plots that appear to be duplicates. However, they were created using both pandas’ `DataFrame.plot()` and Matplotlib’s `pyplot()`.
-	The bar plots show the number of total mice used for each treatment regimen throughout the course of the study. 
-	The pie plots show the gender distribution of the mice used in this study. 

A list was created to analyze the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. The quartiles and IQR were calculated, and the outliers were identified. 

A box and whisker plot of the final tumor volume for all four treatment regimens was generated using Matplotlib. A marker was included in this plot to highlight the outlier(s). 

A code was generated to randomly select a mouse that has been treated with Capomulin. For this analysis, Mouse ID ‘j119’ was randomly selected using the `.sample()` method. A line plot of the tumor volume vs. timepoint was created for Mouse ID ‘j119’. Also, a scatter plot of the mouse’s weight vs the average tumor volume was created. 

Lastly, the correlation coefficient and linear regression model between the mouse’s weight and tumor volume for the Capomulin treatment was calculated. The final plot demonstrates the results of this calculation by recreating the previous scatter plot and placing the linear regression model on top of it. 

#### Analysis
- The animal study had a sample of 249 mice (124 females and 125 males). One mouse had duplicate data; thus, it was expelled. The data analysis was performed from the data collected from 248 mice. The gender distribution for this study was 50.4% male and 49.6% female. 
- Overall, there were 10 treatment regimens used for the animal study. However, four of these (Capomulin, Ceftamin, Infubinol, and Ramicane) were identified as promising treatments.
- The average tumor volumes were significantly low for the mice treated with Capomulin and Ramicane, indicating that these two treatments where the most effective in reducing the size of the tumors of the mice. 
- For the Final Tumor Volume per Drug Regimen, there was one outlier identified in the box plot for Infubinol. 
- The correlation between mouse weight, and average tumor volume is 0.84. This number is considered a strong positive correlation which indicates that when the mouse weight increases the average tumor volume also increases. 

*Additional information and the plots generated for this analysis are in the folder "Pymaceuticals" within this repository.*
