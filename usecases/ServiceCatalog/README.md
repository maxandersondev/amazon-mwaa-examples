# mwaa-service-catalog
This project has two cloudformation templates.  The cf_resources.yaml is the CloudFormation to create the ServiceCatalog Profile and Product.  This needs to be run first.  You will need to have a https location to access the resources.yaml that is also in this project.

The resourcesl.yaml is the CloudFormation for the ServiceCatalog item.  This will be what is used to provision the private MWAA configuration.  

The policy.json is just a reference to the permissions that are required for the launch role in the ServiceCatalog profile.  This is created for you in the CloudFormation.

Use CloudFormation to run cf_resources, then you can add anyone the profile group so they can provision the MWAA environment

# Step-by-step Guide

1. Upload the resources.yaml file to a http(s) location
2. Either use the console or cli to run the cf_resources.yaml file
    1. if you use the cli, you'll need to add the CAPABILITY_NAMED_IAM in the --capabilities
3. 

# Notes and troubleshooting
-- Need to make sure you have your own bucket and key defined

-- Need to make sure the key has access to the logs - https://docs.aws.amazon.com/mwaa/latest/userguide/mwaa-create-role.html#mwaa-create-role-cmk

-- Troubleshooting:

    -- Environment check: https://github.com/awslabs/aws-support-tools/tree/master/MWAA
    
    -- General: https://docs.aws.amazon.com/mwaa/latest/userguide/t-create-update-environment.html#t-create-environ-failed
