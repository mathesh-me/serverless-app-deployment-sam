## Serverless Application Development using AWS SAM 🚀
Deploying a Simple Serverless Application with AWS SAM

### Architecture Description 📚

The architecture of the application is simple. It consists of an API Gateway and a Lambda function. The API Gateway is used to expose the Lambda function to the outside world. The Lambda function is written in Python and it returns a simple JSON response. The API Gateway is configured to accept GET requests and it forwards the requests to the Lambda function. The Lambda function processes the request and returns a JSON response.

### Architecture Diagram 📊

![Serverless App Deployment using AWS SAM -  Architecture Diagram](https://github.com/mathesh-me/serverless-app-deployment-sam/assets/144098846/0433a43e-6181-46c1-9019-51bde70d0733)


### Why SAM? 🤔

Let's Consider a Scenario where we want to build a simple serverless application using AWS Lambda and API Gateway. We can create the Lambda function and API Gateway manually using the AWS Management Console. Or we can Build this using AWS CloudFormation. But the problem with CloudFormation is that we have to manually write the CloudFormation template which is a bit complex and time-consuming. This is where AWS SAM comes into the picture. AWS SAM is a framework that allows us to deploy serverless applications easily. It's syntax is simple and easy to understand than CloudFormation. It is an extension of CloudFormation and it is used to define serverless applications in simple and easy way.

### Prerequisites 📋

- AWS Account with necessary permissions to create resources
- AWS CLI Installed and Configured
- AWS SAM CLI Installed

### Usage 💻

1. Clone the Repository
```
git clone 
```
2. Navigate to the Repository
```
cd 
```
3. Create a S3 Bucket to store the deployment artifacts
```
aws s3 mb s3://<s3-bucket-name>
```
4. Package the Application
```
sam package --template-file sam-template.yaml --output-template-file generated-template-folder/sam-generated-template.yaml --s3-bucket <s3-bucket-name>
```
5. Deploy the Application
```
sam deploy --template-file generated-template-folder/sam-generated-template.yaml --stack-name <stack-name> --capabilities CAPABILITY_IAM
```
6. Get the API Gateway URL: It can be found in the Outputs section of the CloudFormation Stack

7. Test the Application using the API Gateway URL in the browser or using curl.

### Contributing 🤝

Contributions are welcome! Please feel free to submit a Pull Request.

### License 📝

This project is licensed under the MIT License - see the LICENSE file for details.

### Author 📖

- [Mathesh M](https://www.linkedin.com/in/mathesh-me/) on LinkedIn.
- Checkout this Blog for how build this Application from Scratch: [Serverless Application Development using AWS SAM]()
- You Can also check out my [Medium](https://medium.com/@mathesh-me) for articles on DevOps Tools and Technologies.
