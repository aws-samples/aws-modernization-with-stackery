---
title: "Serverless ASP.NET Framework Modernization Workshop"
chapter: true
weight: 1
---

# Serverless ASP.NET Framework Modernization Workshop

### Welcome

This is a workshop to demonstrate how to modernize an ASP.NET REST API service, which runs on expensive, inflexible Windows servers in the cloud, into a resilient, highly scalable serverless service. The approach utilizes the [Strangler Fig Pattern](https://martinfowler.com/bliki/StranglerFigApplication.html) to modernize the application piece-by-piece rather than rewrite the entire application all at once.

### Learning Objectives
- Modernize a [.NET Framework application to .NET Core](https://dotnet.microsoft.com/learn/dotnet/what-is-dotnet-framework).
- Use the [Strangler Fig Pattern](https://martinfowler.com/bliki/StranglerFigApplication.html) to modernize one controller while leaving the rest.
- Augment the .NET Core application to run in [AWS Lambda](https://aws.amazon.com/lambda/) and serve requests from [AWS API Gateway](https://aws.amazon.com/api-gateway/) serverlessly.

### What You'll Need

To complete this workshop you will need an [AWS](https://aws.amazon.com/) account, a free [Stackery](https://stackery.io) account, and a few free tools. There are two routes for accessing an AWS account:

* If you are doing this workshop as part of a scheduled AWS Virtual Workshop, you will have access to a free account provisioned for you for use during the workshop. This account will already be running a .NET Framework API using [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/).
* Otherwise, you can use an existing AWS account or open a new one. The workshop setup steps will guide you to provision some resources into your account to start a .NET Framework API using [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/). All resource usage fits within the [AWS Free Tier](https://aws.amazon.com/free), so you should not incur any expense running this workshop in a new account. If you run the workshop on an AWS account that does not qualify for the free tier it will cost around $1.03 per day that it is running in your account (this estimate is based on us-east-1 prices).

{{% notice info %}}
Even though we'll be modernizing a .NET Framework application, which can only run on Windows machines, this workshop does not require you to be running Windows. One of the great benefits of modernizing to .NET Core is compatibility across operating systems! You can use Windows, OS X, or Linux to complete this workshop.
{{% /notice %}}

### Let's get started!

Ready? Let's find out the [backstory of our modernization project](./10_backstory.html)

{{% notice warning %}}
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be architected to build a solution while demonstrating best practices along the way. These examples are not intended for use in production environments.
{{% /notice %}}
