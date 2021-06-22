# Financial Fraud Detection with Machine Learning, EDA and Visualisation

## Technologies used for analysis:
- Python
- Supervised Machine Learning
- SQL
- Power BI

Financial fraud is increasing every year with the rise of new technologies and the use of mobile phones. In 2020, $32.9 billion worth of financial fraud was committed, and this is expected to rise to $40.63 billion by 2027. On the other hand, there are about 5.19 billion mobile phone users, this has had a steady growth of 2.4% over 2019, but, in the number of chips or phone numbers on average is almost 8 billion.

Based on this data, I decided to conduct a financial fraud analysis. I found a mobile-focused financial fraud dataset with more than 6 million records. With this information, I felt I had enough data to be able to analyse and train machine learning models to try to predict fraud cases versus genuine ones.

I did an exploratory analysis in search of insights and to see how the variables were related, from the formatting of the data with pandas to the visualisation in plots with different python libraries such as seaborn or matplotlib.

I came to the conclusion that the frauds that were being committed were only with two types of transactions: Transfers and Cash Out. Therefore, I decided to focus on both. 

Once I had analysed the data and found the relationships between the variables, I considered doing Feature-engineering in order for the machine to better understand the algorithms for further training with Machine Learning to predict fraud.



I trained 5 Machine Learning models and obtained the following results in terms of model classification accuracy:

- Logistic Regression: 0.996995029616555
- KNN: 0.9989911240574499
- Random Forest: 0.999980147342812
- SGD: 0.9725221176648944
- XGBClassifier: 0.9999837569168463
- DecisionTreeClassifier: 0.9999693186207096

At this point, with the results obtained, I decided to train the best model separately: XGBClassifier 99.9983%.

When training the models, I used only a part of the data in order to be able to predict with the rest of the unused data and not overfit the model in the first instance. (Train Test Split).

The viability of the model is tested: Only the prediction of whether it is fraud or genuine fails 9 times out of 500,000 data.

To improve the model, the model is trained with the full set of data from the Transfers and Cash Out DataFrame (only operations where we have detected fraud). With this action the model improves to 99.9989%, with an error of 30 predictions out of 3 million.

I created the model, imported the dataset into a mySQL database and created the excel files needed to visualise all the insights through the Power BI visualisation tool.


This project has been very satisfying for me, as I have been able to test all the tools I have learnt in IRONHACK. 
