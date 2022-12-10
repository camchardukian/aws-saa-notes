# Key Management Service (KMS)

_AWS Key Management Service (AWS KMS)_ enables us to perform encryption/decryption operations through the use of cryptographic keys.

It also allows us create, store, and manage keys.

The permissions to encrypt, decrypt, and generate keys are all different.

KMS keys can only operate cryptographically on data which is a maximum of 4KB in size.

_Data Encryption Keys (DEKs)_ can work with data larger than 4KB in size.

Generally speaking, KMS keys are isolated to a region and they never leave the region nor KMS itself. You cannot extract a KMS key.

You can, however, work with special multi-region keys within KMS.

Each KMS key has a key policy, which is a type of resource policy.
