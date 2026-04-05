# Revision (Days 01–11)
* I am focused on transitioning from IT Support to a DevOps Engineer role in 2026. By consistently investing time in learning, gaining hands-on experience, and strengthening my expertise in Linux, automation, and cloud technologies, I am making steady progress toward this goal.

## Basics
* Firstly learned how the linux architechture works.
* Playing with basic commands like `cd, ls, mkdir, cat, vim, touch, man, whoami, etc`

## Processes & services
* Whenever my system slows down, I use the following commands to troubleshoot and check service health:
* `ps -aux` - Lists all running processes on the system.
* `top` - Display sorted information about processes.
* `systemctl status <service>` - Displays the status of a specific service (whether it’s active, failed, or inactive).
* `journalctl -u <service>` - Displays logs for a specific service, useful for debugging issues.
* `grep` - find the statement or words in the file

## File skills
I practiced creating/modifying/permission of Linux file/folder. Here is how to safely change ownership and permissions:
* Check current ownership and permissions
* `ls -l /path/to/file`
* Change ownership (user and group)
* `sudo chown user:group /path/to/file`
* Change permissions (least privilege principle)
* `chmod 751 /path/to/file`

## Cheat Sheet
Top commands I'd use in an incident :
* `ps aux` - Lists all running processes with CPU/memory usage
* `mpstat` - Monitors CPU utilization across cores, highlighting bottlenecks or unusual load.
* `systemctl status service` - Verifies if a critical service is active, failed, or restarting.
* `cat /var/log/nginx/error.log` - Reads raw logs for web server errors (replace with relevant service log path).
* `journalctl -u service` - Retrieves detailed logs for a given service, useful for debugging failures.
* `free -m` - Displays memory usage in MB to check for exhaustion or leaks.

## What will I focus on improving in the next 3 days?
* I want to focus the partition and complete Linux Volume Management.
* Also I will practice all the commands repeat again.
* And if time allows I will also watch AWS videos and other tools.
* After all the parts are being completed. Building projects.
