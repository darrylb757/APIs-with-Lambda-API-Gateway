# APIs-with-Lambda-API-Gateway
develop a server-less Lambda function, configure an API with API Gateway, connect Lambda with API Gateway


# APIs with Lambda + API Gateway


**Author:** Darryl Brown  
**Email:** darrylbrown1991@gmail.com

---

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-compute-api_c9d0e1f2)

---

## Introducing Today's Project!

In this project, I will develop a server-less Lambda function, configure an API with API Gateway, connect Lambda with API Gateway, and write JSON documentation for an API. I'm doing this project because it's important to understand how to set up server-less architecture and manage APIs. This will be layer 2 of a three-tier architecture. 

### Tools and concepts

Services I used were Lambda, API, API Gateway, AWS, JSON, REST API. Key concepts I include Lambda functions, API deployment, Lambda proxy integration, REST APIs, API stages, 2nd tier of three-tier architecture. 

### Project reflection

This project took me approximately 30. The most challenging part was navigating in the AWS API. It was most rewarding to the connection between API and Lambda functions.

I chose to do this project today to demonstrate the concept of the 2nd tier of a Three-Tier Architecture. 

---

## Lambda functions

AWS Lambda is a service that lets you run code without needing to manage any computers/servers, Lambda will manage them for you. Lambda runs code only when you need it to, so you're not paying for any idle time. It also scales automatically, from a few requests per day to thousands per second. All you need to do is supply the code in one of the languages that Lambda supports.

The code I added to my function will set up a Lambda function that retrieves data from a DynamoDB table. It looks for specific user data based on a 'user-Id' and returns that data. 

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-compute-api_a1b2c3d5)

---

## API Gateway

APIs or Application Programming Interface, is a way for different software systems to talk to each other. It's like a messenger that carries requests and responses between systems. There are different types of APIs, like REST API, HTTP, and WebSocket.  My API is REST API

Amazon API Gateway is an AWS service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. It manages incoming traffic, directing them to the correct services, and makes sure only authorized requests get through. I'm using API Gateway in this project because directly exposing Lambda functions to user requests isn't best practice. That's because Lambda doesn't have built in security or API management features. API Gateway brings in authentication and authorization features, and advanced API management capabilities that make the app more efficient.

API Gateway acts as the "front door" to my Lambda function. It receives requests and then forwards them to Lambda functions for processing. Lambda processes the request, then sends the response through the API Gateway back to the user.

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-compute-api_m3n4o5p6)

---

## API Resources and Methods

An API is made up of resources, which are individual endpoints within the API that handle different parts of its functionality.

Each resource consists of methods, API methods define the actions you can perform on a resource.

I created a Lambda function and turned on Lambda proxy integration, which is a setting that simplifies the connection between API Gateway and Lambda.

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-compute-api_c9d0e1f2)

---

## API Deployment

When you deploy an API, you deploy it to a specific stage. A stage is snapshot of my API at a specific point in time. I deployed to new stage and named in "production". 

To visit my API, I went to my Stage: Production and copied the invoke Url. The API displayed an error because have not yet set up my DynamoDB table and connected it with my API.

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-compute-api_3ethryj2)

---

## API Documentation

For my project's extension, I am writing API documentation because good documentation is crucial for developers to understand how to use the API correctly and efficiently. You can do this in my selected the documentation tab on the left in your API.

Once I prepared my documentation, I can publish it to a Stage of my API that I select. You have to publish your API to a specific stage because it makes sure that your documentation is consistent with the API version deployed to that stage.

My published and downloaded documentation showed me additional API settings specific to API Gateway. The other text in this file are documentation that API Gateway has automatically generated.

![Image](http://learn.nextwork.org/sincere_vermilion_playful_beaver/uploads/aws-compute-api_z9a0b1c2)

---

---
