# CloudFormation DependsOn

CloudFormation tries to be efficient, and it does this by creating, updating, and deleting resources in parallel.

By default, it tries to determine a dependency order by seeing which resources reference other resources.

Using the _DependsOn_ attribute, however, we can explicitly define what resources depend on other resources.
