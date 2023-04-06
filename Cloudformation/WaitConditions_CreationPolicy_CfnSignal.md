# WaitConditions, CreationPolicy & cfn-signal

_CreationPolicy_, _WaitConditions_, and _cfn-signal_ can be used together to prevent the status of a resource from reaching ‘create complete’ until CloudFormation receives a specified number of success signals or the timeout period has been exceeded.

The cfn-signal helper script signals CloudFormation to indicate whether Amazon EC2 instances have been successfully created or updated.
