+++
title = "Using an AWS Event Engine Account"
chapter = false
weight = 10
+++

To complete this workshop, you are provided with an AWS account via the AWS Event Engine service. A 12-digit hash will be provided to you by event staff - this is your unique access code.

### Logging into Event Engine

1. Go to https://dashboard.eventengine.run to log into AWS Event Engine.
1. Enter your unique 12-digit hash code and choose *Accept Terms & Login*.
    ![Login to Event Engine](/images/ee-login.png)
1. Choose **AWS Console**.
    ![Select AWS Console](/images/ee-console.png)
1. Open the **AWS Console**.
    ![Open Console](/images/ee-open-console.png)

Please note the region that the event is using. You will need to use this region for all workshop activities.

There are instructions for managing CLI credentials, but you will not need them for this workshop.

This account will expire at the end of the workshop and the all the resources created will be automatically deprovisioned. You will not be able to access this account after today.

The existing Catalog API application will already be provisioned as an AWS Elastic Beanstalk application into the Event Engine AWS account. You are ready to continue onto [Testing the Catalog API](./30_testing.html)!