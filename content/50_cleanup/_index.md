+++
title = "Cleanup"
chapter = true
weight = 50
+++

# Cleanup
You've succeeded in modernizing this workshop's Catalog API! You may want to clean up the resources you provisioned if you are using your own AWS account. The following steps will remove all traces of the workshop.

### Deprovision the Modernized API Stack
Click into the *demo-dotnet-webapi* stack in the Stackery dashboard at https://app.stackery.io/stacks. Then, click the **Deploy** section of the stack from the left-hand sidebar.

![Stack Deploy View](/images/deployment.png)

Now click the **CloudFormation Stack** link to take you to the AWS CloudFormation page for this deployment.

![CloudFormation Stack](/images/cloudformation.png)

Click the **Delete** button in the top right corner of the CloudFormation page to deprovision all the resources associated with the modernized API stack. When the stack reaches the `DELETE_COMPLETE` stage all resources have been deprovisioned.

### Deprovision the Original Catalog API
Similarly, you can deprovision the original Catalog API by navigating to its [CloudFormation Stack](https://console.aws.amazon.com/cloudformation/home#/stacks/stackinfo?filteringStatus=active&filteringText=&viewNested=true&hideStacks=false&stackId=stackery-demo-dotnet). Again, click the **Delete** button to deprovision the stack. This will also automatically delete the Elastic Beanstalk stack that was provisioned.

### Unlink Stackery From Your AWS Account
{{% notice info %}}
This step is optional. You can leave Stackery linked to your AWS account for continued use without incurring costs beyond the [AWS Free Tier](https://aws.amazon.com/free/).
{{% /notice %}}

To unlink Stackery from your AWS account, again navigate to the [CloudFormation Stack that links Stackery with your AWS Account](https://console.aws.amazon.com/cloudformation/home#/stacks/stackinfo?filteringStatus=active&filteringText=&viewNested=true&hideStacks=false&stackId=stackery). Click the **Delete** button to delink your AWS account.