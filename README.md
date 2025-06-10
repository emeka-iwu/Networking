# Networking
Networking Fundamentals

## IP Addresses

ip addresses are unique identifiers for computers connected to a local network. two types of ipaddresses
- Public IP - used for connection over the internet
- Private IP - used for connection within a local area network (LAN)
The 2 standard ip addresses are. ipv4 and ipv6. ipv4 are the standard.

ipv4 ip addresses have 4 bytes and each byte known as octet has 8 bits, totalling 32 bits. as shown below
--------|--------|--------|--------
take one octet which has 8 bits (all 1's), 76543210 = 2^0 + 2^1 + 2^2 + 2^3 + 2^4 + 2^5 + 2^6 +2^7 = 255

maximum number on each byte is 255 ie 255.255.255.255.

so an ip address of 192.168.12.4 in binary is same; 11000000 | 10000000 | 00001100 | 00000100

## Subnets/CIDR

subnets means sub netwrok, it involves creating a network within a network or vitualprivate cloud (VPC). Subnets are use to create;
- security
- privacy
- isolation

A subnect can either be private (internal network identification) or public (access to internet)

CIDR rae used to manage the number of ip addresses/networks in a subnet. 
For example, an ip address of 172.16.3.0/24, 24 stands for the bits taken by the network, and the last 8 bits remaining are available for host devices (24 falls in the first 3 octets and the last remainng 8 are in the 4th octet). so the ip address of 172.16.3.0/24 has a mask of 255.255.255.0, as all first 24 bits have been taken. Also the subnet of /24 means 2^32-24, = 2^8, = 256 ip addresses, with only 254 usable addresess.
- 172.16.3.0 = Network address
- 172.16.3.1 = first usable address
- 172.16.3.254 = last usable address
- 172.16.3.255 = broadcast address 
Hence the ip address range for 172.16.3.0/24 is 172.16.3.0 - 172.16.3.255. if more addresses are needed, the next ip address subnet is 172.16.4.0/24.or the inital ip address should be adjuested to 172.16.3.0/23 (incorrect), 172.16.2.0/23(correct).

## Ports

Ports are unique number used to access an applicaion in a network.

## OSI Models

OSI models are used to unerstand the journey of a data.   

There are 7 OSI model layers;
- layer 7: Application layer (HTTP, HTTPS, FTP)
- layer 6: Presentation Layer (responsible for formatting and encryotion in human readable format eg webpage, jpg)
- layer 5: Session Layer (responsible for user session management. stored in cookies and cache)
- layer 4: Transport layer (TCP/UDP, responsible for segementing data being transmitted )
- layer 3: Network Layer (This handles the packet transmision of the data from destination ip to source ip in the router). 
- layer 2: Data link layer (this is handled in the switches. ei mac address)
- layer 1: Physical layer (where data is converted to electric signals)

level 5,6, and 7 are handled in the browser.

