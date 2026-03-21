# File Ownership Challenge (chown & chgrp)
## Users Created 
* tokyo
* berlin
* nairobi
* professor

## Grouop Created
* heist-team
* planners
* vault-team
* tech-team
  
## Files & Directories Created
 * devops-file.txt
* app-logs/
* bank-heist/access-codes.txt
* bank-heist/blueprints.pdf
* bank-heist/escape-plan.txt
* heist-project/plans/strategy.conf
* heist-project/vault/gold.txt
* project-config.yml
* team-notes.txt
  
## Understanding Ownership
* Run ls -l in your home directory
* Identify the owner and group columns
* Check who owns your files
* Command : `-rw-rw-r-- 1 ubuntu ubuntu  0 Mar 12 02:16 devops.txt`
* Owner : The owner is usually the user who created the file or directory. Owner can change permission of file.
* Group : The group is a collection of users who share access to the file.

## Basic chown Operations
* Create file devops-file.txt
* Check current owner: ls -l devops-file.txt
* Change owner to berlin
* Verify the changes
* Command : `sudo chown berlin devops-file.txt`
* Output : `-rw-rw-r-- 1 berlin ubuntu  0 Mar 12 02:16 devops.txt`

## Basic chgrp Operations
* Create file team-notes.txt
* Check current group: ls -l team-notes.txt
* Create group: sudo groupadd heist-team
* Change file group to heist-team
* Verify the change
* Command : `touch team-notes.txt`
* Command : `ls -l team-notes.txt`
* Output : `-rw-rw-r-- 1 ubuntu ubuntu  0 Mar 12 02:16 team-notes.txt`
* Command : `sudo groupadd heist-team`
* Command : `sudo chgrp heist-team team-notes.txt`
* Command : `ls -l team-notes.txt `
* Output : `-rw-rw-r-- 1 ubuntu heist-team  0 Mar 12 02:16 team-notes.txt`

## Combined Owner & Group Change
Using chown you can change both owner and group together:

* Create file project-config.yaml
* Change owner to professor AND group to heist-team (one command)
* Create directory app-logs/
* Change its owner to berlin and group to heist-team
* Command : `touch project-config.yaml`
* Command : `sudo chown professor:heist-team project-config.yaml`
* Command : `mkdir app-logs`
* Command : `sudo chown -R berlin:heist-team app-logs/`
* Output : `drwxrwxr-x 1 berlin heist-team  4096 Mar 12 02:16 app-logs`

## Recursive Ownership
* Create directory structure: <br>
`mkdir -p heist-project/vault`<br>
`mkdir -p heist-project/plans`<br>
`touch heist-project/vault/gold.txt`<br>
`touch heist-project/plans/strategy.conf`

* Create group `planners`: `sudo groupadd planners`
* Change ownership of entire `heist-project/` directory:

Owner: `professor`
Group: `planners`
Use recursive flag (`-R`)

* Verify all files and subdirectories changed: `ls -lR heist-project/`
* Command : `sudo groupadd planners`
* Command : `sudo chown -R professor:planner heist-project/`
* Command : `ls -lR heist-project/`
* Output : `drwxrwxr-x 2 professor planner  4096 Mar 12 02:16 plans`
* Output : `drwxrwxr-x 2 professor planner  4096 Mar 12 02:16 vault`
* Output : `-rw-rw-r-- 1 professor planner  0 Mar 12 02:16 gold.txt`
* Output : `-rw-rw-r-- 1 professor planner  0 Mar 12 02:16 strategy.conf`
  

