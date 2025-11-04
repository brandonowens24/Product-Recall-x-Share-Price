# Product-Recall-x-Share-Price

## Overview

This project aims to predict the immediate stock value change for automotive companies and suppliers after recalls are announced. This would be beneficial to automotive companies to understand how much value they may lose after a major announcement of product recall. By having this forecast, executives and board members can both brace for the impact from the stock market as well as simulate theoretical recalls to determine where the most beneficial enhancements should occur on the product line.

Additionally, there is benefit to the retail investor via prediction of what the stock may temporarily do. If the recall is announced and the market participant believes there is a discrepancy between the value of the asset and its current value, then it may be beneficial to adjust an investment strategy.


## Course Information
- **Course**: CSI-5170/CSI-4170
- **Instructor**: Dr. Mohammad Wardat
- **Semester**: Fall 2025

## Methods

We imported the recall dataset from https://catalog.data.gov/dataset/recalls-data. We cleaned and pre-processed the data, removing all instances where the recall year was before 1995, removing columns that do not contain valuable information for training, matching company names with the appropriate ticker symbol, fetching stock value opening and closing on the given day, and removing any samples that contain null values (either from the original dataset or because the appropraite ticker symbol was not found). 

We then tested a baseline model with linear regression. Isolating the number of people impacted by the recall with the change in stock value gave an r-squared of 0.0009.

We then investigated and implemented more complex models.

## To Run

