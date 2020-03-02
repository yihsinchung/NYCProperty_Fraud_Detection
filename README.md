# NYC Property Fraud Analysis

This project examines the 2010-2011 New York property dataset, which contains over one million property records in New York City. The

 and highlights abnormalities and potential fraud events in the dataset.


This report documented how we analyzed over one million NY property data with the goal of detecting anomalies. We first cleaned the data by filling in missing values, created 45 variables, and standardized these 45 fields. Afterwards, we reduced the dimensionality of the data by performing PCA. At the end, we chose the top 6 principle components for further analysis. The next step we did was to derive two fraud scores for each record using heuristic algorithm and autoencoder model. It turned out that the top ten records between the two analysis methods are highly overlapped.

The goal of this project is to detect anomalies and potentail fraud events by analyzing over one million New York property data within year 2010 and 2011. The following are the outline of what we did to accomplish the analysis. Please refer to the following link for a detailed report.

## 1. Explored the data and generated a Data Quality Report which documented exploratoy analysis and detailed description of the dataset.
	  Data Quality Report:

## 2. Cleaned data and filled in missing values
	  We only used the following fields in the dataset for our analysis:

	  notebook link:

## 3. Created 45 expert variables
	  To detect abnormalities efficiently, we needed further information beyond the original dataset. So, we created 45 variables according to the following method.
###   3.1 Create 3 size variables
          Lot Area (lotarea) = LTFRONT * LTDEPTH
          Building Area (bldarea) = BLDFRONT * BLDDEPTH
          Building Volume (bldvol) = bldarea * STORIES
###   3.2 Divide FULLVAL, AVLAND, and AVTOT by each size variables
	  	  After dividing FULLVAL, AVLAND, and AVTOT by every size variables created in the previous stage, we have a total of 9 variables, noted as r1 to r9.

## 4. Performed PCA to reduce dimensionality
	  After performing PCA to 45 expert variables, we chose the top 6 principle components (accounted for over 90% of the variance) for the remaining analysis.

## 5. Calculated fraud scores using Heuristic Function and an Autoencoder
###   5.1 Heuristic Function
###   5.2 Autoencoder

	  It turned out that the top ten records between the two analysis methods are highly overlapped.

## 6. Ranked all records using the weighted average of Score_1 and Score_2
	  Rank_final = Score_1*0.5 + Score_2*0.5
	  The following table shows the top 10 anomalous records based on Rank_final.

## 7. Investigation about these 10 records
      Through further investigation of these records, we concluded the following causes of abnormalities. 
      1.	Incorrect data inputs
      2.	Mortgage fraud 
      3.	Tax avoidance











