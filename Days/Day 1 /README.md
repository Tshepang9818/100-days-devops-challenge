So here I created a user named Javed with a non-interactive shell on app server 3 
Steps I took to create this 
- ssh into server3
- created a user with non active shell with  useradd -s /sbin/nologin javed 
- verified with grep javed /etc/passwd
