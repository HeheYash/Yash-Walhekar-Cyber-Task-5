# Yash-Walhekar-Cyber-Task-5

## Wireshark Packet Analysis

### Objective
To capture live network packets using Wireshark and identify basic protocols. 

### Process
1.  Started a Wireshark capture on the active network interface. 
2.  Generated network traffic by browsing websites and using the `ping` command. 
3.  Stopped the capture and used display filters to isolate specific protocols. 

### Protocols Identified

At least three protocols were successfully identified: 
**1. DNS (Domain Name System)**
* **What is DNS?**
   
  Think of DNS as the "phone book of the internet". Its main job is to translate human-readable domain names (like `google.com`) into machine-readable IP addresses (like `172.217.14.228`).
* **Finding:** Filtered for `dns` to observe queries from my PC requesting the IP address for a domain name.
* **Screenshot:**
    ![DNS Filter](DNS.png)

**2. UDP (User Datagram Protocol)**
* **Finding:** Filtered for `udp`. The DNS queries were transported using UDP, as seen in the packet details.
* **Screenshot:**
    ![UDP Filter](UDP.png)

**3. TCP (Transmission Control Protocol)**
* **Finding:** Filtered for `tcp`, revealing the three-way handshake (SYN, SYN-ACK, ACK) used to establish a reliable connection for web browsing.
* **Screenshot:**
    ![TCP Filter](TCP.jpg)

**4. TLS (Transport Layer Security)**
* **Finding:** Filtered for `tls`. This protocol encrypted my web browser traffic (`https`), which is why `http` packets were not visible.
* **Screenshot:**
    ![TLS Filter](TLS.png)

### Deliverables
This repository contains:
* `Cyber Internship Task 5.pcap`: The raw packet capture file.
   ![Wireshark Output File](Cyber%20Internship%20Task%205)
* `README.md`: This summary report.
* Screenshots of the filtered protocols. 
