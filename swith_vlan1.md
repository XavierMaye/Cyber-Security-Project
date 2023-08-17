Switch VLAN1 192.168.100.254


1.3 Switch SW1 - Initial setup
VLAN1 - 192.168.100.254/24 for remote management via SSH
No port security

use Putty   >>> Serial >>> open.

Switch#show vlan
Switch#show vlan brief


Switch#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#interface vlan1
Switch(config-if)#ip address 192.168.100.254 255.255.255.0
Switch(config-if)#no shutdown
Switch(config-if)#end
Switch#show
sswitch# copy running-config startup-config

switch# show ip interface brief

setting default-gatway ,so you can access swith from ouside.

Switch(config)#ip default-gateway 192.168.100.1



set the password

Switch>enable
Switch#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#line vty 0 4
Switch(config-line)#login
% Login disabled on line 1, until 'password' is set

Switch(config-line)#password cisco
Switch(config-line)#exit
