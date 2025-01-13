BANCA DATA SCIENTIST CHALLENGE</br>
BANCA is a division specializing in providing insurance services with many
attractive policies. Currently the company is looking to promote incentive for a special
kind of healthcare insurance called MANU policy. In this challenge, I am going to
help the division manager to understand their customer by supporting him to identify
which customer is willing to possess the policy, so he can make an efficient sales
campaign.
TASKS
1) Prediction task: The objective of this task is to construct a model that predicts whether
a customer will buy a MANU policy or not. You are also provided a test set (file
test_data.txt below) of 4000 instances who were likely to have the policy. Please filter out
the most 800 highly promising cases that want to buy the mentioned policy. We will use
the hold out label set to verify your results, the label is not provided to you, so the more
cases that really want to buy a MANU policy you can detect, the better the model you
built. The output of this task is a file that contains 800 lines, each line is the ID of a
customer. Please explain techniques how you monitor the model to ensure the output with
high reliability.
2) Explanation task: The objective of this task is to provide insight into why customers
have a MANU policy, what are the characteristics and portrait of these customers. The
explanation and accompanying interpretation should be scored on comprehensibility,
usefulness and actionability to effectively support the manager in making his sales
campaign.
DATASET DESCRIPTION
1) train_data.txt:
You will use this dataset to train and validate your prediction models. Each row of this
file consists of 86 attributes including sociodemographic (attributes 1-42) and product
ownership (attributes 43-85), the attribute 86 is the target variable or label (possessing a
MANU policy or not) and ID of each customer (identical with the line number of the
row). The sociodemographic data is derived from zip codes. All customers living in areas
with the same zip code have the same socio-demographic attributes
2) test_data.txt:
This dataset is for predictions. It has the same format as train_data.txt, except that the
target variable is missing.
3) attributes_description.pdf:
This file contains the description of each attribute in detail.
