# Automatically Upload files to AWS S3 buckets

You'll learn to Automatically upload to AWS S3 bucket with just few simple steps
This is just a beginner friendly project

## Prerequisites
* AWS Account with *Administrative priveleges*
* Above uploaded `.yaml` file

### 1 Create IAM User
Go the the AWS Management Console and create IAM User that will specifically upload from Github to AWS S3.
Give this user Programmatic access
* Attach the Existing IAM Policies: S3FullAccess

### 2 Create S3 Bucket
Create S3 bucket in AWS 

### 3 Copy code from `.yaml` file
`.yaml` file is present in  **demo>views.yaml** 
copy the code as it is and paste in your `.yaml` file
This is all you need to perform the needful

### 4 Create an HTML file
Let's create an HTML file, in my case, I created `main.html`
When we'll upload to github. this `.html` file will get uploaded to S3 bucket

### 5 Set-up Secrets for Github
For performing this Automation, we need to add some secrets to Github, so that it will upload to S3
Go to **settings> secrets> new repository secrets**

Let's quickly add secrets
You require S3 Bucket name, IAM User's Access Key ans Secret Access key

```
Name: AWS_S3_BUCKET
Value: put your S3 bucket's name
```

```
Name:  AWS_ACCESS_KEY_ID
Value: copy value of Access key id from IAM console
```

```
Name:  AWS_SECRET_ACCESS_KEY
Value: copy value of Secret access key from IAM console
```
Add these secrets one by one

### 5 Upload Files
Upload your `.yaml` and `.html` files to your github repository in which you added your secrets.
You are all done, wait few minutes for upload to complete and check your S3 bucket, you'll see `main.html` file
