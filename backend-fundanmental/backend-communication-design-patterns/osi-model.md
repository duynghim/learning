## OSI Model (Open Systems Interconnection Model)

### Why do we need a communication model?

#### Agnostic Application
* Without a standard model, your application must have knowledge of the underlying network medium
* Imagine if you have to author a different version of your apps so that it works on Wi-Fi vs. ethernet vs. LTE vs. Fiber
#### Network Equipment Management
* Without a standard model, upgrading network equipment becomes difficult 
#### Decoupled Innovation
* Innovations can be done in each layer separately without affecting the rest of the models

#### What is the OSI Model
* 7 Layers each describe a specific networking component
* Layer 7 - Application - HTTP/FTP/gRPC
* Layer 6 - Presentation - Encoding, Serialization
* Layer 5 - Session - Connection establishment, TLS
* Layer 4 - Transport - UDP/TCP
* Layer 3 - Network - IP
* Layer 2 - Data link - Frames, Mac Address Ethernet
* Layer 1 - Physical-Electric signals, fiber, or radio waves

#### Detailed Explanation of the 7 Layers of the OSI Model
##### Layer 7: Application Layer
This is the layer closest to the end user, providing network service services directly to the application.

###### Key characteristics:
* Interfaces with end-user software applications
* Provides protocols that allow software to send and receive information
* Identifies communication partners
* Determine resource availability
* Synchronizes communication

###### Common protocols:
* HTTP/HTTPS (Web Browsing)
* FTP (File Transfers)
* SMTP (Email)
* DNS (Domain Name Resolution)
* gRPC (Remote Procedure Calls)
* Telnet and SSH (Remote Access)

Example functionality: When you open and visit a website, the Application layer handles the HTTP requests and response
between your browser and the web server.

##### Layer 6: Presentation Layer
This layer prepares data for the Application layer, handling format and encryption.

###### Key characteristics
* Translates data between application and network formats
* Handles data compression and encryption/decryption
* Ensures data is readable by the receiving system
* Manages data syntax processing

###### Common functions:
* Character encoding/decoding (ASCII, Unicode)
* Data compression (ZIP, JPEG)
* Encryption/decryption (SSL/TLS - though spanning multiple layers)—SSL(Secure Socket Layer)—TLS(Transport Layer Security)
* Format conversion
* Serialization of complex data structures

Example functionality: When you send an image in a messaging app, the Presentation layer might
compress it and convert it to a standard format before transmission.

##### Layer 5: Session Layer
This layer establishes, manages, and terminates connections between applications.

###### Key characteristics:
* Creates and maintains session between applications.
* Manages dialog control (who can transmit and when)
* Provides synchronization points for long data transfers
* Handles session checkpointing and recovery

###### Common protocols and functions:
* NetBios
* RPC (Remote Procedure Call)
* Session establishment, maintenance, and termination
* Session authentication and reconnection
* TLS handshake processes (Though TLS spans multiple layers)

Example functionality: When you make a video call, the Session layer establishes the connection between
your device and the recipient's device, maintaining it throughout the call.

##### Layer 4: Transport Layer
This layer provides end-to-end communication services for data transfer between endpoints.

###### Key characteristics:
Ensures complete data transfer
Handles segmentation and reassembly of data
Controls flow and provides error checking
Manages reliability through connection-oriented or connectionless protocols

###### Key protocols:
TCP (Transmission Control Protocol) - connection-oriented, reliable
* Establishes connections before sending data
* Guarantees delivery and correct ordering
* Handles flow control and congestion control

UDP (User Datagram Protocol)—connectionless, less reliable but faster
* No connection establishment
* No guarantee of delivery, ordering, or duplicate protection
* Lower overhead, higher speed

Example functionality: When downloading a file, TCP ensures all packets arrive and are reassembled in the
correct order. For streaming video, UDP might be used to prioritize speed over perfect reliability.

##### Layer 3: Network Layer
This layer handles routing of data packets across different networks

###### Key characteristics:
Determines the best path for data to travel from source to destination
Manages logical addressing (IP Addresses)
Routes packets across multiple network
Handles traffic control and congestion management

###### Key protocols and functions:
IP (Internet Protocol) - IPv4 and IPv6
ICMP (Internet Control Message Protocol)
Routing protocols (OSPF, BGP, RIP)
Packet forwarding and routing
Subnet Division and addressing
Example functionality: When you access a website hosted on another continent. The Network layer determines
the best path for your data packets to travel across multiple routers and networks to reach the destination.

##### Layer 2: Network Layer
This layer provides node-to-node transfer between two directly connected nodes.

###### Key characteristics:
* Handles physical addressing (MAC addresses)
* Detects and potentially corrects errors from the Physical layer
* Control how data is placed and received on the medium
* Organized into sublayer:
  + Logical Link Control (LLC): Error and flow control
  + Medical Access Control (MAC): Addressing and channel access

###### Key protocols and technologies:
* Ethernet
* Wi-Fi (802.11)
* PPP (Point-to-Point Protocol)
* MAC addressing
* Frame traffic control
* VLAN tagging
Example functionality: When your computer sends data to your router over Wi-Fi. the Data Link layer packages the data
into frames with the correct MAC addresses and manages the wireless transmission protocol

##### Layer 1: Physical Layer

This is the lowest layer, dealing with the physical connection between devices

###### Key characteristics:
* Defines physical specifications for devices
* Transmits raw bit streams over physical medium
* Handles signal transmission and reception
* Defines cables, cards, and physical aspects

###### Key parts and technologies
* Hardware: cables, switches, network interface cards
* Transmission model: simplex, half-duplex, full-duplex
* Physical topologies: bus, star, mesh, ring
* Electrical specifications: voltage levels, timing
* Physical data rates
* Transmission media: copper wire, fiber optic, wireless

Example functionality: when data moves through an Ethernet cable, the Physical layer converts the digital bit to
electric signals, manages voltage levels, and handles the timing of the signal transmission

##### Data Flow Through the OSI Layers
1. When data is sent across a network:
2. It starts at the Application layer of the sending device
3. Moves down through all layers, with each layer adding its own information
4. Travels across the physical network
5. Moves up through the layers of the receiving device
6. Reaches the Application layer of the receiving device

Each layer communicates with its counterpart on the receiving device, creating a logical communication between peer layers.  

This layered approach allows complex networking tasks to be divided into simpler components, enabling different technologies
to work together seamlessly















