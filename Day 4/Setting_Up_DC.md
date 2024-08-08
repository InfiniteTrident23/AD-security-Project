# Active Directory Project

## Day 4: Setting up an Active Directory with a Domain Controller server

### Steps:
1. We need to log in to our Windows Server machine.

2. Once we log in, we are greeted with the Server Manager application.

3. Select `Manage` and then `Add roles and features`.

4. Select `Role based or feature based installation`.

5. In the `Select Server roles`, select `Active Directory Domain Services`.

6. Let it finish up installation.

7. After it, select the flag ico on the top bar (besides the `Manage` button).

8. Click on `Promote this server to Domain Controller` to make the server a designated Domain Controller.

9. Then, click on `Add new Forest`
    - You can specify a domain, for exam, I used the domain `infinitehax.local`
    - I left all the settings as default, but you can customize to your needs.
    - Set a password and a domain name.\
  
10. Now, go to `Tools`

11. Select `Active directory Computer and users`

12. Right click on the domain, and select `create new Organizational Unit`, and you can make a new group, such as IT, HR, Sales, etc.
    = Make a new user in the Organizational Unit

13. Now we have completed the setup of the Active Directory, and can add users as per your needs!
    
