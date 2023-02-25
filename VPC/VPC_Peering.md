# VPC Peering

VPC Peering is a direct encrypted network link between two, and only two VPCs.

VPC Peering can be done whether the VPCs are in the same accounts or different accounts, and whether the VPCs are in the same region or different regions.

VPC Peering does NOT support transitive peering.

VPC Peering connections cannot be created where there is overlap in the VPC CIDRs, this is why ideally we should never use the same address ranges in multiple VPCs.
