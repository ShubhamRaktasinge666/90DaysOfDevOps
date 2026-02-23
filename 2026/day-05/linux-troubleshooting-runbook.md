<h1>RUNBOOK for ssh service</h1>
<h3>This runbook provides quick troubleshooting steps if the SSH service goes down.</h3><br>

<h2>Enviroment Basics</h2>
<p><b>uname -a</b> : Linux ip-172-31-21-251 6.14.0-1018-aws #18~24.04.1-Ubuntu SMP Mon Nov 24 19:46:27 UTC 2025 x86_64 x86_64 x86_64 GNU/Linux</p>
<p><b>Observation</b> : Kernel version and architechture confirmed.</p><br>

<p><b>cat /etc/os-release</b> : PRETTY_NAME="Ubuntu 24.04.3 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.3 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian</p>
<p><b>Observation</b> : Confirms distribution and release version</p><br>

<h2>Filesystem sanity</h2>
<p><b>mkdir /tmp/runbook-demo</b> : mkdir: created directory '/tmp/runbook-demo'</p>
<p><b>Observation</b> : Directory created successfully</p><br>
<p><b>cp /etc/hosts /tmp/runbook-demo/hosts-copy && ls -l /tmp/runbook-demo</b></p>
<p><b>Observation</b> : Copy files from /etc/hosts. Filesystem is writeable.</p><br>

<h2>CPU / Memory</h2>
<p><b>Command : ps -aux | grep $USER</b></p>
<p> PID - 1352 <br> %CPU - 0.0 <br> %MEM - 0.7 <br>   COMMAND - sshd: ubuntu@pts/1</p>
<p><b>Observation</b> : Process running and CPU & memory usage is negligible.</p><br>

<p><b>Command : free -h</b></p>
<p> Total: 914Mi <br> Used: 360Mi <br> Available: 553Mi </p>
<p><b>Observation</b> : Sufficient memory available.</p><br>

<h2>Disk / IO</h2>
<p><b>Command : df -h</b></p>
<p><b>Output : /dev/root  &nbsp;      6.8G &nbsp; 1.8G &nbsp;  5.0G  &nbsp; 27% &nbsp; /</b></p>
<p><b>Observation</b> : 90% root partition available.</p><br>

<p><b>Command : iostat -h</b></p>
<p><b>Observation</b> : CPU idle= 97.08% -> which is healthy. iowait= 0.55% -> small percentage of CPU time waiting for I/O. system= 0.61% -> low. user= 1.75% .</p><br>

<h2>Network</h2>
<p><b>Command : sudo ss -tulpn | grep  sshd</b></p>
<p><b>Output : tcp  &nbsp;  LISTEN 0   &nbsp;    4096      &nbsp;             0.0.0.0:22      &nbsp;       0.0.0.0:*    &nbsp; users:(("sshd",pid=1029,fd=4),("systemd",pid=1,fd=176))</b></p>
<p><b>Observation</b> : ssh is listening on port 22.</p><br>

<p><b>Command : nc -zv localhost 22</b></p>
<p><b>Output : Connection to localhost (127.0.0.1) 22 port [tcp/ssh] succeeded!</b></p>
<p><b>Observation</b> : ssh connection confirmed.</p><br>















