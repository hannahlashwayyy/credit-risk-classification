# credit-risk-classification

##Analysis Overview 

The purpose of this analysis was to look at users previous lending activity data for the sake of identifying a borrower's creditworthiness. There was a lot of significant data in our dataset, such as loan size, interest rate, total outstanding debt, the borrower's income and debt to income ratio, and additionally the loan status and if there were any derogatory marks associated with the borrower (i.e. do they have a previous history of being negligent with loan repayments, poor credit, etc). With this information, the goal was to build a model that predicted, and classified borrowers' loans as either 0: Healthy Loans or 1: High-Risk Loans. 

After doing a brief EDA with the dataset, I began working on building my Logistic Regression Model. First separating my labels and features; assigning 'loan_status' to y and all other columns to X. I then split my data into two sets - a training set and then a test set which would be used for actual predicting. I fit my model using the training data then made and saved my predictions. To visualize my model's performance I generated a Confusion Matrix and for additional information I printed the Classification Report.

##Results

* ML Model 1:
  * Accuracy: 99%
  
  * Precision: 
    * Class 0: 100%
    * Class 1: 87%
   
  * Recall:
    * Class 0: 100%
    * Class 1: 95%

   
##Summary 

Overall, the model has a 99% accuracy in predicting whether a loan is healthy or high-risk. If you look at just that number, you'd think we have pretty solid model but in my opinion that isn't the case. For starters, we are dealing with a dataset that is incredibly imbalanced - during a brief EDA of the dataset, it was discovered that only 3% of dataset has a high-risk loan status. This explains the discrepancy in predicition between healthy and high loans - of course the model is going to be great at predicting healthy loans - it was trained with data that was comprised of mostly healthy loans, so a 100% accuracy prediction is not a shock at all. The problem, is that with a lack of high-risk loan data, our model isn't great with identifying and predicitng those types of loans. In all fairness, an 87% accuracy isn't terrible BUT if you're a bank or some kind of credit-lender accurate predictions on high-risk loans are infinitely more important to you because that's were you're more likely going to loose money! The only true postive I can point too in this models prediction ability regarding high-risk loans is that we do have a 95% recall, which is promising, even if it can't accurately _predict_ high-risk loans at a satisfactory level, at least it can _identify_ them. In my opinion, I would not implement this model in a real-world setting, but what I would do is train it with more high-risk loan data to eliminate some of the imbalance in the dataset and hopefully improve the model's ability to predict high-risk loans accurately. 

