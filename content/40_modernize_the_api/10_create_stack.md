+++
title = "Create the Stack"
chapter = false
weight = 10
+++

A [Stackery Stack](https://docs.stackery.io/docs/using-stackery/introduction#stacks) is an application consisting of relationships between cloud resources specified in a configuration file (a CloudFormation / SAM template) and their related assets (e.g. Lambda Function source code) inside of a Git repository. We're going to start by forking and checking out the existing [Catalog API Git repository](https://github.com/stackery/dotnet-framework-webapi).

### Fork your GitHub Repository
{{% notice info %}}
You'll need a [GitHub](https://github.com) account. If you don't already have a GitHub account you can create a free one [here](https://github.com/join).
{{% /notice %}}

Open the [Catalog API Git repository](https://github.com/stackery/dotnet-framework-webapi). In the upper right hand corner click the button to **Fork** it, and choose whether to fork it to your personal space or an organization space, if you are part of one.

### Create a New Stackery Stack
We're going to create a new Stackery Stack inside your forked repository. Navigate to the Stackery [Stacks](https://app.stackery.io/stacks) page. Click the drop-down button to **Add a Stack** and choose **With an existing repo**.

![Add a Stack with an Existing Repo](/images/create-stack.png)

Fill in the details for your new stack by selecting *GitHub* as your Git Provider, *demo-dotnet-webapi* (or similar) for your stack name, and use the autocomplete form field to find your fork of the *dotnet-framework-webapi* repo. Click the **Add Stack** button.

{{% notice info %}}
If this is the first time you're using Stackery with GitHub you'll be asked to authorize Stackery to access your GitHub account.
{{% /notice %}}

![Create Stack Form](/images/create-stack-form.png)

### Clone and Check Out Your Fork

#### Using a Local IDE

If you have your own usual method for checking out your fork, now's the time to do it! If not, we highly recommend using [Visual Studio Code](https://code.visualstudio.com/)'s built-in GitHub functionality to [clone and check out](https://code.visualstudio.com/docs/editor/github#_setting-up-a-repository) your fork.

#### Get the source code to Cloud9 environment

To get copy of your fork locally to Cloud9, copy below commands and replace <yourusername> with you real GitHub username.
   ```sh
   mkdir -p ~/.c9/.repositories && \
   mkdir -p /home/ec2-user/environment/github.com/<yourusername> && \
   cd /home/ec2-user/environment/github.com/<yourusername> && \
   git init && \
   git clone git@github.com:<yourusername>/dotnet-framework-webapi.git  && \
   cd /dotnet-framework-webapi && \
   touch ~/.c9/.repositories/dotnet-framework-webapi
   ```

You're now ready to [Create the Infrastructure](./20_create_infrastructure.html) for your stack!