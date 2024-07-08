# python-projects


Automating File Organization in AWS S3 using Lambda Functions


Overview
This project demonstrates how to automate file organization in an AWS S3 bucket using Python and Lambda Functions. The Lambda Function triggers whenever a new file is added to the S3 bucket, organizing it into folders based on the file's creation date.

Requirements
AWS Account with access to Lambda, S3, and IAM services.
Python 3.x installed locally.
AWS CLI configured with appropriate permissions.
Setup Instructions
Create an S3 Bucket:

Log in to your AWS Management Console.
Navigate to S3 and create a new bucket (my-automated-bucket).
Create an IAM Role:

Go to IAM and create a new role (LambdaS3ExecutionRole) with permissions:
AmazonS3ReadOnlyAccess: Allows Lambda to read from S3.
(Add any other permissions needed for your specific use case.)
Set up Lambda Function:

Create a new Lambda Function (FileOrganizer) in your AWS Lambda console.
Use Python 3.x as the runtime.
Attach the LambdaS3ExecutionRole IAM role to this function.
Upload Function Code:

Copy the Python code (lambda_function.py) provided in this repository.
Package any necessary dependencies (boto3) with your function code.
Configure Lambda Trigger:

Add an S3 trigger to your Lambda Function (my-automated-bucket).
Set the trigger to activate on object creation events.
Testing:

Upload a file to your S3 bucket to test the Lambda function.
Check the destination folder (YYYYMMDD/filename) to verify file organization.
