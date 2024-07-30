Suppose that we want to perform a basic scan against a target residing at 10.129.42.253. To do this we should type `nmap 10.129.42.253` and hit return. We see that the `Nmap` scan was completed very quickly. This is because if we don't specify any additional options, Nmap will only scan the 1,000 most common ports by default. The scan output reveals that ports 21, 22, 80, 139, and 445 are available.
By default, `Nmap` will conduct a TCP scan unless specifically requested to perform a UDP scan.

We can use the -sC parameter to specify that Nmap scripts should be used to obtain more detailed information.
The -sV parameter instructs Nmap to perform a version scan.
`-p-` tells Nmap that we want to scan all 65,535 TCP ports.

#  Attacking Network Services
## FTP
FTP(File transfer Protocol) is a standard protocol, and this ser