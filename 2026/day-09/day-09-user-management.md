# Task 1: Create Users
* Command for create user: `Sudo useradd -m tokyo`
* Command for applying password : `sudo passwd tokyo`
* Command for create user: `sudo useradd -m berlin`
* Command for applying password : `sudo passwd berlin`
* Command for create user: `sudo useradd -m professor`
* Command for applying password : `sudo passwd professor`

# Task 2: Create Groups
* Command : `sudo groupadd developers`
* Command : `sudo groupadd admins`

# Task 3: Assign to Groups
* Command : `sudo usermod -aG tokyo developers`
* Command : ` sudo usermod -aG developers berlin && sudo usermod -aG admin berlin `
* Command : `sudo usermod -aG professor admin`

# Task 4: Shared Directory
* Command : `sudo mkdir -p /opt/dev-project`
* Command : `sudo chmod 775 dev-project`
* Command : `sudo chgrp developers dev-project `
* Command : ` sudo chmod 775 dev-project`
* Command : `su tokyo` and `password` , then cd /dev-project and create a file for tokyo user.
* Command : `su berlin` and `password` , then cd /dev-project and create a file for berlin user.

# Task 5: Team Workspace
* Command : `sudo useradd -m nairobi`
* Command : `sudo groupadd project-team`
* 
