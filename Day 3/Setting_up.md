# Active Directory Project

## Day 3: Installing and Configuring Splunk and Sysmon

### Steps:

1. **Open Splunk Server:**
   - Start the Splunk server machine.

2. **Edit IP to Give Static IP:**
   - To do so, Open the network configuration file
     `sudo nano /etc/network/interfaces`
   - 

3. **Sign Up at splunk.com:**
   - Create an account at [Splunk](https://www.splunk.com).

4. **Go to Products > Free Trial > Enterprise > Download the .deb File:**
   - Navigate through the menu to download the Splunk Enterprise .deb file.

5. **Store the File in AD_Project Directory:**
   - Save the downloaded file in the `AD_Project` directory.

6. **Go to Virtual Machine > Device > Shared Folder:**
   - Add a new folder and check all the boxes after adding the project folder.

7. **Install VirtualBox Guest Additions:**
   ```sh
   sudo apt-get install virtualbox-guest-additions-iso
