# Cross-Stack References

Outputs of stacks are not normally visible from other stacks, but outputs can be exported, thus making them visible from other stacks.

Exports must have a unique name in the region of the account they are located in. Different accounts in the same region, however, may have exports with the same name.

`Fn::ImportValue` can be used instead of `Ref` to access outputs exported from other stacks.
