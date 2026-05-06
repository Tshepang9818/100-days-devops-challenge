Question:
The system admins team of xFusionCorp Industries has set up some scripts on jump host that run on regular intervals and perform operations on all app servers in Stratos Datacenter. To make these scripts work properly we need to make sure the thor user on jump host has password-less SSH access to all app servers through their respective sudo users (i.e tony for app server 1). Based on the requirements, perform the following:



Set up a password-less authentication from user thor on jump host to all app servers through their respective sudo users.

how I tackled this task:
-ssh-keygen -t rsa -b 4096 -C "thor@jump_host"
-ssh-copy-id tony@stapp01
-ssh-copy-id steve@stapp02
-ssh-copy-id banner@stapp03
(This appends Thor's public key to /.ssh/authoized_keys file of each target user)

Verification:
ssh tony@stapp01

How I ensure permissions are correct on each app server
-chmod 700 ~/.ssh
-chmod 600 ~/.ssh/authorized_keys
(This ensures SSH respects the key value)