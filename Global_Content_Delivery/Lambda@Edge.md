# Lambda@Edge

Lambda@Edge is a feature of CloudFront that allows us to run lightweight Lambda functions at CloudFront edge locations to modify traffic.

These functions can adjust the data between the Viewer & the Origin.

Lambda@Edge currently only supports Node.js and Python.

It runs in the AWS Public Space.

Lambda@Edge does not support Lambda Layers.

Lambda@Edge has different size and execution time limits than regular Lambda.
