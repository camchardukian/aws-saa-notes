# CloudFormation Resources

CloudFormation templates contain logical resources that define WHAT we want created, and leave the HOW up to the CFN product.

CloudFormation templates create stacks, and stacks create physical resources from the logical resources.

Stacks keep physical and logical resources in-sync. If a stack’s template is changed the physical resources will also be changed.

Likewise, if a stack is deleted, the physical resources will also be deleted (in most cases).
