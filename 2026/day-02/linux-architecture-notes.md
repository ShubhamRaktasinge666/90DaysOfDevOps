<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <h1>Core Linux Components</h1>
</head>
<body>
  <img src="linux.jpg" width="200" height="300">
  <p><b>Hardware:</b> It is a physical component which relies on binary language for doing operation like data storage , processing.</p>

  <p><b>Kernel:</b> It is a very important part of linux system , because the all request which are coming from shell the kernel will process and convert into binary ( low level language ) and send to hardware . so, it can perform the operation which are given from user. After that the hardware will process that and gave kernel and it will convert in human readable language and forward the output on terminal</p>

  <p><b>Shell:</b> It is a command-line interpreter that translates user commands into instructions .</p>

  <p><b>Application:</b> It is the applications are software programs that run on top of the operating system and interact with system resources through a structured hierarchy involving system libraries, the shell, and the kernel.</p>

  <h1>Processes in Linux</h1>
  <p>Process are running instance of a program. which generally show in top command . ex: If i am running some process in background , it will show in top . Also we can list process using ps ( ps au , ps ef ) / or top commands</p>

  <h2>Process State</h2>
  <p><b>Running</b> : Activate Process.</p>
  <p><b>Sleeping</b> : Idle Process.</p>
  <p><b>Stopped</b>: Process suspended by single SIGSTOP. It can be resumed by a SIGCONT signal.</p> 
  <p><b>Zombie</b> : The process has termininated, but it's entry in the process table still exist. Becasuse, it's parent process has not yet read it's exit status.</p>

  <h1>5 Command used daily</h1>
  <p><b>systemctl</b> : It is a command used to manage the service. examle i have to start / enbale the nginx service then using systemctl start nginx / systemctl enable nginx. That's how we can use systemctl command</p>

  <p><b>help</b> : It is a command used to open options which we are don't know . example ls we want to see, how we can use ls and it's option. Using the ls --help</p>

  <p><b>ssh</b> : It is a command used to access the server or machine . from the remote location , it just need only .pem file to access the machine.</p>

  <p><b>chmod</b> : It is a command used to manage the permission which we are apply on files folders</p>

  <p><b>chown</b> : It is a command used to manage the ownership of a file or a folder</p>





</body>
</html>


