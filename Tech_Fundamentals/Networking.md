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

## Other Networking Concepts

### IP Addresses & IP Conversions

It's possible to convert from dotted decimal IPs to binary IPs (and vice versa if necessary).

This is because both addresses are 32 bits and divided into four parts containing 8 bits each (these parts can be referred to as octets).

Each octet is separated by a period.

### IP Addressing v4

All IP addresses have a "network" part and a "host" part.

If the network component of two IP addresses match, then those two devices are local. If not, the two devices are remote.

IP addresses need to be unique both globally and locally.

### Subnet Mask

A _subnet mask_ is a dotted decimal version of a binary number that indicates which part of an IP address is the network and which part is the host.

Subnet masks can help a host determine if an IP address it needs to communicate with is local or remote.

### Address Resolution Protocol

The _Address Resolution Protocol_ (ARP) is a communication protocol for determining the MAC address of a given IP address.

### Routers, Routes & Route Tables

_Routes_ are used to determine where a packet should be forwarded to.

_Route tables_ are simply tables containing many routes.

_Routers_ help move packets from a source to a destination -- encapulating the packets in different layer 2 frames along the way.
