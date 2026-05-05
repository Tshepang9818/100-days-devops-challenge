Here I am tasked to to disable direct login  on all app servers within stratas data centre.This is a standard hardening step to reduce attack surface.

1.Shh
- sudo vi /etc/ssh/sshd_config
2.Find root permit
- Changed the Permit RootLogin prohibit-password and change it to no
3.Restart ssh
-systemctl restart sshd
4. verification
- ssh into that server and t showed "permission denied"