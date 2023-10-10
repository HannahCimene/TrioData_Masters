# Discussion topics part 3

## The AWS-lesson

1. You want to detect fraud in future transactions. You can work with 1.000.000 past transactions of which 2.53% is labeled as fraudulent. Which problem will you be facing?
The model will be high fitting, this could be solved with a smaller dataset with a higher percentage fraudulent transactions.

1. Could I use an Amazon S3 bucket as a sort of google drive for my personal files?
S3 is made for storage and retrieval of your files, whereas google drive is more fit for personal use. Google drive is better for consumers and people who want to be able to collaberate.

1. Give some pros and cons for Amazon FSx.
Pro's:
    - scalable
    - compatible (windows)
    - fully managed (AWS)
    - integration with AWS services
Con's:
    - pricy
    - availability (not every region)

1. Give some pros and cons for Amazon EFS.
Amazon EFS is very similar to Amazon FSx, with the important difference that FSx is compatible with Linux whereas EFS is made for UNIX and LINUX.

1. What is Amazon RDS?
Amazon RDS is a fully managed relational database. It provides a scalable, highly available, and fully managed database infrastructure for popular relational database management systems (RDBMS) such as MySQL, PostgreSQL, Oracle Database, Microsoft SQL Server, and MariaDB.

1. What is Amazon Redshift?
Amazon Redshift is a fully managed data warehouse service that allow you to analyze large datasets. Amazon Redshift looks and feels like Amazon Athena. The big differences are Redshift needs a server and is pay-per-hour and Athena is serverless with a pay-as-you-go policy. 

1. What would a usecase for Amazon Timestream be?
A financial services company can use Timestream to analyze near real-time financial market data. This data can be used to make investment decisions and to manage risk.

1. What is the service that amazon uses to keep data safe - i.e. that not anybody can access it? (IAM)
AM (Identity and Access Management): IAM allows you to manage user identities, roles, and permissions for AWS services and resources. You can control who can access your AWS resources and what actions they can perform.

1. What is CloudTrail?
CloudTrail is used to monitor and log the API's of an application. It can also be used to track user activity, troubleshoot issues, and meet compliance requirements.

1. Explain: feature selection, feature extraction and feature creation.
Feature selection is the process of selecting a subset of features from the original set of features. This is done to improve the performance of machine learning models by reducing the dimensionality of the data and removing redundant or irrelevant features.
Feature extraction is the process of creating new features from the original features. This can be done to improve the performance of machine learning models by creating features that are more informative or predictive.
Feature creation is the process of creating new features that are not present in the original dataset. This can be done to improve the performance of machine learning models by creating features that are more informative or predictive.

1. Why can't we just encode blue as 1 and red as 2? Then what should we do?
This is because the color name red doesn't have a greater value then the color blue. We should use one-hot encoding instead.

1. When doing feature selection, you might use wrapper methods or filter methods. What are the [dis]advantages of both?
Filter methods have high computational efficiency and does not depend on a specific model, but has limited feature interaction and is suboptimal for prediction.
Wrapper methods are model specific and can be fine-tuned, but have high computational cost and are suspect to overfitting

1. Explain the different sets in which you split your data. (Train, test, validation.)
Train set: The train set is the largest set of data and is used to train the model. The model will learn the patterns in the train data and use this knowledge to make predictions on new data. (80%)
Validation set: The validation set is used to evaluate the performance of the model on data that it has not seen before. This helps to prevent overfitting, which is when the model learns the train data too well and is unable to generalize to new data. (10%)
Test set: The test set is the smallest set of data and is used to evaluate the final performance of the model on data that it has never seen before. This gives an unbiased estimate of the model's performance on real-world data.(10%)

1. What is K-fold cross validation and when is it used?
K-fold cross validation is a resampling procedure used to evaluate machine learning models on a limited data sample. It works by dividing the data into k subsets and then training and evaluating the model on each subset. The performance of the model is then averaged over the k subsets. This is used for smaller datasets.

1. Why do we need to randomize data before splitting it in different sets?
We randomize the data to make sure the data is not grouped. If we don't this, the testing data for example could contain all the same values or all really low values and the training data will lack these low values. Thus resulting in a worse model.

1. What is deploying a model? How do you go about it in AWS?
    - Package your model: package in a format that can be deployed to AWS (tools: Amazon SageMaker, TensorFlow Serving or PyTorch)
    - Deploy your model: deploy it to AWS (tools: Amazon SageMaker, Amazon Elastic Compute Cloud (EC2), or Amazon Elastic Kubernetes Service (EKS))
    - Configure your model: configure it to accept requests from users and return predictions (tools: Amazon API Gateway, Amazon Elastic Load Balancing, and Amazon Route 53)
    - Monitor your model: monitor its performance to ensure that it is working as expected (tools: Amazon CloudWatch and Amazon SageMaker Model Monitor)

1. Draw and explain a basic confusion matrix.
A confusion matrix is a fundamental tool for evaluating the performance of a classification model in machine learning. It provides a tabular representation of the model's predictions compared to the actual true values in a classification problem.
<img src="Files/img/MicrosoftTeams-image (6).png" align="left"
     height="150" style="margin-right: 1.5rem">

1. Draw and explain a basic ROC-curve.


1. In the sagemaker labs, you see the function below. Why the 65%? Why not 50%?



![](files/2023-06-14-10-47-05.png)


## The powerpoint and exercises

1. What is the difference in the type of problems XGBoost and Random Forest can cope with?
1. Explain XGBoost.
1. Explain the linear learner we can find on AWS.
1. Explain the K-means algorithm we can find on AWS.
1. Explain the 3-set split in data sets.
1. "The validation data set as well as the testing set, should follow the same probability distribution as the training data set." Explain.
1. Draw a confusion matrix for a binary classifier, and another for a multiclass classifier.
1. Sensitivity and specificity: explain, and give an example for when they would be better high.
1. Explain thresholds in the context of sensitivity and specificity.
1. Describe the best and the worst possible models based on their ROC curves.
1. How would you calculate the AUC-ROC? How is it used?
