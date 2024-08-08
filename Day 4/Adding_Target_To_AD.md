# Active Directory Project

## Day 4: Adding Target PC to the Active Directory

1. Open the Target-PC and log in

2. Open `settings`, then `about`

3. Navigate to `Advanced System Settings`

4. Select `Computer name` > `change`

5. Select Domain

6. Now, if you put in the domain name, it will give the error saying that the Domain Controller cannot be contacted, this is because the Target PC does not know how to resolve the domain name yet, because our Domain Controller is not registered in the DNS Service.

7. To resolve this, Open `Control Panel`, and go to Network settings.

8. Double click on the network adapter.

9. Then `Properties`

10. Double click on `IPv4 settings`

11. And add the Domain Controller's IP in the DNS field as primary, and add your main DNS as the secondary DNS.

12. Now try adding the PC to AD again.

13. Use administrators credetials.

14. Give it a few minutes to finish, and the PC will be added to the Active Directory!

15. Try Logging into the Target PC with one of the credentials we made earlier, and try out various properties which were specified for the user!
