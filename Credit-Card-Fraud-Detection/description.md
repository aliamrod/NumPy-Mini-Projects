## Introduction

In this 

![image](https://github.com/user-attachments/assets/43439fb3-7c0b-48c4-bc33-4ca1529cc2c7)

Credit card fraud is a form of identity fraud/theft. It happens when an unauthorized transaction is made using a credit card without explicit permission from the cardholder. There are various ways card fraud can be conducted...

Fraudsters can get discarded receipts or credit card statements that include your account number and use that information to rack up fraudulent charges.
Credit card info can be leaked during an online transaction, and then unauthorized purchases can be conducted using this information.
Credit card information can be stolen using a card skimmer installed at ATMs
Card fraud is a big problem for card issuers and banks as it accounts for a substantial chunk of revenue loss. As per Annual Fraud Statistics Released by The Nilson Report, fraud losses reached USD 27.8 billion in 2019 and expect to go up to USD 35.67 billion in the next five years.


## Objective

To implement proactive monitoring, prevention mechanisms, reduce time-consuming manual reviews and human errors, this project aims to build and train



 

## Dataset

* Dataset contains credit card transactions done by European cardholders in 2013 for two days

* There are 284,807 total transactions

* 492 transactions are fraudulent

* The positive class (frauds) are only 0.172%

* Dataset has 31 features, 30 independent and one dependent column.

* Due to confidentiality reasons, 28 out of 30 independent features are transformed to numerical values using PCA. The remaining two features, time and amount, are left intact.

* Fraudulent transactions are marked as 1 (Positive class), and genuine transactions are marked as 0 (negative class)


## Evaluation Criteria

* `roc_auc` will be used as the primary metric for model evaluation and performance comparison.
* We will also monitor the `precision` and `recall` for each of the models we build as they can give valuable insigns for different use-cases. 


## Precision, Recall Matrices

Both precision and recall are crucial for information retrieval, where positive class matters the most as compared to negative. _Why is that?_

While searching something on the web, the model does not care about something **irrelevant** and **not retrieved** (this is the true negative case). Therefore, only TP, FP, FN are used in precision and recall. 

#### Precision

Out of all the positive cases predicted, what percentage is *truly positive. 

![image](https://github.com/user-attachments/assets/6c87aa0b-a1c9-4bcb-a3b5-83fbef5f5e8e)



#### Recall

Out of all the positive cases reported, what percentage are predicted positive. It is the same as TPR (true positive rate). 

![image](https://github.com/user-attachments/assets/953a7354-d8fc-45b4-8899-935670334ae4)



![image](https://github.com/user-attachments/assets/745d9094-03c0-48e8-bac9-8319c28d942f)

In this case, we do not want to miss any fraud transactions. Therefore, we want False-Negative to be as low as possible. In these situations, we can compromise with the low precision, but recall should be high. Similarly, in the medical application, we don't want to miss any patient possibly. Therefore, we focus on having a high recall. 
