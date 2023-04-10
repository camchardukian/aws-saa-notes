# Stack Roles

By default, CloudFormation uses the permissions of the logged-in identity.

To use CloudFormation effectively, we need access to both stacks and the resources which those stacks are trying to create/update/delete.

There is an exception to this -- enter Stack Roles.

Stack roles allow an IAM role to be passed into the stack via `PassRole`.

A stack can then use this role, rather than the identity interacting with the stack to create, update, and delete AWS resources.
