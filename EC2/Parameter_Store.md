# AWS Systems Manager Parameter Store

AWS Systems Manager Parameter Store provides secure, hierarchical storage for configuration, data management, and secrets management.

It allows us to store data such as passwords, database strings, AMI IDs, and license codes as parameter values. These values can be stored as encrypted data or plain text.

More importantly, these Systems Manager parameters can be referenced from our scripts, commands, SSM documents, and configuration/automation workflows by using the unique name we specified when creating the parameter.
