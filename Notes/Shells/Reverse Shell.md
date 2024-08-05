A reverse shell is the most common type of shell and is the quickest and easiest method to obtain over a compromised host.

once we find a vulnerability on the remote host we can start a netcat listener on our machine that listens to a specific port.

With this listener in place, we can execute a `reverse shell command` that connects the remote systems shell, i.e., `Bash` or `PowerShell` to our `netcat` listener, which gives us a reverse connection over the remote system.

| Flag      | Description                                                                         |     |     |
| --------- | ----------------------------------------------------------------------------------- | --- | --- |
| `-l`      | Listen mode, to wait for a connection to connect to us.                             |     |     |
| `-v`      | Verbose mode, so that we know when we receive a connection.                         |     |     |
| `-n`      | Disable DNS resolution and only connect from/to IPs, to speed up the connection.    |     |     |
| `-p 1234` | Port number `netcat` is listening on, and the reverse connection should be sent to. |     |     |

