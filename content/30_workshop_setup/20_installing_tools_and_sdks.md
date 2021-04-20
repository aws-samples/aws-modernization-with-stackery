+++
title = "Installing Tools and SDKs"
chapter = false
weight = 20
+++

To complete this workshop we'll need a few additional tools and SDKs.

### Your Favorite IDE or Editor
You can use any IDE or editor of your choosing. If you don't have one set up yet you can use [AWS Cloud9](https://aws.amazon.com/cloud9/).

### .NET Core SDK
We need to .NET Core SDK to build the serverless version of our app. If you want to install the .NET Core SDK into a Cloud9 environment, skip ahead to [Using an AWS Cloud9 Environment](#using-an-aws-cloud9-environment).

#### Using a Local IDE or Editor
Building a .NET Core Lambda Function requires the .NET Core SDK and Runtime. Click [this link](https://dotnet.microsoft.com/download) then click the **Download .NET Core SDK** button to download the SDK for your OS, then complete the installation process.

{{% notice info %}}
Note that we are downloading the current [Long-Term Support](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) (LTS) version: ***.NET Core 3.1***. Do not download the SDK for .NET 5. We're using the built-in AWS Lambda .NET runtime to simplify our operations. AWS Lambda does not support .NET 5 natively because it is not an LTS release.
{{% /notice %}}

We're all set up now! Let's start the [Modernization](../40_modernize_the_api.html).

#### Using an AWS Cloud9 Environment
If you are using a recently provisioned AWS Cloud9 environment it likely already has the .NET Core 3.1 SDK and Runtime installed. You can check by running `dotnet --version` in a Cloud9 terminal session.

<pre>
dotnet --version

3.1.406
</pre>

If you see version 3.1 is installed you can continue to starting the [Modernization](../40_modernize_the_api.html)!

If version 3.1 of the .NET SDK and Runtime aren't installed perform the following steps in a Cloud9 terminal session:

1. Copy and paste the following to install the .NET SDK
    ```sh
    sudo yum -y update && \
    sudo yum -y install libunwind && \
    wget https://dot.net/v1/dotnet-install.sh && \
    chmod u=rx dotnet-install.sh && \
    ./dotnet-install.sh -c 3.1 && \
    echo 'PATH=$HOME/.dotnet:$PATH' >> ~/.bashrc && \
    source ~/.bashrc && \
    rm dotnet-install.sh
    ```
1. Confirm the .NET Core SDK and Runtime is installed.
    ```sh
    dotnet --version
    ```
    
##### Instructions for setting up GitHub access TBD

We're all set up now! Let's start the [Modernization](../40_modernize_the_api.html).
