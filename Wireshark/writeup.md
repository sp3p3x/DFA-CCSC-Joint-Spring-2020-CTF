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

http2 and ip.addr == 192.168.2.1

go through header packets

```
Line-based text data: text/html (517 lines)
    <!DOCTYPE html>\n
    <html lang="en">\n
    <head>\n
    \t<meta name="viewport" content="width=device-width, initial-scale=1">\n
    \n
    \t<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">\n
    \t<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">\n
    \t<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">\n
    \t<link rel="manifest" href="/manifest.json">\n
    \t<link rel="mask-icon" href="/safari-pinned-tab.svg" color="#5bbad5">\n
    \t<meta name="theme-color" content="#ffffff">\n
    \n
    \t<link rel="stylesheet" href="/vendor/font-awesome/css/font-awesome.min.css?v=1580510450">\n
    \t<link rel="stylesheet" href="/vendor/sortable/sortable-theme-bootstrap.css?v=1580510450">\n
    \t<link rel="stylesheet" href="/css/pfSense.css?v=1580510450" />\n
    \n
    \t<title>fw01.fruitinc.xyz - Services: NTP: Settings</title>\n
    \t<script type="text/javascript">\n
    \t//<![CDATA[\n
    \tvar events = events || [];\n
    \tvar newSeperator = false;\n
    \t//]]>\n
    \t</script>\n
     [truncated]<script type="text/javascript">if (top != self) {top.location.href = self.location.href;}</script><script type="text/javascript">var csrfMagicToken = "sid:6f0e49c0ccb23e96909bb7aaa117103b44140ea6,1587148398";var csrfMagicName
    \n
    <body id="2">\n
    <nav id="topmenu" class="navbar navbar-static-top navbar-inverse">\n
    \t<div class="container">\n
    \t\t<div class="navbar-header">\n
    \t\t\t<button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#pf-navbar">\n
    \t\t\t\t<span class="sr-only">Toggle navigation</span>\n
    \t\t\t\t<span class="icon-bar"></span>\n
    \t\t\t\t<span class="icon-bar"></span>\n
    \t\t\t\t<span class="icon-bar"></span>\n
    \t\t\t</button>\n
    \t\t\t<a class="navbar-brand" href="/">\n
    \t\t\t\t<svg id="logo" role="img" aria-labelledby="pfsense-logo" x="0px" y="0px" viewBox="0 0 282.8 84.2">\n
    \t<title id="pfsense-logo-svg">pfSense Logo</title>\n
    \t<path class="logo-st0" d="M27.8,57.7c2.9,0,5.4-0.9,7.5-2.6c2.1-1.7,3.6-4,4.4-6.8c0.8-2.8,0.6-5.1-0.5-6.8c-1.1-1.7-3.2-2.6-6.1-2.6 c-2.9,0-5.4,0.9-7.5,2.6c-2.1,1.7-3.5,4-4.3,6.8c-0.8,2.8-0.7,5.1,0.5,6.8C22.8,56.9,24.8,57.7,27.8,57.7"/>\n
     [truncated]\t<path class="logo-st0" d="M115.1,46.6c-1.5-0.8-3-1.4-4.7-1.8c-1.7-0.4-3.2-0.7-4.7-1.1c-1.5-0.3-2.7-0.7-3.6-1.1c-0.9-0.4-1.4-1.1-1.4-2 c0-1.1,0.5-1.9,1.4-2.4c0.9-0.5,1.9-0.7,2.8-0.7c2.8,0,5,1,6.7,3.1l7-7c-1.7-1.8-3.9-3.1-6.4-
     [truncated]\t<path class="logo-st0" d="M156.3,34.1c-1.5-1.7-3.3-3-5.5-3.9c-2.2-0.9-4.6-1.4-7.2-1.4c-2.9,0-5.6,0.5-8.1,1.4c-2.5,0.9-4.7,2.2-6.6,3.9 c-1.9,1.7-3.3,3.8-4.4,6.2c-1.1,2.4-1.6,5.1-1.6,8c0,3,0.5,5.6,1.6,8c1.1,2.4,2.5,4.5,4.4,6.2
     [truncated]\t<path class="logo-st0" d="M198.3,33.8c-1-1.6-2.4-2.8-4.2-3.7c-1.8-0.9-4.1-1.3-7-1.3c-1.4,0-2.7,0.2-3.8,0.5c-1.2,0.4-2.2,0.8-3.1,1.4 c-0.9,0.6-1.7,1.2-2.4,1.9c-0.7,0.7-1.2,1.4-1.5,2.1H176v-5.1h-11v37.2h11.5V48.4c0-1.2,0.1-2.4
     [truncated]\t<path class="logo-st0" d="M231.5,46.6c-1.5-0.8-3-1.4-4.7-1.8c-1.7-0.4-3.2-0.7-4.7-1.1c-1.5-0.3-2.7-0.7-3.6-1.1c-0.9-0.4-1.4-1.1-1.4-2 c0-1.1,0.5-1.9,1.4-2.4c0.9-0.5,1.9-0.7,2.8-0.7c2.8,0,5,1,6.7,3.1l7-7c-1.7-1.8-3.9-3.1-6.4-
     [truncated]\t<path class="logo-st0" d="M277.4,51.9v-4.2c-0.1-2.7-0.5-5.2-1.2-7.4c-0.8-2.4-2-4.5-3.5-6.2c-1.5-1.7-3.3-3-5.5-3.9 c-2.2-0.9-4.6-1.4-7.2-1.4c-2.9,0-5.6,0.5-8.1,1.4c-2.5,0.9-4.7,2.2-6.6,3.9c-1.9,1.7-3.3,3.8-4.4,6.2c-1.1,2.4-1.
     [truncated]\t<path class="logo-st1" d="M52.6,38.9l2.6-9.2h4.6l1.8-6.6c0.6-2,1.3-4,2.2-5.8c0.8-1.8,2-3.4,3.4-4.8c1.4-1.4,3.2-2.5,5.3-3.3 c2.1-0.8,4.8-1.2,7.9-1.2c0.8,0,1.5,0,2.3,0.1c-0.7-2.9-3.3-5-6.3-5.1H11.9c-3.6,0-6.5,3-6.5,6.6V67l10.5
     [truncated]\t<path class="logo-st2" d="M82.1,17.9c-0.5-0.1-1.1-0.2-1.8-0.2c-1.8,0-3.3,0.4-4.5,1.2c-1.1,0.8-2.1,2.4-2.8,4.9l-1.7,5.9h6.5l1.6,5.1 l-4.2,4.1h-6.5l-7.9,28H49.4l7.9-28h-4.4L52,39.5c0,0.2,0.1,0.5,0.1,0.7c0.2,2.3-0.1,4.9-0.9,7.7
     [truncated]\t<path class="logo-st0" d="M277.6,68.5h0.8c0.4,0,0.6-0.1,0.7-0.2c0.1-0.1,0.2-0.2,0.2-0.4c0-0.1,0-0.2-0.1-0.3c-0.1-0.1-0.1-0.2-0.3-0.2 c-0.1,0-0.3-0.1-0.6-0.1h-0.7V68.5z M277,70.6v-3.8h1.3c0.5,0,0.8,0,1,0.1c0.2,0.1,0.4,0.2,0.5
    </svg>\t\t\t\t<span style="color:white;font-size:.5em;text-transform:uppercase;letter-spacing:1px;">Community Edition</span>\n
    \t\t\t</a>\n
    \t\t</div>\n
    \t\t<div class="collapse navbar-collapse" id="pf-navbar">\n
    \t\t\t<ul class="nav navbar-nav">\n
    \t\t\t\t\t\t\t<li class="dropdown">\n
    \t\t\t\t\t<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-expanded="false">\n
    \t\t\t\t\t\tSystem\t\t\t\t\t\t<span class="caret"></span>\n
    \t\t\t\t\t</a>\n
    \t\t\t\t\t<ul class="dropdown-menu" role="menu"><li><a href="/system_advanced_admin.php" class="navlnk" >Advanced</a></li>\n
    <li><a href="/system_camanager.php" class="navlnk" >Cert. Manager</a></li>\n
    <li><a href="/system.php" class="navlnk" >General Setup</a></li>\n
    <li><a href="/system_hasync.php" class="navlnk" >High Avail. Sync</a></li>\n
    <li><a href="/index.php?logout" class="navlnk" usepost>Logout (admin)</a></li>\n
    <li><a href="/pkg_mgr_installed.php" class="navlnk" >Package Manager</a></li>\n
    <li><a href="/system_gateways.php" class="navlnk" >Routing</a></li>\n
    <li><a href="/wizard.php?xml=setup_wizard.xml" class="navlnk" >Setup Wizard</a></li>\n
    <li><a href="/pkg_mgr_install.php?id=firmware" class="navlnk" >Update</a></li>\n
    <li><a href="/system_usermanager.php" class="navlnk" >User Manager</a></li>\n
    </ul>\n
    \t\t\t\t</li>\n
    \n
    \t\t\t\t<li class="dropdown">\n
    \t\t\t\t\t<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-expanded="false">\n
    \t\t\t\t\t\tInterfaces\t\t\t\t\t\t<span class="caret"></span>\n
    \t\t\t\t\t</a>\n
    \t\t\t\t\t<ul class="dropdown-menu" role="menu"><li><a href="/interfaces_assign.php" class="navlnk" >Assignments</a></li>\n
     <li class="divider"></li><li><a href="/interfaces.php?if=wan" class="navlnk" >WAN</a></li>\n
    <li><a href="/interfaces.php?if=lan" class="navlnk" >LAN</a></li>\n
    </ul>\n
    \t\t\t\t</li>\n
    \n
    \t\t\t\t<li class="dropdown">\n
    \t\t\t\t\t<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-expanded="false">\n
    \t\t\t\t\t\tFirewall\t\t\t\t\t\t<span class="caret"></span>\n
    \t\t\t\t\t</a>\n
    \t\t\t\t\t<ul class="dropdown-menu" role="menu"><li><a href="/firewall_aliases.php" class="navlnk" >Aliases</a></li>\n
    <li><a href="/firewall_nat.php" class="navlnk" >NAT</a></li>\n
    <li><a href="/firewall_rules.php" class="navlnk" >Rules</a></li>\n
    <li><a href="/firewall_schedule.php" class="navlnk" >Schedules</a></li>\n
    <li><a href="/firewall_shaper.php" class="navlnk" >Traffic Shaper</a></li>\n
    <li><a href="/firewall_virtual_ip.php" class="navlnk" >Virtual IPs</a></li>\n
    </ul>\n
    \t\t\t\t</li>\n
    \n
    \t\t\t\t<li class="dropdown">\n
    \t\t\t\t\t<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-expanded="false">\n
    \t\t\t\t\t\tServices\t\t\t\t\t\t<span class="caret"></span>\n
    \t\t\t\t\t</a>\n
    \t\t\t\t\t<ul class="dropdown-menu" role="menu"><li><a href="/services_acb.php" class="navlnk" >Auto Config Backup</a></li>\n
    <li><a href="/services_captiveportal.php" class="navlnk" >Captive Portal</a></li>\n
    <li><a href="/services_dhcp_relay.php" class="navlnk" >DHCP Relay</a></li>\n
    <li><a href="/services_dhcp.php" class="navlnk" >DHCP Server</a></li>\n
    <li><a href="/services_dhcpv6_relay.php" class="navlnk" >DHCPv6 Relay</a></li>\n
    <li><a href="/services_dhcpv6.php" class="navlnk" >DHCPv6 Server &amp; RA</a></li>\n
    <li><a href="/services_dnsmasq.php" class="navlnk" >DNS Forwarder</a></li>\n
    <li><a href="/services_unbound.php" class="navlnk" >DNS Resolver</a></li>\n
    <li><a href="/services_dyndns.php" class="navlnk" >Dynamic DNS</a></li>\n
    <li><a href="/services_igmpproxy.php" class="navlnk" >IGMP Proxy</a></li>\n
    <li><a href="/load_balancer_pool.php" class="navlnk" >Load Balancer</a></li>\n
    <li><a href="/services_ntpd.php" class="navlnk" >NTP</a></li>\n
    <li><a href="/services_pppoe.php" class="navlnk" >PPPoE Server</a></li>\n
    <li><a href="/services_snmp.php" class="navlnk" >SNMP</a></li>\n
    <li><a href="/pkg_edit.php?xml=miniupnpd.xml" class="navlnk" >UPnP &amp; NAT-PMP</a></li>\n
    <li><a href="/services_wol.php" class="navlnk" >Wake-on-LAN</a></li>\n
    </ul>\n
    \t\t\t\t</li>\n
    \n
    \t\t\t\t<li class="dropdown">\n
    \t\t\t\t\t<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-expanded="false">\n
    \t\t\t\t\t\tVPN\t\t\t\t\t\t<span class="caret"></span>\n
    \t\t\t\t\t</a>\n
    \t\t\t\t\t<ul class="dropdown-menu" role="menu"><li><a href="/vpn_ipsec.php" class="navlnk" >IPsec</a></li>\n
    <li><a href="/vpn_l2tp.php" class="navlnk" >L2TP</a></li>\n
    <li><a href="/vpn_openvpn_server.php" class="navlnk" >OpenVPN</a></li>\n
    </ul>\n
    \t\t\t\t</li>\n
    \n
    \t\t\t\t<li class="dropdown">\n
    \t\t\t\t\t<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-expanded="false">\n
    \t\t\t\t\t\tStatus\t\t\t\t\t\t<span class="caret"></span>\n
    \t\t\t\t\t</a>\n
    \t\t\t\t\t<ul class="dropdown-menu" role="menu"><li><a href="/status_captiveportal.php" class="navlnk" >Captive Portal</a></li>\n
    <li><a href="/status_carp.php" class="navlnk" >CARP (failover)</a></li>\n
    <li><a href="/index.php" class="navlnk" >Dashboard</a></li>\n
    <li><a href="/status_dhcp_leases.php" class="navlnk" >DHCP Leases</a></li>\n
    <li><a href="/status_dhcpv6_leases.php" class="navlnk" >DHCPv6 Leases</a></li>\n
    <li><a href="/status_unbound.php" class="navlnk" >DNS Resolver</a></li>\n
    <li><a href="/status_filter_reload.php?user=true" class="navlnk" >Filter Reload</a></li>\n
    <li><a href="/status_gateways.php" class="navlnk" >Gateways</a></li>\n
    <li><a href="/status_interfaces.php" class="navlnk" >Interfaces</a></li>\n
    <li><a href="/status_ipsec.php" class="navlnk" >IPsec</a></li>\n
    <li><a href="/status_lb_pool.php" class="navlnk" >Load Balancer</a></li>\n
    <li><a href="/status_monitoring.php" class="navlnk" >Monitoring</a></li>\n
    <li><a href="/status_ntpd.php" class="navlnk" >NTP</a></li>\n
    <li><a href="/status_openvpn.php" class="navlnk" >OpenVPN</a></li>\n
    <li><a href="/status_pkglogs.php" class="navlnk" >Package Logs</a></li>\n
    <li><a href="/status_queues.php" class="navlnk" >Queues</a></li>\n
    <li><a href="/status_services.php" class="navlnk" >Services</a></li>\n
    <li><a href="/status_logs.php" class="navlnk" >System Logs</a></li>\n
    <li><a href="/status_graph.php" class="navlnk" >Traffic Graph</a></li>\n
    <li><a href="/status_upnp.php" class="navlnk" >UPnP &amp; NAT-PMP</a></li>\n
    </ul>\n
    \t\t\t\t</li>\n
    \n
    \t\t\t\t<li class="dropdown">\n
    \t\t\t\t\t<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-expanded="false">\n
    \t\t\t\t\t\tDiagnostics\t\t\t\t\t\t<span class="caret"></span>\n
    \t\t\t\t\t</a>\n
    \t\t\t\t\t<ul class="dropdown-menu" role="menu"><li><a href="/diag_arp.php" class="navlnk" >ARP Table</a></li>\n
    <li><a href="/diag_authentication.php" class="navlnk" >Authentication</a></li>\n
    <li><a href="/diag_backup.php" class="navlnk" >Backup &amp; Restore</a></li>\n
    <li><a href="/diag_command.php" class="navlnk" >Command Prompt</a></li>\n
    <li><a href="/diag_dns.php" class="navlnk" >DNS Lookup</a></li>\n
    <li><a href="/diag_edit.php" class="navlnk" >Edit File</a></li>\n
    <li><a href="/diag_defaults.php" class="navlnk" >Factory Defaults</a></li>\n
    <li><a href="/diag_halt.php" class="navlnk" >Halt System</a></li>\n
    <li><a href="/diag_limiter_info.php" class="navlnk" >Limiter Info</a></li>\n
    <li><a href="/diag_ndp.php" class="navlnk" >NDP Table</a></li>\n
    <li><a href="/diag_packet_capture.php" class="navlnk" >Packet Capture</a></li>\n
    <li><a href="/diag_pf_info.php" class="navlnk" >pfInfo</a></li>\n
    <li><a href="/diag_pftop.php" class="navlnk" >pfTop</a></li>\n
    <li><a href="/diag_ping.php" class="navlnk" >Ping</a></li>\n
    <li><a href="/diag_reboot.php" class="navlnk" >Reboot</a></li>\n
    <li><a href="/diag_routes.php" class="navlnk" >Routes</a></li>\n
    <li><a href="/diag_smart.php" class="navlnk" >S.M.A.R.T. Status</a></li>\n
    <li><a href="/diag_sockets.php" class="navlnk" >Sockets</a></li>\n
    <li><a href="/diag_dump_states.php" class="navlnk" >States</a></li>\n
    <li><a href="/diag_states_summary.php" class="navlnk" >States Summary</a></li>\n
    <li><a href="/diag_system_activity.php" class="navlnk" >System Activity</a></li>\n
    <li><a href="/diag_tables.php" class="navlnk" >Tables</a></li>\n
    <li><a href="/diag_testport.php" class="navlnk" >Test Port</a></li>\n
    <li><a href="/diag_traceroute.php" class="navlnk" >Traceroute</a></li>\n
    </ul>\n
    \t\t\t\t</li>\n
    \n
    \t\t\t\t<li class="dropdown">\n
    \t\t\t\t\t<a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-expanded="false">\n
    \t\t\t\t\t\tHelp\t\t\t\t\t\t<span class="caret"></span>\n
    \t\t\t\t\t</a>\n
    \t\t\t\t\t<ul class="dropdown-menu" role="menu"><li><a href="/help.php?page=services_ntpd.php" target="_blank" class="navlnk" >About this Page</a></li>\n
    <li><a href="https://redirects.netgate.com/issues" target="_blank" class="navlnk" >Bug Database</a></li>\n
    <li><a href="https://redirects.netgate.com/docs" target="_blank" class="navlnk" >Documentation</a></li>\n
    <li><a href="https://redirects.netgate.com/fbsdhandbook" target="_blank" class="navlnk" >FreeBSD Handbook</a></li>\n
    <li><a href="https://redirects.netgate.com/support" target="_blank" class="navlnk" >Paid Support</a></li>\n
    <li><a href="https://redirects.netgate.com/book" target="_blank" class="navlnk" >pfSense Book</a></li>\n
    <li><a href="https://redirects.netgate.com/forum" target="_blank" class="navlnk" >User Forum</a></li>\n
    <li><a href="https://redirects.netgate.com/survey_1" target="_blank" class="navlnk" >User survey</a></li>\n
    </ul>\n
    \t\t\t\t</li>\n
    \n
    \t\t\t</ul>\n
    \t\t\t<ul class="nav navbar-nav navbar-right">\n
    \t\t\t\t\t\t\t\t\t<li class="dropdown">\n
    \t\t\t\t\t\t<a href="/index.php?logout" usepost>\n
    \t\t\t\t\t\t\t<i class="fa fa-sign-out" title="Logout (admin@fw01.fruitinc.xyz)"></i>\n
    \t\t\t\t\t\t</a>\n
    \t\t\t\t\t</li>\n
    \t\t\t</ul>\n
    \t\t</div>\n
    \t</div>\n
    </nav>\n
    \n
    <div class="container static" >\n
    \n
    \n
    \t<header class="header">\n
    \n
    <ol class="breadcrumb"><li>Services</li><li><a href="/services_ntpd.php">NTP</a></li><li><a href="/services_ntpd.php">Settings</a></li></ol>\t\t<ul class="context-links">\n
    \n
    \t\n
    \t\n
    \t\n
    \t\n
    \t\n
    \t\n
    <li><a href="#" id="restartservice-ntpd" ><i class="fa fa-repeat" title="Restart Service"></i></a>\n
     [truncated]<a href="#" id="stopservice-ntpd"><i class="fa fa-stop-circle-o" title="Stop Service"></i></a></li><li><a href="status_ntpd.php" title="Related status"><i class="fa fa-bar-chart"></i></a></li><li><a href="status_logs.php?logfi
    \t\t\t<a href="/help.php?page=services_ntpd.php" target="_blank" title="Help for items on this page">\n
    \t\t\t\t<i class="fa fa-question-circle"></i>\n
    \t\t\t</a>\n
    \t\t</li>\n
    \t\t\t</ul>\n
    \t</header>\n
     [truncated]<div class="alert alert-success clearfix" role="alert"><button type="button" class="close" data-dismiss="alert" aria-label="Close"><span aria-hidden="true">&times;</span></button><div class="pull-left">The changes have been ap
    \t\t\t<div class="panel panel-default">\n
    \t\t<div class="panel-heading">\n
    \t\t\t<h2 class="panel-title">NTP Server Configuration</h2>\n
    \t\t</div>\n
    \t\t<div class="panel-body">\n
    \t\t\t\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t<span>Interface</span>\n
    \t\t</label>\n
    \t\t\t<div class="col-sm-10">\n
    \t\t\t<select class="form-control" name="interface[]" id="interface[]" multiple="multiple">\n
    \t\t<option value="wan">WAN</option><option value="lan" selected>LAN</option>\n
    \t</select>\n
    \n
     [truncated]\t\t<span class="help-block">Interfaces without an IP address will not be shown.<br />Selecting no interfaces will listen on all interfaces with a wildcard.<br />Selecting all interfaces will explicitly listen on only the inte
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group repeatable" max_repeats="10" max_repeats_alert="10 is the maximum number of configured servers.">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t<span>Time Servers</span>\n
    \t\t</label>\n
    \t\t\t<div class="col-sm-3">\n
    \t\t<input class="form-control" name="server0" id="server0" type="text" value="0.pfsense.pool.ntp.org" placeholder="Hostname">\n
    \n
    \t\t\n
    \t</div>\t<div class="checkbox col-sm-1">\n
    \t\t<label class="chkboxlbl"><input name="servprefer0" id="servprefer0" type="checkbox" value="yes"></label>\n
    \n
    \t\t<span class="help-block">Prefer</span>\n
    \t</div>\t<div class="checkbox col-sm-1">\n
    \t\t<label class="chkboxlbl"><input name="servselect0" id="servselect0" type="checkbox" value="yes"></label>\n
    \n
    \t\t<span class="help-block">No Select</span>\n
    \t</div>\t<div class="checkbox col-sm-1">\n
    \t\t<label class="chkboxlbl"><input name="servispool0" id="servispool0" type="checkbox" value="yes" checked="checked"></label>\n
    \n
    \t\t<span class="help-block">Is a Pool</span>\n
    \t</div>\t<div class="col-sm-1">\n
    \t\t<button class="btn btn-warning" type="submit" value="Delete" name="deleterow0" id="deleterow0"><i class="fa fa-trash icon-embed-btn"> </i>Delete</button>\n
    \n
    \t\t\n
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t<span>Add</span>\n
    \t\t</label>\n
    \t\t\t<div class="col-sm-10">\n
    \t\t<button class="btn btn-success" type="submit" value="Add" name="addrow" id="addrow"><i class="fa fa-plus icon-embed-btn"> </i>Add</button>\n
    \n
    \t\t\n
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t\n
    \t\t</label>\n
    \t\t\t<div class="col-sm-10">\n
    \t\t\n
    \n
     [truncated]\t\t<span class="help-block">NTP will only sync if a majority of the servers agree on the time.  For best results you should configure between 3 and 5 servers (<a target="_blank" href="https://support.ntp.org/bin/view/Support/
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t<span>Orphan Mode</span>\n
    \t\t</label>\n
    \t\t\t<div class="col-sm-10">\n
    \t\t<input class="form-control" name="ntporphan" id="ntporphan" type="text" value="" placeholder="12">\n
    \n
     [truncated]\t\t<span class="help-block">Orphan mode allows the system clock to be used when no other clocks are available. The number here specifies the stratum reported during orphan mode and should normally be set to a number high enou
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t<span>NTP Graphs</span>\n
    \t\t</label>\n
    \t\t\t<div class="checkbox col-sm-10">\n
    \t\t<label class="chkboxlbl"><input name="statsgraph" id="statsgraph" type="checkbox" value="yes"> Enable RRD graphs of NTP statistics (default: disabled).</label>\n
    \n
    \t\t\n
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t<span>Logging</span>\n
    \t\t</label>\n
    \t\t\t<div class="checkbox col-sm-10">\n
    \t\t<label class="chkboxlbl"><input name="logpeer" id="logpeer" type="checkbox" value="yes"> Log peer messages (default: disabled).</label>\n
    \n
    \t\t\n
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t\n
    \t\t</label>\n
    \t\t\t<div class="checkbox col-sm-10">\n
    \t\t<label class="chkboxlbl"><input name="logsys" id="logsys" type="checkbox" value="yes"> Log system messages (default: disabled).</label>\n
    \n
    \t\t<span class="help-block">These options enable additional messages from NTP to be written to the System Log <a href="status_logs.php?logfile=ntpd">Status > System Logs > NTP</a>.</span>\n
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t<span>Statistics Logging</span>\n
    \t\t</label>\n
    \t\t\t<div class="col-sm-10">\n
    \t\t<button class="btn btn-info btn-sm" type="button" value="Display Advanced" name="btnadvstats" id="btnadvstats"><i class="fa fa-cog icon-embed-btn"> </i>Display Advanced</button>\n
    \n
    \t\t<span class="help-block">Warning: These options will create persistent daily log files in /var/log/ntp.</span>\n
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t\n
    \t\t</label>\n
    \t\t\t<div class="checkbox col-sm-10">\n
    \t\t<label class="chkboxlbl"><input name="clockstats" id="clockstats" type="checkbox" value="yes"> Log reference clock statistics (default: disabled).</label>\n
    \n
    \t\t\n
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t\n
    \t\t</label>\n
    \t\t\t<div class="checkbox col-sm-10">\n
    \t\t<label class="chkboxlbl"><input name="loopstats" id="loopstats" type="checkbox" value="yes"> Log clock discipline statistics (default: disabled).</label>\n
    \n
    \t\t\n
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t\n
    \t\t</label>\n
    \t\t\t<div class="checkbox col-sm-10">\n
    \t\t<label class="chkboxlbl"><input name="peerstats" id="peerstats" type="checkbox" value="yes"> Log NTP peer statistics (default: disabled).</label>\n
    \n
    \t\t\n
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t<span>Leap seconds</span>\n
    \t\t</label>\n
    \t\t\t<div class="col-sm-10">\n
    \t\t<button class="btn btn-info btn-sm" type="button" value="Display Advanced" name="btnadvleap" id="btnadvleap"><i class="fa fa-cog icon-embed-btn"> </i>Display Advanced</button>\n
    \n
     [truncated]\t\t<span class="help-block">Leap seconds may be added or subtracted at the end of June or December. Leap seconds are administered by the <a target="_blank" href="https://www.iers.org">IERS</a>, who publish them in their Bulle
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t\n
    \t\t</label>\n
    \t\t\t<div class="col-sm-10">\n
    \t\t\t<textarea rows="5" class="form-control" name="leaptext" id="leaptext"></textarea>\n
    \n
    \t\t<span class="help-block">Enter Leap second configuration as text OR select a file to upload.</span>\n
    \t</div>\n
    \t\t\n
    \t</div>\t<div class="form-group">\n
    \t\t<label class="col-sm-2 control-label">\n
    \t\t\t\n
    \t\t</label>\n
    \t\t\t<div class="col-sm-10">\n
    \t\t<input class="btn-default" name="leapfile" id="leapfile" type="file">\n
    \n
    \t\t\n
    \t</div>\n
    \t\t\n
    \t</div>\n
    \t\t</div>\n
    \t</div><div class="col-sm-10 col-sm-offset-2"><button class="btn btn-primary" type="submit" value="Save" name="save" id="save"><i class="fa fa-save icon-embed-btn"> </i>Save</button></div>\n
    \t</form>\n
    <script type="text/javascript">\n
    //<![CDATA[\n
    \t// If this variable is declared, any help text will not be deleted when rows are added\n
    \t// IOW the help text will appear on every row\n
    \tretainhelp = true;\n
    </script>\n
    \n
    <script type="text/javascript">\n
    //<![CDATA[\n
    events.push(function() {\n
    \n
    \t// Show advanced stats options ============================================\n
    \tvar showadvstats = false;\n
    \n
    \tfunction show_advstats(ispageload) {\n
    \t\tvar text;\n
    \t\t// On page load decide the initial state based on the data.\n
    \t\tif (ispageload) {\n
    \t\t\tshowadvstats = false;\n
    \t\t} else {\n
    \t\t\t// It was a click, swap the state.\n
    \t\t\tshowadvstats = !showadvstats;\n
    \t\t}\n
    \n
    \t\thideCheckbox('clockstats', !showadvstats);\n
    \t\thideCheckbox('loopstats', !showadvstats);\n
    \t\thideCheckbox('peerstats', !showadvstats);\n
    \n
    \t\tif (showadvstats) {\n
    \t\t\ttext = "Hide Advanced";\n
    \t\t} else {\n
    \t\t\ttext = "Display Advanced";\n
    \t\t}\n
    \t\t$('#btnadvstats').html('<i class="fa fa-cog"></i> ' + text);\n
    \t}\n
    \n
    \t$('#btnadvstats').click(function(event) {\n
    \t\tshow_advstats();\n
    \t});\n
    \n
    \t// Show advanced leap second options ======================================\n
    \tvar showadvleap = false;\n
    \n
    \tfunction show_advleap(ispageload) {\n
    \t\tvar text;\n
    \t\t// On page load decide the initial state based on the data.\n
    \t\tif (ispageload) {\n
    \t\t\tshowadvleap = false;\n
    \t\t} else {\n
    \t\t\t// It was a click, swap the state.\n
    \t\t\tshowadvleap = !showadvleap;\n
    \t\t}\n
    \n
    \t\thideInput('leaptext', !showadvleap);\n
    \t\thideInput('leapfile', !showadvleap);\n
    \n
    \t\tif (showadvleap) {\n
    \t\t\ttext = "Hide Advanced";\n
    \t\t} else {\n
    \t\t\ttext = "Display Advanced";\n
    \t\t}\n
    \t\t$('#btnadvleap').html('<i class="fa fa-cog"></i> ' + text);\n
    \t}\n
    \n
    \t$('#btnadvleap').click(function(event) {\n
    \t\tshow_advleap();\n
    \t});\n
    \n
    \t// Set initial states\n
    \tshow_advstats(true);\n
    \tshow_advleap(true);\n
    \n
    \t// Suppress "Delete row" button if there are fewer than two rows\n
    \tcheckLastRow();\n
    });\n
    //]]>\n
    </script>\n
    \n
    \t</div>\n
    \t<footer class="footer">\n
    \t\t<div class="container">\n
    \t\t\t<p class="text-muted">\n
    \t\t\t\t<a id="tpl" style="display: none;" href="#" title="Top of page"><i class="fa fa-caret-square-o-up pull-left"></i></a>\n
     [truncated]\t\t\t\t<a target="_blank" href="https://pfsense.org">pfSense</a> is developed and maintained by <a target="_blank" href="https://netgate.com">Netgate. </a> &copy; ESF 2004 - 2020<a target="_blank" href="https://pfsense.org/li
    \t\t\t</p>\n
    \t\t</div>\n
    \t</footer>\n
    \n
    \t<!-- This use of filemtime() is intended to fool the browser into reloading the file (not using the cached version) if the file is changed -->\n
    \n
    \t<script src="/vendor/jquery/jquery-3.4.1.min.js?v=1580510450"></script>\n
     \t<script src="/vendor/jquery-ui/jquery-ui-1.12.1.min.js?v=1580510450"></script>\n
    \t<script src="/vendor/bootstrap/js/bootstrap.min.js?v=1580510450"></script>\n
    \t<script src="/js/pfSense.js?v=1580510450"></script>\n
    \t<script src="/js/pfSenseHelpers.js?v=1580510450"></script>\n
    \t<script src="/js/polyfills.js?v=1580510450"></script>\n
    \t<script src="/vendor/sortable/sortable.js?v=1580510450"></script>\n
    \n
    \t<script type="text/javascript">\n
    \t//<![CDATA[\n
    \t\t// Un-hide the "Top of page" icons if the page is larger than the window\n
    \t\tif ($(document).height() > $(window).height()) {\n
    \t\t    $('[id^=tp]').show();\n
    \t\t}\n
    \t//]]>\n
    \t</script>\n
    <script type="text/javascript">CsrfMagic.end();</script></body>\n
    </html>\n
```

extracting useful info:

```
    <ol class="breadcrumb"><li>Services</li><li><a href="/services_ntpd.php">NTP</a></li><li><a href="/services_ntpd.php">Settings</a></li></ol>\t\t<ul class="context-links">\n

    \t\t\t<select class="form-control" name="interface[]" id="interface[]" multiple="multiple">\n
    \t\t<option value="wan">WAN</option><option value="lan" selected>LAN</option>\n
```

flag<lan:ntp>
