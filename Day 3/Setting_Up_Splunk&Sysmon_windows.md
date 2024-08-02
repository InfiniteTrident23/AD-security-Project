# Active Directory Project

## Day 3: Installing and Configuring Splunk and Sysmon on Windows Target and Server Machine

I will be listing steps for Target Machine, you can following along and try to repeat these steps on the Windows Server  for practice.

### Steps:

1. Open Windows Target Machine
  
2. Open Settings > System > About
   
3. (This is an optional step, but will be helpful in recognizing pc later) Now, lets rename our machine to `Target-PC`
   
4. Go to [Splunk](https://www.splunk.com) again and log in with your credentials.
   
5. Download the Splunk Universal Forwarder for your machine from there.
    
6. Run the downloaded file as administrator.
   - It will start installing the service
   - When prompted, create a user: admin
   - And allow random password generation.
   - Let Splunk install
  
7. While Splunk is installing, we can install Sysmon on our machine
  - Download sysmon from [sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
  - Now for this project, we will be requiring the sysmon configuration file by Olaf, which has been attached in Day 3 folder or can be downloaded from [here](https://github.com/olafhartong/sysmon-modular/blob/master/sysmonconfig.xml).
  - Once Sysmon is downloaded, extract all files and make sure that the config file is in the same directory as the files after extraction.

8. To set-up Sysmon
  - Copy paths of the extracted folder
  - Search **Windows PowerShell** on the Target-PC and run as administrator
  - cd to the copied path
  - Run: `./sysmon64 -i <config file name>`

9. Now we need to instruct our machine, as to what we need to send over to Splunk, because if we send over all the logs of a machine, it will be too much for us to filter and study from later.
  - To do this, we need to edit the `inputs.conf` file of Splunk.
  - location of file: `c:\Program Files\SplunkUniversalForwarder\etc\system\default`, HOWEVER, we should not change the DEFAULT configurations, or in an case of discrepency everything might go haywire, so we go to directory: `c:\Program Files\SplunkUniversalForwarder\etc\system\local` instead, which only stores our local machine configs.
  - Now place the inputs.conf file attached in the day 2 folder, or create it from [here](https://github.com/MyDFIR/Active-Directory-Project). \

10. Now we need to open Services on our machine.

11. Find `SplunkUniversalForwarder`, check the `Log On As` column
  - If the log on values is `NTSYSTEM`, Then we need to change this
  - Double click on the service
  - Go to Logs > Select log on as local system
  - and Apply

12. Stop the `SplunkUniversalForwarder` service and then start it again for the changes to take place.

13. Log on to the Splunk portal, running on ubuntu machine at port 8000.

14. Log in with ubuntu machine credentials.

15. Go to Settings > Indexes

16. Create new index with name `endpoint`

17. Go to Settings again > forwarding and receiving
  - Do configure receiving
  - Add new port
  - Add port 9997, which is default port for Splunk (This was also mentioned at the time of splunkForwarder setup)

18. Go to Apps and search `index="endpoint"`

19. If everything was setup correctly, we would start seeing reports and logs, and you can see your `Target-PC` in the "sources" section.



