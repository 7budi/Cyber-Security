Once we compromise a system and exploit a vulnerability to execute commands on the compromised hosts remotely, we usually need a method of communicating with the system not to have to keep exploiting the same vulnerability to execute each command. To enumerate the system or take further control over it or within its network, we need a reliable connection that gives us direct access to the system's shell, i.e., `Bash` or `PowerShell`, so we can thoroughly investigate the remote system for our next move.

The other method of accessing a compromised host for control and remote code execution is through shells.  

There are three main types of shells: Reverse Shell, Bind Shell, and Web Shell. Each of these shells has a different method of communication with us for accepting and executing our commands.

| Type of Shell     | Method of Communication                                                                                                     |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------- |
| [[Reverse Shell]] | Connects back to our system and gives us control through a reverse connection.                                              |
| [[Bind Shell]]    | Waits for us to connect to it and gives us control once we do.                                                              |
| [[Web Shell]]     | Communicates through a web server, accepts our commands through HTTP parameters, executes them, and prints back the output. |