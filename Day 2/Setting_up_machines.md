# Active Directory Project

## Day 2: Setting Up Virtual Machines and Configurations

On the second day, I set up the virtual machines and configured the necessary components for the Active Directory project. Below is a detailed breakdown of the steps and configurations performed:

### Components:

1. **Windows 11 (Pro) Host:**
   - Created a virtual machine running Windows 10 Pro.
   - The Pro version is required as the Home edition does not support Active Directory features.
   - Configured the machine to obtain an IP address via DHCP.

2. **Kali Linux Attacker Machine:**
   - Created a virtual machine running Kali Linux.
   - Assigned a static IP address: 192.168.10.250.
   - This machine will be used for penetration testing and security assessments.

3. **Windows Server 2022:**
   - Created a virtual machine running Windows Server 2022.
   - Configured as the Domain Controller for the network.
   - Installed Active Directory Domain Services (AD DS).

4. **Splunk Server:**
   - Created a virtual machine running Ubuntu 22.04 Server.
   - Installed Splunk Enterprise for log management and analysis.

### Steps and Configurations:

1. **Creating Windows 11 (Pro) Virtual Machine:**
   - Downloaded and installed the Windows 11 Pro ISO.
   - Set up the virtual machine with the necessary hardware requirements.
   - Configured network settings to obtain an IP address via DHCP.

2. **Creating Kali Linux Attacker Machine:**
   - Downloaded and installed the Kali Linux ISO.
   - Set up the virtual machine with the necessary hardware requirements.
   - Assigned a static IP address: 192.168.10.250.

3. **Creating Windows Server 2022 Domain Controller:**
   - Downloaded and installed the Windows Server 2022 ISO.
   - Set up the virtual machine with the necessary hardware requirements.
   - Installed and configured Active Directory Domain Services (AD DS).
   - Promoted the server to a Domain Controller.

4. **Creating Splunk Server:**
   - Downloaded and installed the Ubuntu 22.04 Server ISO.
   - Set up the virtual machine with the necessary hardware requirements.
   - Installed Splunk Enterprise.
   - Configured Splunk for initial setup and prepared it for receiving logs.

5. **Make sure all the machines are on the same NAT network**
   - (If you are using virtualbox) Go to Tools > NAT Networks > Create
   - Specify a name for the network, and specify IP address pool for the machines, along with a CIDR notation.
   - ![image](https://github.com/user-attachments/assets/ab685239-2a57-43f6-8676-0752e322ab4d)
