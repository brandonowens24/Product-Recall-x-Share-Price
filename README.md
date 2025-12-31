# Product-Recall-x-Share-Price

## Overview

This project aims to predict the immediate stock value change for automotive companies and suppliers after recalls are announced. This would be beneficial to automotive companies to understand how much value they may lose after a major announcement of product recall. By having this forecast, executives and board members can both brace for the impact from the stock market as well as simulate theoretical recalls to determine where the most beneficial enhancements should occur on the product line.

Additionally, there is benefit to the retail investor via prediction of what the stock may temporarily do. If the recall is announced and the market participant believes there is a discrepancy between the value of the asset and its current value, then it may be beneficial to adjust an investment strategy.


## Course Information
- **Course**: CSI-5170/CSI-4170
- **Instructor**: Dr. Mohammad Wardat
- **Semester**: Fall 2025

## Methods and Results

We imported the recall dataset from https://catalog.data.gov/dataset/recalls-data. We cleaned and pre-processed the data, removing all instances where the recall year was before 1995, removing columns that do not contain valuable information for training, creating a manual ticker map to match company names with the appropriate ticker symbol, fetching historical stock prices, and removing any samples that contain null values (either from the original dataset or because the appropriate ticker symbol was not found). 

We then tested a baseline model, the "null model", with linear regression. Isolating the number of people impacted by the recall with the change in stock value gave an r-squared of 0.0009.

We then investigated and implemented more complex models, including a decision tree classifier to determine the directionality of the stock value, a random forest regression model, and a custom ensemble model to make use of the polynomial regression model and the decision tree classifier. The additional regression models did not significantly improve the r-squared value. However, the directionality improved from 50.1% to 54.2%. 

To expand on this work, an isolated dataset for a specific automotive company may reduce some of the noise that the model was trained on. There is room for improvement in regard to feature extraction, whether that be making use of an LLM analyzing the severity of a recall based off of the recall description and using that metric in the training or obtaining data from additional sources such as the age of the product recalled and if the recall resulted in a lawsuit. Additionally, a time series analysis would be better suited for this dataset but was beyond the scope of the class. 

