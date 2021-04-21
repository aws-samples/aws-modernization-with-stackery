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

##### Setup .NET on Cloud9 environment
To install version 3.1 of the .NET SDK and Runtime follow these steps in a Cloud9 terminal session:

1. Copy and paste the following to install the .NET SDK
    ```sh
    sudo yum -y update && \
    sudo yum -y install libunwind && \
    wget https://dot.net/v1/dotnet-install.sh && \
    chmod u=rx dotnet-install.sh && \
    ./dotnet-install.sh -c 3.1 && \
    echo 'PATH=$HOME/.dotnet:$PATH' >> ~/.bashrc && \
    source ~/.bashrc && \
    rm -f dotnet-install.sh
    ```
   
1. Confirm the .NET Core SDK and Runtime is installed.
    ```sh
    dotnet --version
    ```
    
##### Setup Access to GitHub in Cloud9 Environment

1. Generate an SSH key pair and display the public key to be copied to GitHub. Leave the default file name by pressing enter when asked for a file to save the key, and enter a passphrase of your choice (twice to confirm). You will see the key starting from "ssh-rsa"
    ```sh
    ssh-keygen -t rsa && \
    cat /home/ec2-user/.ssh/id_rsa.pub
    ```

    You will see your new public SSH key printed to the terminal like the following:

    <pre>ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAklOUpkDHrfHY17SbrmTIpNLTGK9Tjom/BWDSUGPl+nafzlHDTYW7hdI4yZ5ew18JH4JW9jbhUFrviQzM7xlELEVf4h9lFX5QVkbPppSwg0cda3Pbv7kOdJ/MTyBlWXFCRHAo3FXRitBqxiX1nKhXpHAZsMciLq8V6RjsNAQwdsdMFvSlVK/7XAt3FaoJoAsncM1Q9x5+3V0Ww68/eIFmb1zuUFljQJKprrX88XypNDvjYNby6vw/Pb0rwert/EnmZ+AW4OZPnTPI89ZPmVMLuayrD2cE86Z/il8b+gw3r31nKatmIkjn2so1d01QraTlMqVSsbxNrRFi9wrf+M7Q== yourmail@example.com</pre>

    Select and copy all the printed text of the key.

1. Create a new SSH key authorization in GitHub:
    1. Go to your GitHub account [keys](https://github.com/settings/keys)
    1. Click **New SSH Key**
    1. Add a title (for example *Stackery workshop Cloud9 environment*)
    1. Paste the public key text from above into the **Key** section
    1. Click **Add SSH key**

1. Start the SSH agent in your Cloud9 environment if it's not already running, and add your new private SSH key to its registry. Enter the passphrase you used when creating the key when asked.
    ```sh
    eval $(ssh-agent -s) && \
    ssh-add /home/ec2-user/.ssh/id_rsa
    ```

1. Set required git author information, replacing values with your name and email below
    ```sh
    git config --global user.name <yourusername> && \
    git config --global user.email <yourmail@example.com>
    ```

We're all set up now! Let's start the [Modernization](../40_modernize_the_api.html).
