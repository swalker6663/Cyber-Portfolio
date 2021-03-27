## Ensure/Double Check Permissions on Sensitive Files


Permissions on /etc/shadow should allow only root read and write access.


Command to inspect permissions: ls -l /etc/shadow


Command to set permissions (if needed): sudo chmod 755 /etc/





Permissions on /etc/gshadow should allow only root read and write access.


Command to inspect permissions: ls -l /etc/gshadow



Command to set permissions (if needed): sudo chmod <octal>/etc/gshadow





Permissions on /etc/group should allow root read and write access, and allow everyone else read access only.


Command to inspect permissions: ls -l /etc/group


Command to set permissions (if needed): sudo chmod <octal>/etc/group




Permissions on /etc/passwd should allow root read and write access, and allow everyone else read access only.


Command to inspect permissions: ls -l /etc/passwd

Command to set permissions (if needed): sudo chmod <octal>/etc/passwd





## Create User Accounts


Add user accounts for sam, joe, amy, sara, and admin.

Command to add each user account (include all five users): sudo useradd -d <name>



Ensure that only the admin has general sudo access.

Command to add admin to the sudo group: sudo usermod aG sudo admin




## Create User Group and Collaborative Folder


Add an engineers group to the system.

Command to add group: sudo addgroup engineers 



Add users sam, joe, amy, and sara to the managed group.

Command to add users to engineers group (include all four users): sudo usermod aG engineers <user name>



Create a shared folder for this group at /home/engineers.

Command to create the shared folder: sudo mkdir /home/engineers




Change ownership on the new engineers' shared folder to the engineers group.

Command to change ownership of engineer's shared folder to engineer group: sudo chown :engineers /home/engineers




## Lynis Auditing


Command to install Lynis: sudo apt install lynis


Command to see documentation and instructions: man lynis


Command to run an audit: sudo lynis audit system


Provide a report from the Lynis output on what can be done to harden the system.

Screenshot of report output:




