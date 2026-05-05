There is a security audit and the security team has opted to enhance application and server security with SELINUX on Server 2 so I need to install required Selinux packages,permanantly disable SELINUX for the time being as it will reenable after config changes and final status should be disabled

sudo dnf install selinux-policy selinux-policy-targeted policycoreutils (This ensures core selinux tools and policies are present)
Permanantly dsabling SElinux without rebooting.I achieve this by editing config file sudo vi /etc/selinux/config change SELINUX=enforcing to =disable 
verify change grep SELINUX= /etc/selin/config