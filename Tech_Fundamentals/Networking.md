# Networking

According to [Wikipedia](https://en.wikipedia.org/wiki/OSI_model), the _Open Systems Interconnection model (OSI model)_ is a conceptual model that provides a common basis for the coordination of [ISO] standards development for the purpose of systems interconnection.

The 7 layers in the OSI model work together to collaboratively transmit data from one person to another across the globe.

## OSI Model Layer 1 (Physical)

Layer 1 (the lowest layer) of the OSI model focuses on the electrical and physical shared medium of devices.

This may include the layouts of pins, hubs, network adapters, etc.

This layer is responsible for containing information inside bits and transferring these individual bits from one node to the next.

## OSI Model Layer 2 (Data Link)

The _Data Link_ layer requires a physical layer underneath it in order to run.

This is actually common in the OSI model. Higher level layers typically build upon lower layers.

The data link layer or layer 2 provides the means to detect and possibly correct errors that occur in the physical layer.

Devices at layer 2 (L2) have a unique hardware (MAC) address.

A _media access control address (MAC address)_ is a unique identifier commonly used with networking technologies such as Ethernet, Wi-Fi, and Bluetooth.

They also have a frame which is a container of sorts. Frames contain a source, destination, and data.

When devices attempt to use a medium simultaneously, frame collisions may occur.

The data link layer often includes data-link protocols that specify how devices should detect and recover from these collisions.

## OSI Model Layer 3 (Network)

Layer 3 of the OSI Model is the network layer. The network layer requires one or more data link layers (layer 2) beneath it in order to function.

The "job" of this layer is to get data from one location to another.

Layer 3 adds _Internet Protocol_ (IP), which adds cross-network IP addressing and routing to move data between local area networks without direct point-to-point connections.

Packets contain data which they generally carry for layer 4 protocols.

Packets also have a source and destination IP address.

Packets have a time-to-live or hop limit, which dictates the maximum number of hops a packet can go through before being discarded.

## OSI Model Layer 4 (Transport)

The 4th layer of the OSI model is the transport layer.

This layer handles transport protocols such as the _Transmission Control Protocol_ (TCP) and _User Datagram Protocol_ (UDP).

TCP is the more reliable procotol while UDP is faster and more efficient.

TCP can assist with the retransmission of lost packets. UDP can't because it focuses on speed and efficiency rather than reliability.

## Other Networking Concepts

### IP Addresses & IP Conversions

It's possible to convert from dotted decimal IPs to binary IPs (and vice versa if necessary).

This is because both addresses are 32 bits and divided into four parts containing 8 bits each (these parts can be referred to as octets).

Each octet is separated by a period.

### IP Addressing v4

All IP addresses have a "network" part and a "host" part.

If the network component of two IP addresses match, then those two devices are local. If not, the two devices are remote.

IP addresses need to be unique both globally and locally.

### Subnetting

_Subnetting_ is the process of breaking a network up into smaller logical sub-networks commonly called subnets.

The larger the prefix value, the smaller the network.

The entire internet is a /0 network. That's the reason 0.0.0.0 is often the default route (because it matches the entire internet).

Networks are usually split into even numbers. While uncommon, odd number splits can also be valid.

### Subnet Mask

A _subnet mask_ is a dotted decimal version of a binary number that indicates which part of an IP address is the network and which part is the host.

Subnet masks can help a host determine if an IP address it needs to communicate with is local or remote.

### Address Resolution Protocol

The _Address Resolution Protocol_ (ARP) is a communication protocol for determining the MAC address of a given IP address.

### Routers, Routes & Route Tables

_Routes_ are used to determine where a packet should be forwarded to.

_Route tables_ are simply tables containing many routes.

_Routers_ help move packets from a source to a destination -- encapulating the packets in different layer 2 frames along the way.

### Network Address Translation

_Network Address Translation_ (NAT) is the process of adjusting packets' source and destination addresses to allow transit across different networks.

We generally only need to use NAT with IPv4.

The engineers that created IPv4 couldn't predict that the 4,294,967,296 available public IPv4 addresses wouldn't be enough.

IPv6 on the other hand has enough available addresses that NAT is generally unnecessary.

For that reason, it seems likely that one day we will no longer need NAT or private IP addresses.

## Distributed Denial of Service (DDoS) Attacks

DDoS attacks compete with legitimate traffic by overwhelming servers/services/networks with a flood of internet traffic.

DDoS attacks can be broadly sorted into three categories:

- **Application Layer Attacks** -- This type of attack takes advantage of the fact that it's often very easy to make requests from the client, but expensive for the server to generate a response.

- **Protocol Attacks** -- Protocol attacks attempt to exhaust the resource of a server or the infrastructure surrounding it such as its firewalls, routing engines, or load balancers. The most common example of this type of attack is the SYN flood attack.

- **Volumetric Attacks** -- This type of attack attempts to bombard a server with tremendous amounts of traffic such that the server's bandwidth gets completely exhausted. The most common example of this type of attack is the DNS amplification attack.

### SSL & TLS

_Secure Sockets Layer_ (SSL) and _Transport Layer Security_ (TLS) are two protocols used to help securely authenticate and transport data over the internet.

Both operate in similar fashions, but TLS is used more these days as SSL is deprecated.

SSL 2.0 and 3.0 were released in the mid 1990s (SSL 1.0 was never released due to security issues), and both were since deprecated in the mid 2010s.

There is no difference between a TLS and an SSL certificate. Both refer to the same thing.

The way both TLS and SSL work is that an TLS/SSL certificate is installed on a website.

This certificate contains a public key as well as a private key that authenticates the server and allows it to encrypt/decrypt data.

When a visitor visits a website the browser will attempt to verify that website's SSL certificate.

It's able to do this because browsers come installed with the public keys of the major _certificate authorities_ (CAs).

Thus, the browser is able to check that a web server's certificate was signed by the trusted certificate authority.

If the browser confirms this successfully, it will create an encrypted link between itself and the server to securely transport data.

And if not... that's when we're likely to encounter the familiar, "Your connection is not private" error.

### Hashing

_Hashing_ is a process where data of any arbitrary size is mapped to fixed-size values.

Some of the core concepts of hashing are as follows:

1. The same input should always result in the same outout.
1. Different data should never generate the same hash value.
1. Changing even one pixel or character should result in a different hash value being output.
1. Hashing is 1-way only -- it cannot (without infinite processing power), give us back the same data/document used to generate the hash.

When two different pieces of data generate the same hash value, it's referred to as a _collision_. This is one of the potential issues that can occur when using some hashing algorithms such as MD5.

Some practical uses of hashing include:

- Verifying the integrity of downloaded content
- Password verification
- Signature generation and verification
- Proof-of-work
- File or data identification

### Digital Signatures

_Digital signatures_ are electronic, encrypted stamps of authentication that can accompany emails, messages, or other electronic documents.

Digital signatures utilize public/private keys and hashing to help us verify the "who" and "what" of data/documents.

In other words, these digital signatures can help us to confirm that the information sent originated from the sender and has not been altered.

### DNS Overview

The _Domain Name System_ (DNS) can be thought of as the phonebook of the internet.

Historically, if you knew someone's name you could look up their phone number in the phonebook.

Likewise, if we know a website's domain name, DNS can find the IP address of that website's server for us.

Here are some key terms related to DNS:

- **Top-Level Domain (TLD)** -- This is the final part of the domain name such as .com, .org, .net, etc.
- **DNS Zone** -- A portion of the DNS namespace that is managed by a specific organization or administrator.
- **DNS Record** -- A domain name along with its corresponding IP address.
- **Root Servers** -- There are currently 13 root servers in operation that handle requests for information about top-level domains.
- **Top-Level Domain Servers (TLD Servers)** -- Receives requests from the root server to find information about its specific TLD type. For example, the .org TLD server will help to find where .org TLD are located.
- **Zone Files** -- Zone files are the way that name servers store information about the domains they know about.
