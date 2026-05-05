sudo chmod a+x xfusioncorp.sh
a+x means all users (owner, group, others) get execute permission.

This ensures anyone can run the script.
Why 755?
Owner (u): read, write, execute → rwx

Group (g): read, execute → rx

Others (o): read, execute → rx