👤 Linux User & Group Management Script
📌 Overview

This is an interactive Bash script that helps system administrators manage users and groups on Linux.
It provides a simple menu-driven interface to add/delete users, manage groups, check password expiry, and monitor failed login attempts.

🛠 Features

➕ Add User → Create a new user with a default shell and password.

❌ Delete User → Remove a user account (and home directory).

👥 Add Group → Create a new group.

🗑 Delete Group → Remove an existing group.

🔑 Password Expiry Check → View password expiration details of a user.

🔎 Login Attempts Monitoring → Display the last 10 failed login attempts from /var/log/auth.log.

🚪 Exit Option → Quit the script safely.

⚙️ Requirements

Must be run as root (or with sudo).

Linux system with useradd, userdel, groupadd, groupdel, chage, and tail utilities.

▶️ Usage

Make script executable

chmod +x user_group_management.sh


Run as root

sudo ./user_group_management.sh


Menu Options

=======================================
   Linux User & Group Management Tool
=======================================
1. Add User
2. Delete User
3. Add Group
4. Delete Group
5. Password Expiry Check
6. Login Attempts Monitoring
7. Exit
=======================================
Choose an option [1-7]:

🧪 Example Run
Add a User
Enter username to add: devuser
Enter default shell (/bin/bash):
Changing password for user devuser.
✅ User 'devuser' added successfully.

Check Password Expiry
Enter username to check password expiry: devuser
Last password change                                    : Sep 17, 2025
Password expires                                        : never
Password inactive                                       : never
Account expires                                         : never
Minimum number of days between password change          : 0
Maximum number of days between password change          : 99999

Failed Login Attempts
🔎 Failed login attempts (last 10):
Sep 17 10:22:33 server sshd[1234]: Failed password for root from 192.168.1.50 port 45678 ssh2
Sep 17 10:22:36 server sshd[1234]: Failed password for root from 192.168.1.50 port 45678 ssh2

🚀 Future Improvements

Add functionality to lock/unlock user accounts.

Add group membership management (assign users to groups).

Support logging actions (audit trail).

Add export/import feature for user details.

👨‍💻 Author

Tushar Srivastava
Project: System Administration & User Management
