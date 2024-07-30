# What is Shell?
On linux system, shell is a program that takes input from the user and sends it to the os to perform the tasks.

|**Shell Type**|**Description**|
|---|---|
|`Reverse shell`|Initiates a connection back to a "listener" on our attack box.|
|`Bind shell`|"Binds" to a specific port on the target host and waits for a connection from our attack box.|
|`Web shell`|Runs operating system commands via the web browser, typically not interactive or semi-interactive. It can also be used to run single commands (i.e., leveraging a file upload vulnerability and uploading a `PHP` script to run a single command.|

# What is Port?
Ports are virtual points where network connections begin and end.
They are software-based and managed by the hosts os.
Ports are associated with a specific process or service and allow computers to differentiate between different traffic types (SSH traffic flows to a different port than web requests to access a website even though the access requests are sent over the same network connection).
There are two categories of ports, [Transmission Control Protocol (TCP)](https://en.wikipedia.org/wiki/Transmission_Control_Protocol), and [User Datagram Protocol (UDP)](https://en.wikipedia.org/wiki/User_Datagram_Protocol).
TCP is a connections-oriented, meaning a connection between a client and a server must be established before data can be sent.
UDP utilizes a connection-less model. There is no "handshake" and therefore introduce certain amount of unreliability since there is no guarantee of data transfer.

|Port(s)|Protocol|
|---|---|
|`20`/`21` (TCP)|`FTP`|
|`22` (TCP)|`SSH`|
|`23` (TCP)|`Telnet`|
|`25` (TCP)|`SMTP`|
|`80` (TCP)|`HTTP`|
|`161` (TCP/UDP)|`SNMP`|
|`389` (TCP/UDP)|`LDAP`|
|`443` (TCP)|`SSL`/`TLS` (`HTTPS`)|
|`445` (TCP)|`SMB`|
|`3389` (TCP)|`RDP`|

# What is a Web Server
A web-server is a back-end application that handles all the HTTP traffic from the client-side browser, route it to the request destination page, finally responds to the client-side browser.\

Web servers usually run on TCP ports `80` or `443`, and are responsible for connecting end-users to various parts of the web application.
Ports are numbered from 0 to 65,535.
The first 1024 ports (0-1023) are considered "well-known" ports and are reserved for common protocols and applications.
A network protocol is a set of rules and standards that define how data is transmitted between devices on a computer network. The protocol specifies the format, timing, sequencing, and error checking methods used for the exchange of data.

network protocols define the rules and formats for network communication, while ports act as the logical endpoints or interfaces where this communication occurs.

# Using Netcat
[Netcat](https://linux.die.net/man/1/nc), `ncat`, or `nc`, is an excellent network utility for interacting with TCP/UDP ports. It can be used for many things during a pentest. Its primary usage is for connecting to shells.
In addition to that, `netcat` can be used to connect to any listening port and interact with the service running on that port. For example, `SSH` is programmed to handle connections over port 22 to send all data and keys.
