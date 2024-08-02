# Active Directory Project

## Day 3: Installing and Configuring Splunk service on Ubuntu server

### Steps:

1. Open Splunk Server:
   - Start the Splunk server machine.

2. Give Static IP to machine:
   - To do so, Open the network configuration file
     `sudo nano /etc/netplan/00-installer-config.yaml`
   - Now edit the contents of the file to get Static IP on your ubuntu machine.
      - ![image](https://github.com/user-attachments/assets/b9970753-667f-4566-9e8d-9feacd9565ba)
      - **Note: The IP should be according to your network plan.

3. Sign Up at splunk.com:
   - Create an account at [Splunk](https://www.splunk.com).

4. **Go to Products > Free Trial > Enterprise > Download the .deb File:**
   - Navigate through the menu to download the Splunk Enterprise .deb file.

5. Save the File in your project directory:

6. Now we need to make the project folder shared with the ubuntu machine, to access the Splunk file
   - Go to Virtual Machine > Device > Shared Folder
   - Add a new folder and check all the boxes after adding the project folder.

7. In order to mount the folder to the virtual machine, we need to install VirtualBox Guest Additions:
   - `sudo apt-get install virtualbox-guest-additions-iso`
   - Now reboot the system to let the changes take place.

8. Log Back in the machine
   
9. Run command: `sudo apt-get install virtualbox-guest-utils`
 
10. Now we need to add a new user named vboxsf: `sudo adduser infinitehax vboxsf` (Make sure to put your machine username)
 
11. Make a new directory named `share`

12. Mount the shared folder to the newly created directory:
   - 	`sudo mount -t vboxsf -o uid=1000,gid=1000 AD_Project share/` (Replace your project folder name)
   - 	
13. Now we need to build the splunk iso file that we downloaded from Splunk.com
   - `sudo dpkg -i <splunk iso file>`

14. Change directory to /opt/splunk

15. Change user to User Splunk
   - `sudo -u splunk bash`
16. Change directory to bin.

17. Now we need to run the splunk file to run the installation: `./splunk start` and give it a few mins to finish installation, depending on your machine.

18. Exit out of user Splunk
    
19. We need to make sure, that the Splunk service starts on its own at boot time, and we dont have to do all these series of steps to start it everytime we turn off out machine, so we do the following:
   - `cd bin`
   - `sudo ./splunk enable boot-start -user splunk`

20. We have successfully installed Splunk service on our machine!





