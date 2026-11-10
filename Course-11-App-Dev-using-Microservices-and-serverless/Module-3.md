# Course 11: Application Development using Microservices and Serverless

## Module 3: Serverless Overview

### Key Concepts
- Serverless computing allows building and running applications without managing servers, using Backend as a Service (BaaS) and Function as a Service (FaaS) platforms.
- Cloud providers handle infrastructure management, enabling developers to focus on writing code with benefits like high availability, fault tolerance, and pay-per-request billing.

### Notes
Serverless computing abstracts away server management by leveraging cloud services that automatically handle infrastructure tasks. It includes BaaS, which provides ready-to-use backend services, and FaaS, which lets developers deploy individual functions triggered by events. This model accelerates development and reduces operational overhead. However, serverless has constraints such as latency issues for time-critical applications, challenges in monitoring and debugging, and lack of state persistence. The Serverless Framework, built on Node.js, helps manage serverless applications. Popular platforms include AWS Lambda, Google Cloud Functions, Microsoft Azure, IBM Cloud Functions, and Knative, each offering unique features for event-driven, scalable, and cost-effective computing.

### Code Examples
```python
# Example of a simple AWS Lambda function in Python
def lambda_handler(event, context):
    message = 'Hello, Serverless!'
    return {
        'statusCode': 200,
        'body': message
    }
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| Serverless | Runs applications without managing servers |
| BaaS | Backend as a Service, provides ready backend APIs |
| FaaS | Function as a Service, runs code in response to events |
| Serverless Framework | Tool to develop and deploy serverless applications |
| AWS Lambda | AWS's serverless compute service |
| API Gateway | Manages API requests to serverless functions |

### Glossary
- **Serverless**: A cloud computing model where the cloud provider manages the infrastructure, allowing developers to focus on code.
- **BaaS (Backend as a Service)**: Cloud services that provide backend functionalities like databases, authentication, and storage.
- **FaaS (Function as a Service)**: A serverless model where individual functions are executed in response to events.
- **API Gateway**: A service that acts as an entry point for APIs, routing requests to appropriate backend services or functions.

### Summary
Serverless computing simplifies application development by removing the need to manage servers, using BaaS and FaaS to build scalable, event-driven applications. While it offers benefits like cost efficiency and high availability, developers must consider its limitations such as latency and debugging complexity. Various cloud providers offer serverless platforms tailored to different needs.