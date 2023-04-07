# Nested Stacks

Resources in a single stack share a lifecycle.

A single stack has a limit of 500 resources.

Stacks can’t easily reference other stacks and can’t easily reuse resources (e.g. A VPC).

The root stack is the one stack that is created manually. A stack is a parent stack of any stack which it directly creates.

Nested stacks can reuse templates whereas cross-stack references reuse resources actually created by another stack.

Nested stacks should only be used when everything is lifecycle linked. If not, cross-stack references may be a better choice.
