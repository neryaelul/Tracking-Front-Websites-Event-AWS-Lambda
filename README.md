# Tracking Front Websites Event with AWS Lambda

This repository contains the AWS Lambda function used for tracking events on frontend websites. The function is designed to capture user interactions and other significant events, facilitating analytics and insights on user behavior.

## Getting Started

These instructions will get you a copy of the project up and running on your AWS Lambda environment for development and testing purposes.

### Prerequisites

Before you deploy the lambda function, make sure you have the following:
- An AWS account.
- AWS CLI installed and configured.
- Basic knowledge of AWS Lambda and IAM roles.

### Deployment

To deploy this lambda function:
1. Clone the repository to your local machine:
  ```
   git clone https://github.com/neryaelul/Tracking-Front-Websites-Event-AWS-Lambda.git
  ```

   
Navigate to the repository directory:
  ```
  cd Tracking-Front-Websites-Event-AWS-Lambda
  ```

Use the AWS CLI to create a new lambda function:
  ```
  aws lambda create-function --function-name tracking-function \
--runtime nodejs12.x --role <role-arn> --handler index.handler \
--zip-file fileb://function.zip --timeout 15 --memory-size 128
  ```

## Configuration

Configure the lambda function by setting the environment variables as needed:

- `DATABASE_URL`: URL to the database where events will be stored.
- `API_KEY`: Key for authenticating requests if necessary.

## Usage

This lambda function is triggered by events specified in AWS Lambda's console under the function's configuration. Configure your front-end to send events to this lambda function through AWS API Gateway or another preferred method.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.



