# IntroToLAN
Notes regarding the Local Area Network Topologies

**Topology** is referred to the design of a network.


### Star Topology

Star topology is a network setup in which each device is connected to a central node called a hub. The hub manages the data flow between the devices.

<img title="star topology" alt="Star Topology" style="text-align: center" src="https://upload.wikimedia.org/wikipedia/commons/8/84/Star_Topology.png" width="400">


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

<img title="star topology" alt="Star Topology" style="text-align: center" src="https://tryhackme-images.s3.amazonaws.com/user-uploads/5de96d9ca744773ea7ef8c00/room-content/6d17472b87f8792dadde3bb06aa1fdaa.svg" width="400">
