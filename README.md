## Unicorn Ride App

## Project Overview
This project demonstrates the implementation of a secure serverless web application using AWS services. The application includes user authentication, data storage, and API management following cloud security best practices.

## Architecture
The application uses the following AWS services:
- **AWS Cloud9**: Development environment
- **AWS CodeCommit**: Source code repository
- **AWS Amplify**: Web application hosting and CI/CD
- **Amazon Cognito**: User authentication and authorization
- **AWS Lambda**: Serverless compute functions
- **Amazon DynamoDB**: NoSQL database
- **Amazon API Gateway**: REST API management
- **AWS IAM**: Identity and access management

## Features
- User registration and authentication
- Secure API endpoints with authorization
- Real-time data storage and retrieval
- Automated deployment pipeline
- Responsive web interface

## Prerequisites
- AWS Account with appropriate permissions
- Basic knowledge of JavaScript/Node.js
- Understanding of AWS services
- Git installed locally

## Setup Instructions

### 1. Development Environment Setup
1. Create AWS Cloud9 environment named "serverless"
2. Configure the development environment with necessary tools

### 2. Source Code Repository
1. Create a new repository in AWS CodeCommit
2. Clone the repository to your local development environment
3. Create a new branch for development
4. Set up folder structure with necessary files

### 3. Web Application Deployment
1. Connect AWS Amplify to the CodeCommit repository
2. Create an IAM role for Amplify with read-only permissions
3. Configure build settings and deploy the application
4. Verify successful deployment and website functionality

### 4. Authentication Setup
1. Install AWS Amplify CLI
2. Configure Amplify authentication with Amazon Cognito
3. Set up user pool and identity pool
4. Test user registration and login functionality

### 5. Database Configuration
1. Create DynamoDB table for data storage
2. Configure table settings and indexes
3. Set up IAM roles and policies for database access

### 6. Lambda Function Setup
1. Create Lambda function for backend processing
2. Configure function runtime and permissions
3. Update function code (index.js) with business logic
4. Test function execution

### 7. API Gateway Configuration
1. Create REST API in Amazon API Gateway
2. Set up API authorizer using Cognito tokens
3. Create resources and methods (/ride endpoint)
4. Configure POST method for data submission
5. Deploy API and test endpoints

## Security Implementation

### Authentication & Authorization
- User authentication via Amazon Cognito
- JWT token-based authorization
- API Gateway authorizer for secure endpoint access

### Access Control
- IAM roles with least privilege principle
- Resource-based policies for DynamoDB access
- API-level authorization checks

### Data Security
- Encrypted data storage in DynamoDB
- Secure API communication
- Input validation and sanitization

## API Endpoints

### POST /ride
- **Description**: Submit ride request data
- **Authorization**: Required (Cognito JWT token)
- **Method**: POST
- **Response**: 200 OK on success

## Testing
1. User registration and email verification
2. User login functionality
3. API authorization testing
4. Data submission and retrieval
5. End-to-end application workflow

## Deployment Pipeline
The project uses AWS Amplify for continuous deployment:
1. Code changes pushed to CodeCommit
2. Amplify automatically triggers build process
3. Application deployed to hosting environment
4. Build status and logs available in Amplify console

## Project Structure
```
serverless-project/
├── src/
│   ├── index.html
│   ├── styles/
│   └── scripts/
├── amplify/
│   ├── backend/
│   └── team-provider-info.json
├── lambda/
│   └── index.js
└── README.md
```

## Configuration Files
- **amplify/backend/**: Amplify backend configuration
- **lambda/index.js**: Lambda function code
- **src/**: Frontend application files

## Screenshots and Documentation
Refer to the submitted assignment document for detailed screenshots of:
- Cloud9 environment setup
- CodeCommit repository creation
- Amplify deployment process
- Cognito user pool configuration
- DynamoDB table creation
- Lambda function setup
- API Gateway configuration
- Testing results

## Best Practices Implemented
1. **Infrastructure as Code**: Configuration managed through Amplify
2. **Least Privilege Access**: IAM roles with minimal required permissions
3. **Secure Authentication**: Multi-factor authentication support
4. **API Security**: Token-based authorization
5. **Monitoring**: CloudWatch logs and metrics
6. **Version Control**: Git-based source control

## Troubleshooting
- Verify IAM permissions for all services
- Check Cognito user pool configuration
- Ensure Lambda function has correct execution role
- Validate API Gateway authorizer configuration
- Monitor CloudWatch logs for errors

## Future Enhancements
- Implement additional security headers
- Add rate limiting to API endpoints
- Implement data encryption at rest
- Add comprehensive logging and monitoring
- Implement automated security scanning



**Note**: This README provides a comprehensive overview of the serverless cloud security project implementation. For detailed step-by-step instructions with screenshots, refer to the complete assignment submission document.
