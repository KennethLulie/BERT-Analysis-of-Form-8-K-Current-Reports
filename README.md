# BERT-Analysis-of-Form-8-K-Current-Reports
Capstone Project for Masters in Data Analytics, Analysis of Form 8-Ks Current Reports including creation of dataset.

I have split the work logicially into different jupyter notebooks and have comments to help decipher any areas that are non-obvious.
If you have any questions or would like me to send you the data I have pulled please email me at Kenneth.Lulie@gmail.com.


This project was completed for the capstone project of the Master's in Data Analytics from UMUC. 
This project uses BERT to categorize Form 8-Ks, a report mandated by law when certain signficant events happen as a listed company,
as having either a positive, negative, or neutral impact on the stock price of the company that filed it.

For this project I wanted to challenge myself, so the project followed the full CRISP-DM process for data mining.  
Data was collected from the SEC EDGAR website in the form of 20,000 Form 8-K reports (most recent 40 from the current S&P 500 companies).
Then the stock history for each of these companies was collected from Yahoo Finance API going back for the entire time period (around 2012).
Additonally, the Key Statistics of these companies as reported on their 10-K and 10-Qs was pulled from another website.
These include numbers such as Assets, Liabilities, Current Ratio etc.

The project goes through the collection, processing, and merging of these datasets, as well as the use and evaluation of BERT's performance
to classify these datasets.

Additionally, the possibility of taking the numerical representation of the text as created by BERT, and combining it with additional information 
was explored i.e. the key statistics such as Assets.  
However, the large feature set produced by BERT (768) was too large to succesfully model within the time period of the project.

I intend to go back and explore the use of ALBERT which would produce a much smaller vector to represent the text, as well as other models
to evaluate the combined dataset to see if that would increase performance. 
