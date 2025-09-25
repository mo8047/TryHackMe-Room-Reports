# Section 1 

Nmap uses multiple ways to specify the scope of it's targets.
It uses '-' to find the IP range e.g. 192.168.0.1-10, and '/' to find the subnet range e.g. 192.168.0.1/24 and you can also specify the target by it's hostname.

Nmap has the '-sn' option which stands for ping scan but this isn't limited as the conventional ping command.

# To scan a local network using Nmap

Usually to scan a local network we use the arp-scan because it only works on local networks but nmap isn't limited to.
To scan a local network we use the following command 'nmap -sn ip address' using this command it will also shoe us the MAC address of the device because it's a local device (Connected through ethernet or wifi). 

# To scan a remote network

To scan a remote network we use the same command for the Local network scan and this is also what makes using Nmap unique it's versatility and convenience.
To run a Remote scan we'd usually use the ping command but the ping command won't give information if the target's system has a firewall setup.

Nmap also offers a List scan option '-sL'. This scan only lists the targets to scan without scanning them.
For example 'nmap -sL 192.168.0.1/24' will list the 256 targets that will be scanned. This option helps confirm the targets before running the actual scan.


Task:What is the last IP address that will be scanned when your scan target is 192.168.0.1/27?

To find this command I used the -sL to list the IP addresses and took out the last IP address as the answer.

![](Picture1.png) Command 
![](Picture2.png) Answer

**What I Learned**

1. -sn is more flexible than normal ping.
2. /27 subnet = 32 addresses (192.168.0.1 → 192.168.0.31).
3. -sL lets me preview targets before launching scans.
4. Local scans reveal MAC addresses, remote scans don’t.

# Section 2

