# Network Fundamentals

## **`What’s a Network ?`**

a network is a collection of interconnected devices,
such as computers, servers, printers,
etc…that can communicate and share resources with each other.
These devices are linked together through various communication channels,
such as wired (e.g., Ethernet cables..) or wireless (e.g., Wi-Fi) connections

## **`What’s the purpose of a network ?`**

the purpose from a network is to be enable to transfer date,
and share resources, and communicate among the connected devices.

## **`what’s the network types ?`**

the most two common types of computer network is :

- **Local Area Network (LAN)**
    
    Local Area Network is a computer network that connects devices within a
  “limited geographical area” (Covers a local area of 1km) such as a home,
  office building, school… LANs are commonly used to enable communication
   and share resources between devices like computers, printers, servers, etc…
    
- **Wide Area Network (WAN)**
    
    > Wide Area network is a computer network that connects
    >  devices in a “large geographical area” (Between states, countries …),
    > typically connecting multiple local area networks (LANs)
    > together.allowing organizations and individuals to communicate and share data over long distances.
    > 

there are some other types of computer networks like : **WAN**(Campus area network),
**MAN**(Metropolitan Area Network)..

## **`what’s the network topologies ?`**

Network topologies refer to the physical or logical layout of a computer network.
They define how devices, nodes, and links are connected to each other within the network.
there are many topologies the most common ones are :

- **Bus topology :** All devices are connected to a single communication line
- (called the   **backbone cable**), and if the backbone failed the entire network may be affected.

    
    https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9832db87-666d-48e2-8eef-bf0168934d2a/bus.png
    
- **Ring Topology :** Each device is connected to exactly two other devices
    
    (https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a4f77206-7042-42a6-9da5-12e47ddcbe03/ring.webp)
    
- **Star Topology :** In a star topology, all devices are connected directly to a central hub or switch.
    
    ![star.webp](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7f6a38d3-ec5d-41e5-9999-71b2adc38ae4/star.webp)
    
- **Mesh topology :** Each device is connected to every other device in the network,
- creating **redundant “وفرة”** paths for data transmission (but expensive af).
- so we can that only between switches or routers. (if you delete one or more cables you get **Half Mesh**)

![Mesh.webp](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8118ca30-1387-4c35-87ed-474ae6adb3ae/Mesh.webp)

We can combine these topologies to get a **Hybrid Topology** for example :

![hybrid.webp](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3f775bf2-d7f5-43e2-bec6-d41babd24d07/hybrid.webp)

## **`What’s the Network Devices out there ?`**

Network devices are hardware components or equipment
used to facilitate communication and data exchange within a computer network.
These devices play specific roles in the network infrastructure,
enabling devices and users to connect, share resources, and communicate effectively.
Here are some common network devices:

- **Network card / NIC / Network adapter :**
    
    A Network Interface Card, also known as network card or network adapter,
    is a hardware component installed in a computer or device that enables it to connect to a network.==
  NICs support various network technologies, such as Ethernet or Wi-Fi. here are some common NIC speeds for Ethernet :
    
    - Ethernet 10mb/s (Megabits per second).
    - Fast Ethernet 100mb/s.
    - GigaEthernet 100mb/s.
        
        ![Network-Interface-Card-Example-1.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4cd5214f-56ad-484b-b529-7ded353e38f0/Network-Interface-Card-Example-1.jpg)
        
    
    Each NIC has a **unique** identifier assigned to it called **MAC address**.
    
    ### **MAC address :**
    
    > A MAC address, short for "Media Access Control" address,
    > is a hardware address (**physical address**) that serves as a permanent
    >  and unique identifier for a device on a local area network (LAN) or a wide area network (WAN).
    > Every network device, such as computers, routers, switches, smartphones, and other networked devices,
    > has a unique MAC address.
    > 
    
    and it’s **48 bits** long and typically represented in **hexadecimal format** with six groups of two characters each.
    
    ![l-adresse-mac-1618209718-GYzYSMPm46.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1f477dfe-a906-4f2a-bf96-26fb8af5ef2a/l-adresse-mac-1618209718-GYzYSMPm46.jpg)
    
    The **uniqueness** of MAC addresses is ensured through the assignment process,
governed by the Institute of Electrical and Electronics Engineers (IEEE).
the first three groups of characters (OUI) are assigned by the IEEE.
and the last three groups of characters (NICs) are assigned by the vendor.
    
- **Hub** :
    
    a hub is simple network device that connects multiple devices in a local area network (LAN).
  Its primary function is to facilitate data transmission between devices by **broadcasting**
  incoming data **packets** to all connected devices. Hubs operate at the physical layer (Layer 1) of the **OSI model**.
    
    When a hub receives data from one device, it replicates and sends that data to all
  other devices connected to its **ports**. This process is known as **"data flooding"** or
  "**data broadcasting.**" It means that all devices on the hub's network segment receive all the data,
  regardless of whether it is intended for them or not.
    
    due to their limited functionality and broadcast nature, hubs have largely been replaced by **`switches`**.
    
    hubs are **[half duplex](https://www.blackbox.co.uk/gb-gb/page/25069/Resources/Technical-Resources/Black-Box-Explains/Fibre-Optic-Cable/Simplex-vs-duplex-fiber-patch-cable/)** devices,
  means only one device can transmit data at a time VLANs improve network security and efficiency.
        
        ![Switch-MAC-Table.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7335d681-8be5-4e0b-9587-5ce9d4b90942/Switch-MAC-Table.png)
        
    
- **Router :**
    
    A router is a network device that connects different networks together and directs data packets between them,
  serving as a gateway. Routers operate at the network layer (Layer 3) of the **OSI model**.
    
    Routers are commonly used to connect local area networks (LANs) to the Internet,
    allowing devices on the LAN to communicate with external networks and access online resources.
    
    Routers can be hardware devices or software-based solutions that perform similar functions.
    
    A typical router performs these primary functions:
    
    1. **IP Routing:** Routers determine the best path for data packets
    2. to travel from the source to the destination across the network.
    3. They do this by analyzing the destination IP address in the packet
    4. header and using routing algorithms and tables to find the optimal route.
    5. **Network Address Translation (NAT):** NAT is a mechanism used by
    6. routers to map private IP addresses to a single public IP address,
    7. enabling devices within a LAN to share a common public address for
    8. Internet access. NAT helps conserve public IP addresses and adds a layer of security to the internal network.
    9. **Firewall Functionality:** Many routers include built-in firewall
    capabilities that can filter traffic based on source, destination, port,
protocol, or other criteria. These firewalls provide an additional layer of
security by protecting the internal network from unauthorized access and potential threats.
    11. **VPN Support:** Some routers offer Virtual Private Network (VPN) support,
    12. allowing secure remote access to the internal network from outside locations.
    13.  VPNs create encrypted tunnels through which data can travel securely over the Internet or other public networks.
    14. **Wireless Access:** Many routers include wireless functionality,
    15. enabling devices to connect to the network without physical cables.=
    Wireless routers provide Wi-Fi access and can support various security protocols such as WPA and WPA2.
        
        ![Router.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0d0e49a0-196e-475b-8e63-f6e5d88e2fa3/Router.png)
        
    
- **Gateway :**
    
    A gateway is a network device that serves as an interface between two different networks,
  translating communication protocols, data formats, or network architectures.
  Gateways operate at multiple layers of the **OSI model** and can function as routers,
  switches, or a combination of both. They enable devices on different networks to
  communicate with each other, even if they use different protocols or technologies.
    
    Gateways can be implemented as software applications, hardware devices,
  or a combination of both. They provide essential services for network integration and interoperability.
    
    Gateways are commonly used in scenarios where different networks need to communicate, such as:
    
    - Connecting a Local Area Network (LAN) to the Internet using different protocols.
    - Facilitating communication between legacy systems and modern network infrastructure.
    - Enabling integration between different voice and data networks, such as VoIP gateways.
    
    ![Gateway.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/95318b75-304b-408c-809a-f06a43e4f848/Gateway.png)
    

## **`What’s the OSI Model ?`**

The OSI (Open Systems Interconnection) Model is a conceptual framework that
standardizes the functions and processes of a network into seven distinct layers.
This model serves as a guide for designing, troubleshooting, and understanding networking architectures.

The seven layers of the OSI Model are:

1. **Physical Layer (Layer 1):** Deals with the physical transmission of
   raw bits over the network medium. This layer includes cables, switches,
   hubs, and other physical elements that make up the network.
2. **Data Link Layer (Layer 2):** Ensures error-free data transmission between
   devices on the same network segment. It includes MAC addressing,
   frame error detection, and collision management.
3. **Network Layer (Layer 3):** Handles routing and packet forwarding between different networks.
. This layer includes the IP addressing scheme, routers, and other related components.
4. **Transport Layer (Layer 4):** Ensures reliable data delivery by establishing, maintaining ,
     and terminating connections. It includes error recovery, flow control, and multiplexing.
5. **Session Layer (Layer 5):** Manages sessions between applications, ensuring proper communication and synchronization.
6. **Presentation Layer (Layer 6):** Translates data formats between applications and the transport layer. It deals with data compression, encryption, and format translation.
7. **Application Layer (Layer 7):** Provides network services to end-users and applications.
   It includes protocols like HTTP, FTP, SMTP, and other user interfaces.

The OSI model helps to understand the role and functionality of different network
devices and how they interact with each other. It is important to note that the
OSI model is a theoretical construct, and real-world networking protocols may not align precisely with its structure.

![OSI-Layers.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/032e7e4f-cf89-4f62-8766-3c9c577eb108/OSI-Layers.png)

## **`What’s the TCP/IP Model ?`**

The TCP/IP (Transmission Control Protocol/Internet Protocol) Model
is a set of networking protocols that govern the operation of the Internet.
It simplifies the OSI model into four layers, with the primary
focus on providing end-to-end communication and host-to-host networking.

The four layers of the TCP/IP Model are:

1. **Network Interface Layer (Equivalent to OSI Layers 1 & 2):** Includes
2. the physical and data link layers, dealing with hardware components, MAC addressing, and data framing.
3. **Internet Layer (Equivalent to OSI Layer 3):** Responsible for packet
4. routing and IP addressing.
5. **Transport Layer (Equivalent to OSI Layer 4):** Ensures reliable data
6. transmission by managing connections, error recovery, and flow control. TCP and UDP are examples of transport layer protocols.
7. **Application Layer (Equivalent to OSI Layers 5, 6 & 7):** Provides
8.  network services to applications, combining the functions of the OSI's session, presentation, and application layers.

The TCP/IP model is widely used in modern networking, forming the basis of 
the Internet's architecture. While it may not map perfectly to the OSI model, 
both models serve as valuable tools for understanding and working with network technologies.

![TCP-IP-Layers.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/32e6f6cd-d3ca-4e6d-a253-3822a20057c7/TCP-IP-Layers.png)

## **`What’s the main Internet protocols ?`**

The Internet is governed by a wide variety of protocols that facilitate 
communication and data exchange across different networks. Here are some of the main Internet protocols:

- **IP (Internet Protocol):** Provides the basic framework for
- delivering data packets from the source to the destination, utilizing 

    ![SwitchDiagram.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/75186a95-bc40-4dfe-a47d-0e84e2a61b5c/SwitchDiagram.png)
    
- **Router :**
    
    a router is a network device that connects and directs data packets
  between different networks, such as a LAN to a WAN or the Internet.
  It operates at the network layer (Layer 3) of the **OSI model**.
    
    a router's primary functions are :
    
    - **Routing:** Routers determine the best path for data packets to travel
    -  between different networks. They use **routing tables** and
    -  **routing protocols** to dynamically calculate the optimal path for data transmission.
    - **Network Segmentation:** Routers can divide a network into different
    - **subnets** and isolate them to manage traffic and enhance security.
    - **Network Address Translation (NAT):** Routers perform NAT to translate
    -  private IP addresses into a public IP address, allowing devices within
    -   a private network to communicate with external networks (e.g., the Internet).
    - **Firewall Functionality:** Routers can incorporate firewall features
    -  to filter traffic and provide security against malicious attacks.
    - **Dynamic Host Configuration Protocol (DHCP):** Routers often include
    - DHCP functionality to automatically assign IP addresses to devices on the network.
    - **Virtual Private Network (VPN) Support:** Routers may support VPNs,
    -  allowing secure remote access to a local network.
    - **Wireless Connectivity:** Many routers include wireless functionality,
    - acting as a wireless access point to connect Wi-Fi-enabled devices.

    ![router.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9282767a-02f1-4713-8c91-e648e5b8f5a0/router.png)
    
    Some routers are designed to handle specific tasks, such as enterprise-level routing, home networking, or edge routing.
    
    routers provide **convergence** by integrating multiple services and technologies,
  such as voice, video, and data, within a single network.

- **Access Point (AP) :**
    
    An access point (AP) is a network device that allows wireless devices,
  such as laptops, smartphones, and tablets, to connect to a wired network using Wi-Fi.
  It acts as an interface between wireless devices and the wired LAN, enabling data communication and network access.
    
    access points are used in various environments, including homes, offices,
  airports, hotels, and other public places, to provide Wi-Fi connectivity.
    
    Some features of access points include :
    
    - **SSID Broadcasting:** Access points broadcast a Service Set Identifier (SSID),
    - which is a unique name for the wireless network.
    - This allows users to identify and connect to the desired network.
    - **Encryption and Security:** Access points can offer various encryption methods
    -  (e.g., WEP, WPA, WPA2) to secure data transmission and network access.
    - **Multiple Input Multiple Output (MIMO):** MIMO technology allows access
    points to use multiple antennas for simultaneous data transmission and reception, improving performance and range.
    - **Guest Networking:** Some access points offer guest networking features,
    - allowing visitors to connect to the internet without gaining access to the internal network.
    - **Quality of Service (QoS):** Access points can provide QoS features to
    -  prioritize specific types of data traffic, ensuring optimal performance for high-demand applications like voice or video.
    - **PoE (Power over Ethernet) Support:** Many access points support PoE,
    - enabling them to receive both power and data through a single Ethernet cable, simplifying installation.

    ![Access-Point.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7a5c786f-e3ad-49e0-acc0-93d24e895c7e/Access-Point.jpg)

- **Modem :**
    
    a modem is a network device that modulates and demodulates digital signals,
   allowing data transmission over analog communication lines like telephone
  lines or cable systems. Modems are commonly used to connect computers and other devices to the Internet or other remote networks.
    
    Modems can be found in various types, such as:
    
    - **Dial-up Modems:** Use telephone lines to connect to the Internet, with relatively slow data rates.
    - **DSL Modems:** Utilize telephone lines as well but offer higher data rates than dial-up modems.
    - **Cable Modems:** Connect to the Internet via cable television lines, offering even faster data rates.
    - **Fiber-Optic Modems:** Used with fiber-optic communication lines, providing the highest data rates.
    
    ![modem.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/42ad3d4d-6dc1-4bb6-85aa-9e5986f34394/modem.png)
    
    Modems are often combined with routers in a single device to provide both modulation/demodulation and routing functions.

- **Firewall :**
    
    a firewall is a network security system that monitors and controls
  incoming and outgoing network traffic based on predetermined security rules.
   Firewalls can be implemented as hardware devices, software programs, or a combination of both.
    
    firewalls act as barriers between trusted internal networks and untrusted external networks,
  such as the Internet. They enforce access controls,
  filtering data packets based on parameters like source and destination IP addresses, protocols, ports, and other criteria.
    
    Types of firewalls include :
    
    - **Packet-Filtering Firewalls:** Examine packets and allow or block them based on predefined rules.
    - **Stateful Inspection Firewalls:** Track the state of active connections and apply rules accordingly.
    - **Proxy Firewalls:** Act as intermediaries between users and external servers, providing a layer of isolation.
    - **Next-Generation Firewalls (NGFWs):** Offer advanced features like intrusion prevention, application-level filtering, and more.

    ![firewall.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9c071ed3-38d2-4a30-8c00-7a9e49b04846/firewall.png)
    
    Firewalls play a crucial role in network security, protecting data,=
  devices, and users from unauthorized access, attacks, and other malicious activities.

- **Gateway :**
    
    a gateway is a network device that serves as a bridge between different networks
   allowing data to flow between them. Unlike routers, which typically connect similar networks,
   gateways enable communication between networks using different protocols or architectures.
   A gateway can be implemented as a dedicated hardware device, software application, or a combination of both.
    
    Gateways perform protocol translation, converting data formats and communication
  methods to enable interoperability between networks. They act as entry and exit points for data,
   facilitating communication and ensuring that data is appropriately translated for the target network.
    
    Examples of gateways include :
    
    - **VoIP Gateways:** Enable voice communication between traditional telephone networks and IP-based networks.
    - **Email Gateways:** Manage and filter email traffic between internal and external email servers.
    - **Cloud Gateways:** Provide a bridge between on-premises data centers and cloud services, enabling seamless data transfer.
    - **IoT Gateways:** Facilitate communication between IoT devices and the central network, providing processing and security functions.

    ![Gateway.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/70fb842b-e236-401d-a147-109bdf1cbb6c/Gateway.png)
    
    Gateways are vital for ensuring connectivity and compatibility between heterogeneous networks, enhancing flexibility, and supporting various applications and services.

- **Switch :**
    
    a switch is a network device that connects multiple devices within a Local Area Network (LAN).
  It operates at the data link layer (Layer 2) of the **OSI model** and selectively forwards data packets between devices based on their MAC addresses.
    
    switches are essential for reducing collisions and enhancing the efficiency of network communication.
  They segment the network into individual collision domains, allowing simultaneous data transmission between devices.
    
    Types of switches include :
    
    - **Unmanaged Switches:** Simple plug-and-play devices with no configuration required.
    - **Managed Switches:** Offer advanced features like VLANs, Quality of Service (QoS),
    -  and security settings, allowing for customized configuration.
    - **Smart or Hybrid Switches:** Provide a balance between unmanaged and managed switches,
    - offering some advanced features with limited configuration options.
    - **Multilayer Switches:** Perform functions at both Layer 2 and Layer 3,
    -  combining switching and routing capabilities.

    ![switch.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d4a08d92-9344-43c9-9a7e-88bd165ea667/switch.png)
    
    switches play a crucial role in building and maintaining efficient and scalable LANs,
  allowing for high-speed communication between devices and minimizing network congestion.

- **Load Balancer :**
    
    a load balancer is a device or software application that distributes
  network or application traffic across multiple servers, ensuring optimal resource utilization,
   maximizing throughput, and minimizing response time.
    
    By balancing the load, it helps in achieving high availability, reliability,
   and performance of services. If one server becomes overloaded or fails,
   the load balancer redirects traffic to other healthy servers, maintaining uninterrupted service.
    
    Types of load balancing methods include :
    
    - **Round Robin:** Distributes requests evenly among available servers.
    - **Least Connections:** Sends requests to the server with the fewest active connections.
    - **IP Hashing:** Directs requests from the same IP address to the same server, maintaining session persistence.
    
    ![Load-Balancer.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5e1adfa6-cdf8-49d6-a537-780146f27b02/Load-Balancer.png)
    
    Load balancers can be found in various environments,
   from data centers to cloud infrastructures, playing a vital role in ensuring
   seamless and efficient operation of applications and services.

These network devices collectively enable the creation, operation,
and management of complex network infrastructures. They provide the essential functions
required for data transmission, connectivity, security, scalability, and performance, 
catering to the diverse needs of users, businesses, and organizations across various domains and industries.


### Networking Cables

Networking cables are integral components that enable devices to communicate within a computer network. 
They facilitate the transfer of data between devices such as computers, switches,
routers, and servers. Here's a detailed look at some common types of networking cables:

#### 1. Ethernet Cables

Ethernet cables are the standard cables used for most wired networks. 
They are classified into various categories based on performance and characteristics:

- **CAT5 (Category 5):** Supports speeds up to 100 Mbps with a maximum length of 100 meters. Commonly used in older networks.
- **CAT5e (Category 5e):** An enhanced version of CAT5, supports speeds up to 1 Gbps with reduced crosstalk.
- **CAT6 (Category 6):** Supports up to 10 Gbps over short distances, offering higher performance and reduced interference.
- **CAT6a (Category 6a):** An advancement over CAT6, offering the same 10 Gbps speed but up to 100 meters.
- **CAT7 (Category 7):** Known for high-speed data transfer up to 10 Gbps and enhanced shielding to reduce interference.

These cables typically consist of twisted pairs of copper wires and are commonly used to connect devices in a Local Area Network (LAN).

#### 2. Coaxial Cables

Coaxial cables are constructed with a central conductor surrounded by insulation, a metallic shield, and an outer layer:

- **RG-6:** Commonly used for residential cable internet and TV.
- **RG-59:** Often used for video applications and CCTV.
- **RG-11:** Used for long-distance connections.

Coaxial cables are known for their durability and resistance to signal interference, 
making them suitable for broadband internet connections.

#### 3. Fiber-Optic Cables

Fiber-optic cables transmit data as light signals through thin strands of glass or plastic.
They come in two main types:

- **Single-Mode Fiber (SMF):** Transmits a single ray of light, suitable for long distances and high speeds.
- **Multi-Mode Fiber (MMF):** Allows multiple light paths, typically used for shorter distances.

Fiber-optic cables offer very high-speed connections, resistance to electromagnetic interference, 
and have the capacity for carrying large amounts of data. They are often used for internet backbones, 
data center connections, and in areas requiring high-speed data transmission.

### Conclusion Of Networking Cable

Understanding the different types of networking cables and their applications is essential 
in selecting the right cable for specific network requirements. From traditional Ethernet to 
advanced fiber-optic connections, each cable type offers unique characteristics and benefits, 
tailored to various networking environments and needs.


![Networking Cables](https://www.google.com/url?sa=i&url=https%3A%2F%2Fipcisco.com%2Flesson%2Fnetwork-cabling%2F&psig=AOvVaw3XNrBDuZJQj6yrSU7K3wo6&ust=1691662875018000&source=images&cd=vfe&opi=89978449&ved=0CBEQjRxqFwoTCMDBwLitz4ADFQAAAAAdAAAAABAD)

## OSI Model

The OSI (Open Systems Interconnection) Model is a conceptual framework that standardizes 
the functions of a telecommunication or computing system into seven abstraction layers.

#### Sending Data

1. **Application Layer**
    - **Sender:** Encodes user data into network format, such as HTTP for web browsing.
    - Example: Writing an email in a web browser.

2. **Presentation Layer**
    - **Sender:** Converts data into a common format, like ASCII, and may compress or encrypt the data.
    - Example: Encrypting the email text.

3. **Session Layer**
    - **Sender:** Establishes, maintains, and terminates connections (sessions) between applications.
    - Example: Creating a connection to the email server.

4. **Transport Layer**
    - **Sender:** Divides data into segments, adds error checking, and ensures reliable data delivery.
    - Example: Breaking the email into packets and numbering them for proper reassembly.

5. **Network Layer**
    - **Sender:** Adds logical addressing (e.g., IP addresses) and routes data to its destination.
    - Example: Adding the recipient's IP address and finding the best route.

6. **Data Link Layer**
    - **Sender:** Encapsulates data into frames with error-checking and controls access to the physical network.
    - Example: Adding a MAC address and checking for errors in the frame.

7. **Physical Layer**
    - **Sender:** Converts data into electrical, optical, or radio wave signals for transmission.
    - Example: Sending the data through an Ethernet cable.

#### Receiving Data

1. **Physical Layer**
    - **Receiver:** Translates physical signals into binary data.
    - Example: Receiving the data through an Ethernet cable.

2. **Data Link Layer**
    - **Receiver:** Decapsulates frames, checks for errors, and controls access to the physical network.
    - Example: Checking the frame for errors and stripping the MAC address.

3. **Network Layer**
    - **Receiver:** Reads the logical addressing and routes data to its destination within the network.
    - Example: Reading the IP address and sending the data to the correct device.

4. **Transport Layer**
    - **Receiver:** Reassembles data segments into the original data stream, with error checking.
    - Example: Reassembling the email packets in the correct order.

5. **Session Layer**
    - **Receiver:** Manages the connection between applications, possibly terminating it when complete.
    - Example: Managing the connection to the email server.

6. **Presentation Layer**
    - **Receiver:** Converts data back into its original format and may decrypt or decompress the data.
    - Example: Decrypting the email text.

7. **Application Layer**
    - **Receiver:** Decodes the network data into user data, such as displaying an email in a web browser.
    - Example: Displaying the received email.

### Conclusion Of OSI Moedl

The OSI Model provides a framework for understanding how data is processed and transmitted over a network. 
By breaking down the process into seven distinct layers, it allows for complex
interactions to be understood and managed in a standardized way.
Whether sending or receiving data, each layer of the OSI Model plays a crucial
role in ensuring that the information reaches its destination correctly and efficiently.


### TCP/IP Model

#### 1. Link Layer (Network Interface Layer)

This layer is responsible for the physical connection between devices. 
It includes the hardware elements involved in connecting to a network, such as network interface cards, switches, and cabling.

- **Frame Creation:** Data packets are framed with necessary headers and trailers that contain addressing information.
- **Physical Transmission:** The data frames are transmitted over the physical medium (e.g., Ethernet cable, Wi-Fi).

#### 2. Internet Layer (IP Layer)

This layer is responsible for logical addressing and routing of data packets. Key protocols and components:

- **IP (Internet Protocol):** Assigns logical addresses (IP addresses) to devices and handles routing between them.
- **ICMP (Internet Control Message Protocol):** Used for error handling and diagnostics.
- **Routing:** Routers determine the best path for data packets based on destination IP addresses.

#### 3. Transport Layer

This layer ensures reliable data transfer between devices, with two main protocols:

- **TCP (Transmission Control Protocol):** Ensures reliable,
- ordered delivery by establishing connections, performing error checking,
- and retransmitting lost packets.
  - **Handshake:** Connection establishment uses a three-way handshake (SYN, SYN-ACK, ACK).
  - **Data Transfer:** Segments data into manageable chunks, sends, and ensures delivery.
  - **Termination:** Connection is closed using a four-way handshake.

- **UDP (User Datagram Protocol):** Provides connectionless, faster data transfer without error checking.
  - **Usage:** Suitable for real-time applications like VoIP, where occasional lost packets are acceptable.

#### 4. Application Layer

This layer includes user-facing protocols and applications that rely on underlying network services.

- **HTTP, HTTPS:** Used for web browsing.
- **FTP, SFTP:** File transfer protocols.
- **SMTP, POP3, IMAP:** Email protocols.
- **DNS:** Domain name resolution to IP addresses.

### Conclusion Of TCP/IP

The TCP/IP model is a fundamental framework that enables diverse devices to communicate over a network. 
Understanding how each layer works and interacts with the others is essential in network design, 
troubleshooting, and security. Visual diagrams and hands-on labs can further deepen this understanding.


![TCP/IP Model](https://www.google.com/url?sa=i&url=https%3A%2F%2Fvelog.io%2F%40amuse%2FOSI-7-Layers&psig=AOvVaw1WgeYdf-ZCUr9Puh7yM4nA&ust=1691663171116000&source=images&cd=vfe&opi=89978449&ved=0CBEQjRxqFwoTCJjz5cWuz4ADFQAAAAAdAAAAABAI)

### Why TCP/IP is Needed

- **Standardization:** Enables different systems to communicate.
- **Reliability:** TCP ensures that data is reliably transmitted.
- **Scalability:** Suits a wide range of applications, from small networks to the entire Internet.

## Subnetting

Subnetting is dividing an IP network into subnetworks. 

### Why Use Subnetting

- **Improved Network Performance:** Reduces traffic.
- **Enhanced Security:** Isolates parts of the network.
- **Ease of Management:** Simplifies network configuration.

### How Subnetting Works

- Dividing the IP address into a network and host portion.
- Using a subnet mask to determine the network address.

![Subnetting](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.techtarget.com%2Fsearchnetworking%2Fdefinition%2Fsubnet&psig=AOvVaw3_nq-38Qu19PnRmEZTMSQB&ust=1691662792299000&source=images&cd=vfe&opi=89978449&ved=0CBEQjRxqFwoTCIDiv5Ktz4ADFQAAAAAdAAAAABAP)

## IP Addresses

An IP address identifies a device on a network.

### IP Address Classes

- **Class A:** Large number of hosts, fewer networks.
- **Class B:** Balance between hosts and networks.
- **Class C:** More networks, fewer hosts.

### IPv4 vs IPv6

- **IPv4:** 32-bit address, e.g., 192.168.1.1
- **IPv6:** 128-bit address, e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334

### Difference

- IPv6 provides a larger address space.
- IPv6 has simplified header format.
- IPv6 improves routing efficiency.

### Examples

- Class A: 10.0.0.1
- IPv4: 192.168.1.100
- IPv6: 2001:0db8:85a3:0000:0000:8a2e:0370:7334

These topics provide a comprehensive view of networking essentials, from physical connections to advanced networking concepts such as subnetting and IP addressing.
