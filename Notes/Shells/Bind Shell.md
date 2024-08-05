Unlike a `Reverse Shell` that connects to us, we will have to connect to it on the `targets'` listening port.

it means we connect to the target

Once we execute a `Bind Shell Command`, it will start listening on a port on the remote host and bind that host's shell, i.e., `Bash` or `PowerShell`, to that port. We have to connect to that port with `netcat`, and we will get control through a shell on that system.

