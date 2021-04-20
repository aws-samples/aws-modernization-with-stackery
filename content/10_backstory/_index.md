+++
title = "Backstory"
chapter = true
weight = 10
+++

# Backstory
![Books R Us](/images/logo.png)

Books R Us is a small online bookseller based in the Pacific Northwest with absolutely no aspirations beyond selling books.

They have a home-grown legacy .NET Framework application to maintain their catalog of books. In the past year they migrated to AWS from their on-prem data center (phew!), but now they wish their catalog API were more resilient and scalable as their inventory and sales transactions are increasing exponentially!

Their application is running on [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/) in a Windows server. The catalog is stored in an MS SQL Server Database running in [Amazon RDS](https://aws.amazon.com/rds/).

![Existing Infrastructure](/images/existing-architecture.png)

You have been brought on as a cloud expert to help Books R Us modernize their catalog API. To make the catalog API more resilient, scale better, and cost less, you will upgrade the application from .NET Framework to .NET Core and run it serverlessly using [AWS Lambda](https://aws.amazon.com/lambda/).

There is a catch, however. Books R Us doesn't want to spend all the effort and time needed to reimplement the entire catalog API. There are two main ASP.NET controllers in the API servicing the /api/authors and /api/books routes. The /api/books routes are requested much more frequently, so those are the routes we will modernize and service via AWS Lambda. We'll leave the /api/authors routes to be serviced by the existing API server.

Continue to [Getting Started](../20_getting_started.html).