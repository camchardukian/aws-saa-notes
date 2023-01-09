# Route 53 Health Checks

Amazon Route 53 health checks are used to monitor the health and performance of our web applications, web servers, and other resources.

Health checks can monitor one of the following:

- The health of a specified resource, such as a web server
- The status of other health checks
- The status of an Amazon CloudWatch alarm

Health checks are separate from records, but are used by records.

Health checkers are located globally and by default perform their checks every 30 seconds. These checks can be sped up to every 10 seconds for an additional cost.
