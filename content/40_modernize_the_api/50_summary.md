+++
title = "Summary"
chapter = false
weight = 50
+++

You did it! You modernized an existing .NET Framework API to run serverlessly using AWS API Gateway and Lambda. More impressively, you did this without rewriting the entire app from scratch! Books R Us are super pleased.

To recap, you started with a [two- or three-tier](https://en.wikipedia.org/wiki/Multitier_architecture) ASP.NET Framework application running on Windows-based EC2 servers:

![Previous Architecture](/images/existing-architecture.png)

You then started converting half of the application, the /books routes, to be served serverlessly:

![Modernized Architecture](/images/modernized-architecture.png)

Running a serverless architecture enables you to lower operational overhead by sharing infrastructure operations with AWS, enabling your service to have higher scalability and reliability while reducing total cost of ownership.

At this point you can choose to complete the modernization by refactoring the Authors controller. Then you will be able to shut down the Elastic Beanstalk application and run completely serverlessly, in a more scalable, reliable, and cost effect manner. And you won't have to track any more operating system licenses for your servers :).

If you are running this workshop in your own AWS account, continue to the [Cleanup](../50_cleanup.html) section to safely remove all the resources from your AWS account.