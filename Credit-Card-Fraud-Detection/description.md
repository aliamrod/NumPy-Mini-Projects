## Introduction

Utilizing specific predictive models, we forecast credit card fraud in the transactional dataset in this project. In the following project, a wide range of Python libraries is exploited-- this includes Numpy (used to work with arrays + functions for working in domain of linear algebra, Fourier Transform, and matrics), pandas (facilitates working with datasets; functions for analyzing, cleaning, exploring, and manipulating data), seaborn (provides a high-level interface for drawing attractive and informative statistical graphics), matplotlib, etc.

I have worked with the two validation matrices-- recall matrix and precision matrix, using Numpy. 
 
 

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
