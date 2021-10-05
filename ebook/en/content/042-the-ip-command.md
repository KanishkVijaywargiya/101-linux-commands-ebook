# 042 The ip Command

ip command in Linux is present in the net-tools which is used for performing several network administration tasks. 
IP stands for Internet Protocol. 
This command is used to show or manipulate routing, devices, and tunnels. 
It is similar to ifconfig command.
ip command is used to perform several tasks like assigning an address to a network interface or configuring network interface parameters.
It can perform several other tasks like configuring and modifying the default and static routing, setting up tunnel over IP, listing IP addresses and property information, modifying the status of the interface, assigning, deleting and setting up IP addresses and routes.

Syntax:
ip [ OPTIONS ] OBJECT { COMMAND | help }

<!--1-->
Options:
* address    :     This option is used to show all IP addresses associated on all network devices.
  syntax     :     ip address
  Description:     This will show the information related to all interfaces available on our system, but if we want                to view the information of any particular interface, add the options show followed by the name of               the particular network interface.
ip address show (interface)
Example:
ip address show enp3s0

<!--2-->
* link       :     It is used to display link layer information, it will fetch characteristics of the link layer                     devices currently available. Any networking device which has a driver loaded can be classified as                 an available device.
  syntax     :     ip link
  Description:     This link option when used with -s option is used to show the statistics of the various network                 interfaces.
ip -s link
And, to get information about a particular network interface, add option show followed by the name of the particular network interface.

ip -s link show (interface)
Example:
ip -s link show enp3s0
  
<!--3-->
* route       :    This command helps you to see the route packets your network will take as set in your routing                     table. The first entry is the default route.
  syntax     :     ip route
  
<!--4-->
* add        :    This is used to assign an IP address to an interface.
  syntax     :    ip a add (ip_address) dev interface
  Example    :    ip a add 192.168.1.50/24 dev enp3s0

<!--5-->
* del        :    This is used to delete an assigned IP address to an interface.
  syntax     :    ip a del (ip_address) dev interface
  Example    :    ip a del 192.168.1.50/24 dev enp3s0

<!--6-->
* up         :    This option enables a network interface.
  syntax     :    ip link set (interface) up
  Example    :    ip link set enp3s0 up

<!--7-->
* down       :    This option disables a network interface.
  syntax     :    ip link set (interface) down
  Example    :    ip link set enp3s0 down

<!--8-->
* monitor    :    This command can monitor and displays the state of devices, addresses and routes continuously.
  syntax     :    ip monitor
  
<!--9-->
* help       :    This command is used as a help to know more about ip command.
  syntax     :    ip help

<!--10-->
* neighbour  :    This command is used to view the MAC address of the devices connected to your system.
  syntax     :    ip neighbour


** STABLE: This means that the neighbor is valid, but is probably already unreachable, so the kernel will try to             check it at the first transmission.

** REACHABLE: This means that the neighbor is valid and reachable.

** DELAY: This means that a packet has been sent to the stable neighbor and the kernel is waiting for confirmation.


** Modifying ARP(address resolution protocol) entries:

* Delete an ARP entry:
    ip neighbour del (ip_address) dev interface
    
    Example: ip neighbour del 192.168.0.200 dev enp3s0

* Add an ARP entry:
    ip neighbour add (ip_address) dev interface

    Example: ip neighbour add 192.168.0.200 dev enp3s0
