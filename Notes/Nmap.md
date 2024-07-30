Suppose that we want to perform a basic scan against a target residing at 10.129.42.253. To do this we should type `nmap 10.129.42.253` and hit return. We see that the `Nmap` scan was completed very quickly. This is because if we don't specify any additional options, Nmap will only scan the 1,000 most common ports by default. The scan output reveals that ports 21, 22, 80, 139, and 445 are available.
By default, `Nmap` will conduct a TCP scan unless specifically requested to perform a UDP scan.

We can use the -sC parameter to specify that Nmap scripts should be used to obtain more detailed information.
The -sV parameter instructs Nmap to perform a version scan.
`-p-` tells Nmap that we want to scan all 65,535 TCP ports.

#  Attacking Network Services
## FTP
FTP(File transfer Protocol) is a standard protocol, and this service can often contain interesting data.
## SMB
SMB(Server Message Block) is a prevalent protocol on Windows machines that provides many vectors  for vertical and lateral movements.
Sensitive data, including credentials(is the information required to authenticate and authorize a user, device, or application to access a specific resource or service.), can be in network file shares, and some SMB versions may be vulnerable to RCE exploits such as [EternalBlue](https://www.avast.com/c-eternalblue). 
It is crucial to enumerate this sizeable potential attack surface carefully. `Nmap` has many scripts for enumerating(is the process of gathering information about a target system or network) SMB, such as [smb-os-discovery.nse](https://nmap.org/nsedoc/scripts/smb-os-discovery.html), which will interact with the SMB service to extract the reported operating system version.
## Shares
SMB allows users and administrators to share folders and make them accessible remotely by others users.