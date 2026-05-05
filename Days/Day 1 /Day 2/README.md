Today what I did is 
As part of the temporary assignment to the Nautilus project, a developer named ravi requires access for a limited duration. To ensure smooth access management, a temporary user account with an expiry date is needed. Here's what you need to do:



Create a user named ravi on App Server 3 in Stratos Datacenter. Set the expiry date to 2027-02-17, ensuring the user is created in lowercase as per standard protocol.    

So what I did is 
1.SSH to the server
 - ssh
 2.Create the user with expiry and home directory
 - sudo useradd -m -s /bin/bash -e 2027-02-17 ravi 
 3.Set an initial password
 - I added the public key to /home/ravi/ .ssh/authorized_keys and set  ownership
 4. Verification 
 - sudo chage -l ravi 

 for worrkflow  refer to screenshots section