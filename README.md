# AWS Service Catalog CF Templates
A couple of very simple CF Templates to be used for an AWS Service Catalog POC

### Handy One-Liners for testing
    Notes:
    The '--profile <profile_name>' can be omitted if using a default aws profile
    These commands assume you are in the root of the repository

* Create a Stack

    `aws --profile <profile_name> cloudformation create-stack --stack-name presidioTest --template-body file://<template_name>.tmpl --parameters file://tests/<template_name>tests.params`

* Delete a Stack

    `aws --profile <profile_name> cloudformation delete-stack --stack-name presidioTest`

* Check the Status of a Stack (with formatting)

    `aws --profile <profile_name> cloudformation describe-stack-resources   --stack-name presidioTest   --output table  --query 'StackResources[*].[StackName,ResourceType,LogicalResourceId,PhysicalResourceId,ResourceStatus]'`
