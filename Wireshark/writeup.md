# @1 A second listener (50)

tcp.stream eq 0

follow > Listening on [0.0.0.0] (family 0, port 9999)

flag<9999>

# @2 I am groot (50)

tcp.stream eq 5

packet 133 > smb2 > tree connect request > tree

flag<\\192.168.2.10\public>

# @3 I will assit (50)

Sender MAC address: VMware_89:f4:58 (00:0c:29:89:f4:58)
Target IP address: 192.168.2.244

flag<192.168.2.244>

# @4 Listening (50)

tcp.stream eq 0

TCP > src port

flag<4444>

# @5 Please give (50)

dhcp

dhcp > Requested IP Address

flag<192.168.20.11>

# @6 Shark01 (50)

Transaction ID: 0x9f8fa557

flag<0x9f8fa557>

# @7 Some good ol fashion txt (50)

TXT: ACOOLDNSFLAG

flag<ACOOLDNSFLAG>

# @8 Tick Tock (50)

Internet Protocol Version 6, Src: 2003:51:6012:110::dcf7:123, Dst: 2003:51:6012:121::10

flag<2003:51:6012:110::dcf7:123>

# @9 Who speaks (50)

tcp.stream eq 0

Ethernet II > Source > Address

flag<00:0c:29:82:f5:94>

# @10 Yellow Brick Road (50)

GUID handle File: HelloWorld\TradeSecrets.txt

flag<HelloWorld\TradeSecrets.txt>

# @11 Exif (75)

tcp.stream eq 0

follow stream > jtomato@ns01:~$ echo "\*umR@Q%4V&RC" | sudo -S nc -nvlp 9999 < **/etc/passwd**

flag</etc/passwd>

# @12 How recent (75)

0 upgraded, 1 newly installed, 0 to remove and 18 not upgraded.
Need to get 3,436 B of archives.
After this operation, 13.3 kB of additional disk space will be used.
Get:1 http://us.archive.ubuntu.com/ubuntu bionic/universe amd64 netcat all 1.10-41.1 [3,436 B]

Request URI: /ubuntu/pool/universe/n/netcat/netcat_1.10-41.1_all.deb

flag<1.10-41.1>

# @13 I have the answers (75)

udp.stream eq 1

flag<e.root-servers.net>

# @14 Uh uh uh (75)

NT Status: STATUS_LOGON_FAILURE (0xc000006d)

flag<0xc000006d>

# @15 A very secure authication method (100)

echo "\*umR@Q%4V&RC" | sudo -S apt install netcat

flag<*umR@Q%4V&RC>

# @16 According to all known laws of aviation (100)

smb2.sesid eq 0x0000000063e5fab2

e lived in the topsy-turvy world Mr [....] doesn't someone just step on this creep, and we can all go home?! - Order in this court! flag<OneSuperDuperSecret> - You're all thinking it! [...]

flag<OneSuperDuperSecret>

# @17 What version pt. 2 (100)

tcp.stream eq 0

follow stream > Hit:1 http://us.archive.ubuntu.com/ubuntu bionic InRelease

flag<bionic>

# @18 Who has authority (100)

dns

dns > Authoritative nameservers > Name Server

flag<ns2.hans.hosteurope.de>

# @19 How am I talking? (150)

cdp

cdp.deviceid eq CCNP-LAB-S2.webernetz.net

check the Port ID

flag<GigabitEthernet0/2>

# @20 Who changed (150)

stp.flags.tc == 1

STP > Originating VLAN (PVID)

flag<20>

# @21 Who is using me (150)

tcp.stream == 6

flag<31>

# @22 How cool are you (200)

cdp.deviceid eq CCNP-LAB-S2.webernetz.net

Software version: IOS (tm) C2950 Software (C2950-I6K2L2Q4-M), Version 12.1(22)EA14, RELEASE SOFTWARE (fc1)

flag<12.1(22)EA14>

# @23 Please talk (200)

icmpv6

3 Router Solicitations

flag<3>

# @24 Some secret sauce (200)

tcp.stream eq 27

follow stream

```
flag: y2*Lg4cHe@Ps
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Content-Type: text/html; charset=UTF-8

<h1> Fruit Inc </h1>
<h2> Authorized Personal Only </h2>

Hi Mum
```

flag<y2*Lg4cHe@Ps>

# @25 Virtual Sharing (200)

hsrp

2nd packet (source == 192.168.121.254)

CHSRP > Group State TLV > Virtual IP Address

flag<192.168.121.1>

# @26 Who is root (200)

vlan.id == 60

STP > Bridge Identifier > Bridge System ID

flag<00:21:1b:ae:31:80>

# @27 Who is sharing (200)

rip and (ip.addr eq 192.168.10.1 or ip.addr eq 192.168.20.1)

from both ip addr. > rip

```
IP Address: 0.0.0.0, Metric: 2
    Address Family: IP (2)
    Route Tag: 0
    IP Address: 0.0.0.0 (0.0.0.0)
    Netmask: 0.0.0.0
    Next Hop: 0.0.0.0 (0.0.0.0)
    Metric: 2
IP Address: 192.168.10.0, Metric: 1
    Address Family: IP (2)
    Route Tag: 0
    IP Address: 192.168.10.0 (192.168.10.0)
    Netmask: 255.255.255.0
    Next Hop: 0.0.0.0 (0.0.0.0)
    Metric: 1
IP Address: 192.168.20.0, Metric: 1
    Address Family: IP (2)
    Route Tag: 0
    IP Address: 192.168.20.0 (192.168.20.0)
    Netmask: 255.255.255.0
    Next Hop: 0.0.0.0 (0.0.0.0)
    Metric: 1
IP Address: 192.168.30.0, Metric: 1
    Address Family: IP (2)
    Route Tag: 0
    IP Address: 192.168.30.0 (192.168.30.0)
    Netmask: 255.255.255.0
    Next Hop: 0.0.0.0 (0.0.0.0)
    Metric: 1
IP Address: 192.168.121.0, Metric: 1
    Address Family: IP (2)
    Route Tag: 0
    IP Address: 192.168.121.0 (192.168.121.0)
    Netmask: 255.255.255.0
    Next Hop: 0.0.0.0 (0.0.0.0)
    Metric: 1
```

IP address are:

```
0.0.0.0
192.168.10.0
192.168.20.0
192.168.30.0
192.168.121.0
```

without itself:

```
0.0.0.0
192.168.30.0
192.168.121.0
```

adding the network reserved bits,

flag<0.0.0.0/0;192.168.30.0/24;192.168.121.0/24>

[ref](https://www.cloudaccess.net/cloud-control-panel-ccp/157-dns-management/322-subnet-masks-reference-table.html)

# @28 Working together (200)

lacp

lacp > actor state

flag<0x3d>

# @29 How are you controlled (250)

cdp.deviceid eq CCNP-LAB-S2.webernetz.net

cdp > management addresses > ip address

flag<192.168.121.20>

# @30 Sharing is caring (250)

snmp > 1st response > snmp > data > get-response > variable-bindings > value

flag<Fa0/1>

# @31 A sneak peak (300)

add [ssl keys](secret_sauce.txt) to wireshark

export objects > http > save

![image](assets/get_a_new_phone_today__720.jpg)

flag<get_a_new_phone_today\_\_720.jpg>

# @32 Someone needs a change (400)

http2

tcp.stream eq 39 and http2.streamid eq 21

http2 > HTML Form URL Encoded: application/x-www-form-urlencoded

Form item: "email" = "Jim.Tomato@fruitinc.xyz"

flag<Jim.Tomato@fruitinc.xyz>

# @33 That's not good (400)

dns.qry.name eq fw01.fruitinc.xyz

tcp.stream eq 34

tcp.stream eq 34 and http2.streamid eq 15

[...]...MH.@......X. ....a{ZT%...@.I..M.5.........................__csrf_magic=sid%3Aa68a97d4f80a4ff8f25235ed57574d2979224f5a%2C1587148353%3Bip%3A0f813abe32d96228b630d34339938d54ca4d8077%2C1587148353&usernamefld=admin&passwordfld=Ac5R4D9iyqD5bSh&login=Sign+In........................A...... H.302v..cU.a..a....C].....z."......\_.I|...M.j.q..[...]

usernamefld=admin&passwordfld=Ac5R4D9iyqD5bSh

**OR**

tcp.stream eq 34

tcp.stream eq 34 and http2.streamid eq 15

got through the packets for a x-www-form-urlencoded packet.

HTTP2 > HTML Form URL Encoded: application/x-www-form-urlencoded > Form item: "usernamefld" = "admin"
HTTP2 > HTML Form URL Encoded: application/x-www-form-urlencoded > Form item: "passwordfld" = "Ac5R4D9iyqD5bSh"

flag<admin:Ac5R4D9iyqD5bSh>

# @34 Last update (500)

tftp / udp.stream eq 55

follow stream

```
! Last configuration change at 20:55:45 UTC Fri Mar 3 2017 by weberjoh
! NVRAM config last updated at 21:02:36 UTC Fri Mar 3 2017 by weberjoh
! NVRAM config last updated at 21:02:36 UTC Fri Mar 3 2017 by weberjoh
```

flag<21:02:36 03/03/2017>

# @35 Some Authentication (500)

tftp / udp.stream eq 55

follow stream

```
radius server blubb
 address ipv6 2001:DB8::1812 auth-port 1812 acct-port 1813
```

flag<2001:DB8::1812>

# @36 Some more sharing (500)

tftp / udp.stream eq 55

follow stream

```
interface FastEther........net0/1.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
 ip verify unicast source reachable-via rx
 ipv6 address 2003:51:6012:122::1/64
 ipv6 rip CCNPv6 enable
!
interface FastEthernet0/1.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0
 ip verify unicast source reachable-via rx
!
interface FastEthernet0/1.30
 encapsulation dot1Q 30
 ip address 192.168.30.1 255.255.255.0
 ip verify unicast source reachable-via rx
!
interface FastEthernet0/1.121
 encapsulation dot1Q 121
 ip ........address 192.168.121.2 255.255.255.0
 ip verify unicast source reachable-via rx allow-default
 ipv6 address 2003:51:6012:121::2/64
 ipv6 rip CCNPv6 enable
```

2003:51:6012:122::1/64
2003:51:6012:121::2/64

flag<2003:51:6012:121::/64;2003:51:6012:122::/64>

## @37 What changed? (600)
