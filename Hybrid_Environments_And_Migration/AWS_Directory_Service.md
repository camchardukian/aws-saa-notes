# AWS Directory Service

Directories store objects (e.g. Users, Groups, Computers, Servers, File Shares) with a structure (domain/tree).

Multiple trees can be grouped into a forest.

Directory Service is an AWS managed implementation of a directory.

Directory Service runs from within a VPC.

Some AWS services such as Amazon Workspaces NEED a directory in order to operate.

AWS Directory Service can run in one of three modes:

- Simple AD - An implementation of Samba 4 (compatible with basic AD functions)
- AWS Managed Microsoft AD - An actual Microsoft AD DS Implementation
- AD Connector - proxies requests back to an on-premises directory
