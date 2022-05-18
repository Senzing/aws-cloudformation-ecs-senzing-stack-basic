# aws-cloudformation-ecs-senzing-stack-basic

## Synopsis

The `aws-cloudformation-ecs-senzing-stack-basic` AWS Cloudformation template
deploys Senzing for use with a previously deployed
[aws-cloudformation-database-cluster](https://github.com/Senzing/aws-cloudformation-database-cluster) Cloudformation stack.

## How to deploy without much thinking

1. :warning: **Warning:** This Cloudformation deployment will accrue AWS costs.
   With appropriate permissions, the
   [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/)
   can help evaluate costs.
1. Visit [AWS Cloudformation with Senzing template](https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=senzing-basic&templateURL=https://s3.amazonaws.com/public-read-access/aws-cloudformation-ecs-senzing-stack-basic/cloudformation.yaml)
1. Download the appropriate [AWS Cloudformation template example](https://raw.githubusercontent.com/Senzing/aws-cloudformation-ecs-senzing-stack-basic/main/cloudformation.yaml) from this repository to your local device.  Example:
    ```
    curl -X GET \
        --output ~/cloudformation.yaml \
        https://raw.githubusercontent.com/Senzing/aws-cloudformation-ecs-senzing-stack-basic/main/cloudformation.yaml
    ```
3. It is highly suggested to take a look at the AWS Cloudformation Template that has been downloaded.  This template is an example that deploys and configures a number of services and facilities.  While it is a working and complete example, each business may have different requirements and their account may not have all the privledges required to deploy it.  Furthermore, the examples change over time and these files are meant to be treated as code files so they should be put under source control.
1. Visit the [AWS Cloudformation home](https://console.aws.amazon.com/cloudformation/home).
1. At the upper-right, click the "Create stack" drop-down and choose "With new resources (standard)".
1. In the "Specify template" area choose the "Upload a template file" radio button.
1. Select the "Choose file" button and choose the AWS Cloudformation template that was downloaded previously.1. At lower-right, click on "Next" button.
1. In **Specify stack details**
    1. In **Parameters**
        1. In **Security responsibility**
            1. Understand the nature of the security in the deployment.
            1. Once understood, enter "I AGREE".
        1. In **Senzing installation**
            1. Accept the End User License Agreement
        1. In **Security**
            1. Enter your email address.  Example: `me@example.com`
        1. In **Identify existing resources**
            1. Enter the stack name of the previously deployed
               [aws-cloudformation-database-cluster](https://github.com/Senzing/aws-cloudformation-database-cluster)
               Cloudformation stack
               Example:  `senzing-db`
    2. At lower-right, click "Next" button.
2. In **Configure stack options**
    1. At lower-right, click "Next" button.
3. In **Review senzing-basic**
    1. Near the bottom, in **Capabilities**
        1. Check ":ballot_box_with_check: I acknowledge that AWS CloudFormation might create IAM resources."
    2. At lower-right, click "Create stack" button.

## Additional topics

1. [Details of deployment](docs/README.md)
1. [How to load AWS Cloudformation queue](https://github.com/Senzing/knowledge-base/blob/main/HOWTO/load-aws-cloudformation-queue.md)
1. [How to update Senzing license](https://github.com/Senzing/knowledge-base/blob/main/HOWTO/update-senzing-license.md)
