# CloudHSM

CloudHSM is a true “single tenant” hardware security module that can help us meet corporate, contractual, and regulatory compliance requirements for data security.

CloudHSM is fully FIPS 140-2 Level 3 compliant whereas KMS overall is only level 2 compliant (because some of KMS is level 3 compliant whereas other parts are only level 2 compliant).

CloudHSM has no native AWS integrations by default.

SSL/TLS processing for web servers can be offloaded onto CloudHSM.

CloudHSM can also be used to protect the Private Keys for an Issuing Certificate Authority (CA).
