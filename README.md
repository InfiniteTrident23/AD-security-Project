# <p align="center">AD-security-Project</p>
<p style="display: flex; justify-content: space-between;"><img src= "https://github.com/user-attachments/assets/2ae489cb-adf9-430c-bb55-8c5666ee772e" style="width:200px;height:150x;"><img src="https://github.com/user-attachments/assets/fb307bac-3b2e-4d29-be2a-c5fdcb6d00d0" style="width:300px;height:200x;"><img src= "https://github.com/user-attachments/assets/8bdd6321-20b3-4a80-9260-7cac29afb03a" style="width:300px;height:200x;"></p>

### Summary

**Overview:**
This project involves setting up and securing a network environment using Active Directory, Splunk, Sysmon, and Atomic Red Team. The goal is to create a simulated network, configure logging and monitoring, and test security measures.

**Components:**
1. **Logical Diagram:**
   - Created a network diagram to visualize the setup.

2. **Virtual Machines:**
   - **Windows 11 Pro Host:** Target machine.
   - **Kali Linux Attacker:** Used for penetration testing.
   - **Windows Server 2022:** Configured as the Domain Controller.
   - **Ubuntu 22.04 Server:** Installed Splunk for log management.

3. **Configurations:**
   - **Splunk:** Installed and configured for centralized log management.
   - **Sysmon:** Deployed on both the server and target machine for detailed system monitoring.
   - **Active Directory (AD):** Set up on the Windows Server to manage network resources and security.

4. **Implementation Steps:**
   - **Day 1:** Built a detailed logical diagram of the network setup.
   - **Day 2:** Set up the virtual machines.
   - **Day 3:** Installed and configured Splunk, and deployed Sysmon.
   - **Day 4:** Promoted the Windows Server to Domain Controller and added the Windows 11 machine to the AD.
   - **Day 5:** Conducted a brute-force attack using Kali Linux and Crowbar, and ran security tests with Atomic Red Team.

**Tools Used:**
- **Splunk:** For monitoring and analyzing machine data.
- **Sysmon:** For logging system activity.
- **Atomic Red Team:** For testing security measures by simulating adversary techniques.
- **Crowbar:** For brute-force attack testing.

**Purpose:**
This project aims to enhance understanding and skills in Active Directory, network security, and data analysis. It simulates a real-world network environment to test and validate security measures.

Feel free to explore the project files and detailed steps in the repository.
