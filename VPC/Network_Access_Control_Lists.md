# Network Access Control Lists (NACLs)

NACLs are an optional layer of security that can be used with VPCs. NACLs act as a firewall for controlling traffic in and out of one or more subnets.

Each subnet has an associated NACL. This can either be the default NACL or a custom NACL we create and assign to it. While NACLs filter traffic coming in and out of subnets, connections within a subnet are NOT impacted by NACLs.

NACLs are stateless. Because of this, both the REQUEST and RESPONSE parts of every communication need individual rules.

NACLs allow both explicit ALLOWS and explicit DENYS. NACL rules are processed in order. The lowest numbered rules are processed first, and processing stops once a match occurs.

VPCs are created with a default NACL that’s given an implicit DENY `(*)` as well as an ALLOW all rule. The result is that this default NACL allows all traffic by default, meaning it has essentially no effect.

Custom NACLs can be created for a specific VPC and they are initially associated with no subnets. Newly created custom NACLs have implicit DENY rules, but no ALLOW rules. The result is that they deny all traffic.

NACLs are often used with Security Groups in a way such that the Security Groups are used to allow traffic while the NACLs are used to deny traffic.
