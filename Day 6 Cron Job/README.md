Question:  
The Nautilus system admins team has prepared scripts to automate several day‑to‑day tasks. They want them deployed on all app servers in Stratos DC on a set schedule. Before rollout, they need to test similar functionality with a sample cron job.

Tasks:  
a. Install the cronie package on all Nautilus app servers and start the crond service.
b. Add a cron job for the root user:

Code
*/5 * * * * echo hello > /tmp/cron_text
Solution:

Installed cronie with dnf install cronie -y and enabled the service using systemctl start crond && systemctl enable crond.

Edited the root crontab (crontab -e) to add the */5 * * * * echo hello > /tmp/cron_text entry.

Verified with systemctl status crond and checked /tmp/cron_text after 5 minutes to confirm execution.