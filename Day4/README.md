I am granting executables permisiions to the /tmp/fushioncorp.sh script on app server 2.Additionally ensurring that all users have capabilities to execute 

steps...
ssh into server 2 
cd /tmp/ 
chmod 755 /tmp/xfusioncorp.sh
ls -l /tmp/xfusioncorp.sh
expected outcome -rwxr-xr-x 1 root root 40 Apr 29 15:52 /tmp/xfusioncorp.sh

2