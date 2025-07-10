# IntroToLAN
Notes regarding the Local Area Network Topologies

**Topology** is referred to the design of a network.


### Star Topology

Star topology is a network setup in which each device is connected to a central node called a hub. The hub manages the data flow between the devices.

<img title="star topology" alt="Star Topology" style="text-align:center" src="https://upload.wikimedia.org/wikipedia/commons/8/84/Star_Topology.png" width="400">


### Bus Topology

A bus topology relies on a single backbone cable to connect all devices within the network. This configuration resembles the structure of a tree, where devices (the leaves) branch off from the main cable (the trunk).

While this setup is straightforward, it can quickly become a bottleneck. Since all data traffic travels along the same cable, simultaneous requests from multiple devices can lead to significant slowdowns. This congestion complicates troubleshooting, as it becomes challenging to pinpoint which device is experiencing issues when all data flows through a single route.

Despite these drawbacks, bus topologies are among the easiest and most cost-effective to implement. The reduced expenses associated with cabling and the minimal need for specialized networking equipment make them an attractive option for many applications.

However, a notable disadvantage of bus topology is its lack of redundancy. The reliance on a single backbone cable creates a single point of failure; if this cable is damaged, all connected devices lose their ability to transmit or receive data, disrupting the entire network.

### Ring Topology

Ring topology, also known as token topology, features a unique configuration where devices, such as computers, are connected in a closed loop. This design minimizes cabling requirements and reduces reliance on dedicated hardware compared to star topologies.

In a ring topology, data is transmitted around the loop until it reaches its intended destination. Each device forwards the data to the next device in the loop. Notably, a device will only relay data it receives from another device if it does not have its own data to send. If it does have data to transmit, it prioritizes its own transmission before passing along any received data.

The unidirectional flow of data in a ring topology simplifies troubleshooting, as identifying faults is relatively straightforward. However, this characteristic also presents a downside; the data must often pass through multiple devices before reaching its destination, which can lead to inefficiencies in data transmission.

Additionally, ring topologies are generally less susceptible to bottlenecks compared to bus topologies, as they do not experience high volumes of simultaneous traffic. However, this design does have a critical vulnerability: if a cable is cut or a device fails, the entire network can become inoperable, disrupting communication for all connected devices.

### Router

##### What a Router is. 

Routers are the traffic officers of Internet. Routers forward data packets between computer networks. The most popular ones, at home or the office, do forward IP packets between home ocmputers and the internet. They decide the best path to exchange the information packs.

##### What do they do.

- Redirection of data packets to the right device in your network

- Local network connection to the global internet

- Wireless devices point

##### Which parts a router has.

Ports: 

- LAN Ports. The ones used to connect the wired devices: computers, consoles.

- WAN Port. Is the one router to the internet services providers.

- Antenas. Crucial to distribute the WI-FI signal throughout your home or work space.

- Memory processor. it handles all the data settings and traffic.

#### OSI (Open System Interconnaection Model)

<img title="star topology" alt="Star Topology" style="text-align:center" src="https://tryhackme-images.s3.amazonaws.com/user-uploads/5de96d9ca744773ea7ef8c00/room-content/6d17472b87f8792dadde3bb06aa1fdaa.svg" width="400">

The **OSI** is a model used in networking. This model provides a framework dictating how all networked devices will send, recive and interpret data.

The process to succeed using this framework is called *Encapsulation*

##### Physical (Layer 1)

This layer refers to the physical components of the hardware used in networking: Ethernet cables, routers, modems...

##### Data Link (Layer 2)

*The data link layer focuses on the physical addressing of the transmission. It receives a packet from the network layer (including the IP address for the remote computer) and adds in the physical MAC (Media Access Control) address of the receiving endpoint. Inside every network-enabled computer is a Network Interface Card (NIC) which comes with a unique MAC address to identify it.*

*Layers of Networking*: Networking is often conceptualized in layers, with each layer having specific functions. The data link layer is one of these layers, sitting just above the physical layer (which deals with the actual transmission of data over physical media) and below the network layer (which handles routing data between devices).

*Packets and Addresses*: When data is sent over a network, it is broken down into smaller units called packets. The network layer is responsible for packaging this data and assigning it an IP address, which is a logical address used to identify devices on a network.

*Physical Addressing*: The data link layer adds another layer of addressing called the MAC (Media Access Control) address. While the IP address is used for routing data across networks, the MAC address is used for communication within the same local network. Each network-enabled device has a Network Interface Card (NIC) that has a unique MAC address assigned to it. This MAC address is like a postal address for the device on the local network.

*Role of the NIC*: The NIC is the hardware component that allows a computer to connect to a network. It is responsible for sending and receiving data over the network. The unique MAC address on the NIC ensures that data sent over the local network reaches the correct device.

*Process*: When a device wants to send data to another device on the same local network, it first gets the IP address of the destination device. The data link layer then converts this IP address into a MAC address (if it doesn't already have it) and adds it to the packet. This packet is then sent over the physical medium (like Ethernet cables or Wi-Fi) to the destination device.

In summary, the data link layer is crucial for ensuring that data packets are delivered to the correct device within a local network by using MAC addresses, while the network layer handles the broader task of routing packets across different networks using IP addresses.

##### Network (Layer 3)

**Overview of the Network Layer**

The network layer is essential for routing data packets across networks. It evaluates various paths based on criteria like distance, reliability, and speed, using IP addresses to identify devices. Routers, as Layer 3 devices, play a critical role in this process, ensuring that data reaches its destination efficiently and reliably.

*Purpose of the Network Layer*: The primary role of the network layer is to facilitate the routing of data packets from the source to the destination across multiple networks. It takes care of determining the best path for data to travel, ensuring that it reaches the correct endpoint efficiently.

*Routing*: Routing is the process of selecting the best path for data packets to travel through a network. The network layer uses various algorithms and protocols to determine this optimal path based on several criteria.

Key Factors in Routing
When determining the best route for data packets, the network layer considers several factors:

*Shortest Path*: The route with the least number of hops (devices or routers) that the packet must pass through is often preferred. Fewer hops generally mean less latency and faster delivery.

*Reliability*: The network layer also assesses the reliability of the paths. If certain paths have a history of packet loss or other issues, they may be avoided in favor of more reliable routes.

*Speed of Connection*: The physical medium used for the connection can impact speed. For example, fiber optic connections are typically much faster than copper connections. The network layer may prefer routes that utilize faster connections to enhance overall performance.

*IP Addresses and Layer 3 Devices*
IP Addresses: At the network layer, devices are identified using IP addresses (like 192.168.1.100). These addresses are crucial for routing packets across different networks, as they provide a logical way to identify devices.

*Layer 3 Devices*: Routers are the primary devices that operate at the network layer. They are responsible for forwarding packets based on their IP addresses. Because they function at this layer, they are referred to as Layer 3 devices.

*Routing Protocols*
While we don’t need to dive deeply into the specifics of routing protocols at this stage, it’s good to know that there are various protocols that help routers determine the best paths for data. Some common ones include:

*OSPF* (Open Shortest Path First): A link-state routing protocol that uses a method of calculating the shortest path based on the current state of the network.

RIP (Routing Information Protocol): A distance-vector routing protocol that uses the number of hops as its primary metric for determining the best path.




