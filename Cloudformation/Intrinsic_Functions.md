# CloudFormation Intrinsic Functions

CloudFormation provides several built-in functions that we can use to manage our stacks by assigning values to properties that are not available until runtime.

A few of the key intrinsic functions are:

- **Ref** — Returns the value of the specified parameter or resource.

- **Fn::GetAtt** — Returns the value of an attribute from a resource in the template.

- **Fn::Join** — Appends a set of values into a single value, separated by the specified delimiter.

- **Fn::Split** — Splits a string into a list of string values.

- **Fn::GetAZs** — Returns an array that lists Availability Zones for a specified region in alphabetical order.

- **Fn::Select** — Returns a single object from a list of objects by index. This function doesn’t check for null values or if the index is out of bounds of the array, so it’s important to be certain the chosen index is valid to avoid stack errors.

- **Fn::Base64** — Returns the Base64 representation of the input string.

- **Fn::Sub** — Substitutes variables in an input string with values that we specify.

- **Fn::Cidr** — Returns an array of CIDR address blocks.

- Conditional intrinsic functions such as **Fn::If**, **Fn::Equals**, **Fn::Not**, **Fn::And**, **Fn::Or**.
