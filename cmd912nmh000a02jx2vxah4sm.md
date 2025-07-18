---
title: "Week 2: Basic Networking concepts required for DevOps: Part 1"
datePublished: Fri Jul 18 2025 16:22:59 GMT+0000 (Coordinated Universal Time)
cuid: cmd912nmh000a02jx2vxah4sm
slug: week-2-basic-networking-concepts-required-for-devops-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1752855254839/0dd441e6-0669-4c25-8a6b-37fa4ad92119.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1752855513138/2b320bbf-4fc2-4251-b20b-73d6763eb8e3.jpeg
tags: linux, devops, networking, networkingbasics, hashnodedevopsjourney

---

After diving into the basics of DevOps, this week I focused on fundamental Linux commands and foundational networking concepts—a crucial step for any aspiring DevOps engineer.

## 2.1 What is Linux?

Linux is an open-source operating system widely used for servers, development environments, and cloud platforms. Its command-line interface (CLI) is powerful, allowing users to manage files, processes, and system resources efficiently.

```bash
ls     # Lists all the files
cd     # Changes current directory
mkdir  # Creates a new directory
touch  # Creates a new empty file
cp     # Copies files or directories
mv     # Moves or renames files
cat    # Displays contents of a file 
echo   # Prints a line of text
pwd    # Prints current directory
clear  # Clears the terminal
```

**KodeKloud** provides a lab that replicates a Linux environment where you can practice these commands without installing Linux on your local machine. We’ll learn more about Linux commands and how to install Linux locally later in the blogs.

## 2.2 Let's Dive Into Networking Basics

### 2.2.1 What is Networking?

Networking refers to the practice of connecting computers and other devices to share resources, exchange data, and enable communication.

As a DevOps engineer, it's essential to understand networking because modern applications are distributed — running across multiple servers, containers, and cloud environments.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1752852248128/f18cbc10-cfb9-4796-9064-25d90b8b0079.png align="center")

> 📌 The Internet is essentially a massive collection of interconnected computer networks.

> 💡 Fun Fact:  
> The full form of *COMPUTER* blew my mind:  
> **Common Operating Machine Purposely Used for Technological and Educational Research**

### 2.2.2 How It All Started?

* **Late 1960s**: The journey began with *ARPANET*, which connected four universities in the U.S.
    
* Recognized limitations eventually led to the invention of the **World Wide Web (WWW)**.
    
* **WWW**: A system of interlinked hypertext documents and multimedia content accessed via browsers, using URLs and hyperlinks.
    
* Web resources are transferred using protocols like **HTTP (Hypertext Transfer Protocol)**.
    

### 2.2.3 What is a Protocol?

A **protocol** is a set of rules and standards that ensure proper communication in a computer network.

Just like a country has laws and regulations, the Internet relies on organizations like [**Internet Society**](https://www.internetsociety.org/) to define and manage these protocols.

### 2.2.4 Network Topologies

**Network topology** describes how devices are arranged in a network, influencing data flow and resiliency. Here are the most common types:

* **Bus Topology**: All devices share a single communication line. Main con: A cable failure brings down the entire network.
    
* **Ring Topology**: Devices form a closed loop; data moves in one direction. Main con: High cost and poor scalability.
    
* **Star Topology**: Devices connect to a central hub or switch. Main con: If the hub fails, the network goes down.
    
* **Mesh Topology**: Each device connects to every other device; robust but expensive and complex.
    
* **Hybrid Topology**: Combinations of the above, tailored for specific needs.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1752852568984/d972a5ac-77dc-48c6-aee7-95b65e701879.jpeg align="center")

## 2.3 Layers of Communication

### 2.3.1 OSI Model: Open System Interconnection Model

The OSI model is a conceptual framework that describes how data travel through a network - from the user’s application all the way down to the physical cables (and back up again on the other side).

It helps in:

* Understanding how networking works step-by-step.
    
* Troubleshooting communication issues
    
* Designing modular network systems.
    

**7 layers of OSI Model are:**

* Application layer
    
* Presentation Layer
    
* Session Layer
    
* Transportation Layer
    
* Network Layer
    
* Data Link Layer
    
* Physical Layer
    

Lets talk little bit about all of these layers:

1. **Application Layer**: User’s directly interact with this layer for example: when you interact with browser, whatsapp, or any other client-based application. This layer provides user-facing applications and networking services. Protocols that are used at this layers are:
    
    1. HTTP/HTTPS
        
    2. FTP
        
    3. SMTP
        
    4. DNS
        
2. **Presentation Layer**: At this layer, the data is converted to machine-oriented language, encryption and decryption works at this level and also data compression happens at this layer.
    
3. **Session Layer**: This layer is responsible for setting up connection and enables sending and receiving of data followed by termination of connected sessions. At this stage, authentication and authorization takes place.
    
4. **Transportation Layer**: This layer receives data from session layer and then it takes care of the data using its protocol like TCP, UDP. This layer has 3 main important role to play:
    
    1. Segmentation: It divides the data in segments and assigns port number and sequence number. On the other side this layer helps in reassembling of the data.
        
    2. Flow control: It handles the flow of data between client and server. It controls the flow of data on both the sides.
        
    3. Error control: Works on error detection and recovery if any data packet gets lost.
        
5. **Network Layer**: It works for transmission of data between different computers that are present in different networks. Logical Addressing and IP addressing are assigned at this layer. This layer determines the best path for data between devices on different networks.
    
6. **Data Link Layer**: This layer packages bits into frames and vice versa, handles MAC addressing and points point-to-point node delivery. It helps in directly communicating with the computer.
    
7. **Physical Layer**: The hardwares are involved at this stage. Transmits raw bits ( 0 and 1 ) over physical media like cables or radio signals.  
    

### 2.3.2 TCP/IP Model

The TCP/IP model is the practical framework that describes how data is actually transmitted over the internet. The OSI model is the conceptual framework that standardizes the function of a network in 7 days.

TCP/IP Model simplifies the OSI Model and breaks it into 5 layers:

* Application Layer
    
* Transport Layer
    
* Network Layer
    
* Data Link Layer
    
* Physical Layer
    

Below is a structure that displays how two computer communicates using TCP/IP Model:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1752854393979/76f5f6d8-a45e-4fa0-86d4-e80ddf19b348.png align="center")

### 2.4 How Your Device Talks to the Internet??

### \- IP Address

An **IP address** is a unique identifier for each device on a network. Your **ISP** (Internet Service Provider) gives you a **modem** with a **global IP address**. That modem assigns **local IPs** to devices in your home.

So, when **Device 1** sends a request to **Google**, the modem (via NAT - Network Address Translation) routes the response back to the correct device.

### \- Ports

Your device might have multiple applications communicating at once. **Ports** (16-bit numbers) ensure that responses go to the correct app. Think of it like this:

* **Device = IP Address**
    
* **Application = Port Number**
    

Together, they make up a unique endpoint like: `192.168.0.2:3000`

👉 Your ISP (Internet Service Provider) is connected to the global network which provides internet to the ISP. This ISP gives you a modem which is connected to various devices which are present in your house. This Modem has a Global IP Address which connects with the internet. All devices connected to this modem will have same Global IP Address. This modem assigns local IP address to devices suppose Device 1, Device 2 and Device 3. When your device suppose Device 1 sends a request to Google then your ISP uses this global IP address to send a request to Internet. Once response is received the modem decides whom to send the response via NAT (Network Access Translator). But what about within device? I mean once the response is received by your device how does your device decide which application send the request. It is done by the Ports. Device has IP address and application or processes inside devices has port numbers.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1752854809116/829f965c-60a5-496e-a459-7fe2fa46a904.png align="center")

Lets take a deep dive into layers:

## Application Layer in Depth:

The top layer in the network architecture is the application layer where user interacts with the application. It provides services and interfaces that enable software applications to communicate over the network. Common protocols in the application layer are HTTP/HTTPS, SMTP, FTP, DHCP etc.

### Architectures:

* **Client-Server**: Client-Server architecture is an example of application layer where client sends a request to server and servers sends a response back to the client.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1752854933707/fcb38b8d-9473-4a60-a421-c216a53c796b.png align="center")
    
* **Peer-to-Peer (P2P)**: Peer-2-peer architecture is an example of application layer where every node can act as clients and servers, for example utorrent where peers/seeds can be added to increase the upload and download speed.
    

* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1752854957028/114e4857-b7dc-4012-9617-7ee6e4058aba.png align="center")
    

### **HTTP (Hyper Text Transfer Protocol):**

It is a client-server protocol that tells that how you can send a request to server and how the server will send response back to the client. It is an application-layer protocol used for transmitting data on the world wide web.

* HTTP uses TCP as transport layer because it needs to send all the information.
    
* TCP or Transmission Control Protocol is one of the main transport layer protocols used in computer networking. Its job is to reliably deliver data between devices over a network. TCP make sure that all the data are transmitted to the receiver without any data packet loss.
    
* UDP or User Datagram Protocol is a transport layer protocol used to send messages called datagrams, without establishing connection. Its fast but unreliable - meaning it does not guarantee delivery, order, or data integrity. Examples include video conferencing.
    

It is a stateless protocol that means it does not remember previous interactions by default.

You can send request to the server using some common HTTP methods which are as follows:

* GET: Retrieve data from the server
    
* POST: Send data to the server
    
* PUT: Update or replace data
    
* PATCH: Partially update data
    
* DELETE: Delete data from the server
    

Once the server sends response back some codes are followed which are:

* 1XXX : Informational Status Codes
    
* 2XXX: Success Status Codes
    
* 3XXX: Redirecting Status Codes
    
* 4XXX: Client Error
    
* 5XXX: Server Error
    

This was all that I learnt in this week about networking. This is Part 1, Part 2 will come on next friday so just stay tuned.

### Coming Up Next Friday – Week 3: Basic Networking Concepts: Part 2

Stay tuned for a deep dive into:

* How Email Works
    
* DNS
    
* CDN / VPN
    
* Subnetting
    
* Firewalls