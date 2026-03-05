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
