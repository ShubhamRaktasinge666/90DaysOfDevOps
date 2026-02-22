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
<p><b>Observation</b> : Copy files from /etc/hosts. Filesystem is writeable.</p>






