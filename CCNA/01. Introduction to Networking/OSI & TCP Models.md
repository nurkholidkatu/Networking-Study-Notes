# TCP/IP vs OSI Model

In computer networking, there are two models that are very important: the **OSI model** and the **TCP/IP model**.  
The topic *“TCP/IP vs OSI”* is often discussed, so let’s understand how these two models are different.  

---

## OSI Model

The **OSI model (Open System Interconnection)** was created by the International Organization for Standardization (ISO).  
It was designed as a **reference model** to explain how a communication system should work.  

The OSI model gives a framework for:  
- Building networking standards  
- Designing devices  
- Explaining how applications on different computers can communicate through a network  

The OSI model has **seven layers**, and each layer describes a specific function of data traveling through the network.  
The layers are usually numbered starting from the bottom (the **Physical layer** as Layer 1).  

👉 Many people remember the order of these layers with the sentence:  
**“Please Do Not Throw Sausage Pizza Away”**  

### OSI Layers Diagram  
![OSI](https://github.com/user-attachments/assets/7d0e7c21-75fa-4640-86d4-b5b2a860cf28)


### OSI Layers Explained
1. **Physical Layer (Layer 1)** – Defines how to send bits (0s and 1s) from one device to another. It includes cables, connectors, and network cards.  
2. **Data Link Layer (Layer 2)** – Wraps packets into frames.  
   - **Header**: Contains source and destination MAC addresses.  
   - **Trailer**: Contains error-checking information.  
   - Has two parts:  
     - **Logical Link Control (LLC)**: Flow control and error detection  
     - **Media Access Control (MAC)**: Hardware addressing and access control  
3. **Network Layer (Layer 3)** – Defines device addressing (like IP addresses), routing, and path selection.  
4. **Transport Layer (Layer 4)** – Splits data into segments, controls the connection between computers, ensures reliable delivery, and error recovery.  
5. **Session Layer (Layer 5)** – Manages sessions, starting and ending communication between two systems.  
6. **Presentation Layer (Layer 6)** – Defines data formats, compression, and encryption.  
7. **Application Layer (Layer 7)** – The closest to the user. Allows applications (like browsers, email, etc.) to communicate over the network.  

➡️ Example: HTTPS is called an **Application Layer (Layer 7) protocol**.  
➡️ Devices are also often described by OSI layers, e.g. a **Layer 2 switch** or a **Layer 7 firewall**.  

---

## TCP/IP Model

The **TCP/IP model** was created in the 1970s by DARPA (Defense Advanced Research Project Agency).  
It is an **open and public model** that provides general guidelines for building and implementing computer networks.  

The TCP/IP model has **four layers**:  
![TCPIP](https://github.com/user-attachments/assets/7e085c56-5f5d-454c-9f4c-e539c0400db4)


1. **Network Access Layer** – Defines the hardware and protocols to deliver data physically over the network.  
2. **Internet Layer** – Defines how packets are transmitted logically over the network (e.g., IP addressing and routing).  
3. **Transport Layer** – Defines protocols for reliable communication, transmission quality, and error-free delivery (e.g., TCP, UDP).  
4. **Application Layer** – Defines protocols for communication between applications, and provides services for software (e.g., HTTP, FTP, SMTP).  

---

## Comparing TCP/IP vs OSI

The following diagram shows the comparison between the OSI and TCP/IP models:  
<img width="1000" height="500" alt="1715655975494" src="https://github.com/user-attachments/assets/46172420-8e60-4fdf-88cf-b6bed769e880" />


- The **TCP/IP model has 4 layers**, while the **OSI model has 7 layers**.  
- In TCP/IP:  
  - The **Application, Presentation, and Session layers** of OSI are combined into one layer (**Application layer**).  
  - The **Physical and Data Link layers** of OSI are combined into one layer (**Network Access layer**).  
- The OSI model is more detailed and prescriptive (it says exactly what should happen at each step).  
- The TCP/IP model is more practical and descriptive (it explains how communication happens but with fewer details).  

👉 In simple words:  
- **OSI model = theory (a reference guide, more detailed)**  
- **TCP/IP model = practice (the actual model used in the Internet today)**  
