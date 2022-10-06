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
