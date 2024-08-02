# Active Directory Project

## Day 1: Building a Logical Diagram

On the first day, I created a logical diagram to visualize the network setup for the project using <a href= "draw.io">draw.io</a>. This diagram includes the various components and their interactions within the network. Below is a detailed explanation of each component and their roles:

![image](https://github.com/user-attachments/assets/35ef0387-7e49-4f13-ac79-1a607541f843)


### Components:

1. **Domain: InfiniteHax**
   - **Network:** 192.168.10.0/24
   - **Splunk Server:** 192.168.10.10
   - **Active Directory:** 192.168.10.7

2. **Splunk Server (192.168.10.7)**
   - Responsible for log management and analysis.
   - Receives logs from various machines in the network.

3. **AD Server (192.168.10.10)**
   - Acts as the Active Directory server for the network.
   - Uses Splunk Universal Forwarder and Sysmon for forwarding logs to the Splunk server.

4. **Target Machine**
   - **OS:** Windows 11
   - **IP:** DHCP
   - Uses Splunk Universal Forwarder and Sysmon for log forwarding.
   - Runs Atomic Red Team for security testing.

5. **Attacker Machine**
   - **OS:** Kali Linux
   - **IP:** 192.168.10.250
   - Used for penetration testing and attacks on the target machine.

6. **Router**
   - Connects the internal network to the Internet.

7. **Layer 2 Switch**
   - Connects all devices within the internal network.

### Network Flow:

- The **Splunk Server** forwards logs to the **AD Server**.
- The **AD Server** and the **Target Machine** send logs to the **Splunk Server** for centralized logging and analysis.
- The **Attacker Machine** is connected to the network for performing security tests and attacks on the **Target Machine**.
- All devices are interconnected via the **Layer 2 Switch**, which also connects to the **Router** for Internet access.

This logical diagram serves as the foundation for the subsequent steps in the project, providing a clear overview of the network structure and the relationships between different components.

---

Feel free to explore the project further as I document each day's activities and configurations.
