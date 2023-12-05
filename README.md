# Cisco-Packet-Tracer-


Cisco Representation
![image](https://github.com/cemreucar/Cisco-Packet-Tracer-/assets/59101099/85070b2c-f00c-46f5-b57f-b9b612edb0e6)


![image](https://github.com/cemreucar/Cisco-Packet-Tracer-/assets/59101099/20bf7280-b64e-406f-a7fc-8d64f7d3a07b)

Configuration of basic settings for
each router
First we have to disable DNS lookup. Because we
don’t use DNS server and If we don’t need to have a
DNS server configured for our router, we can use            

the no ip domain-lookup command to disable the
DNS translation process. The no ip domain
lookup tells the router to stop interacting with any
DNS servers. Having a DNS server configured is
then a useless thing because it is not going to be
used, anyway.

![image](https://github.com/cemreucar/Cisco-Packet-Tracer-/assets/59101099/328590ef-e1a1-4b1e-8e55-110f8fdd3d0c)

To configure a device name, we use hostname
command therefore we specify the name for the router
as shown in the topology.

We have to set an encrypted password to prevent
unauthorized access to the router and in this lab the
password will be ‘siena’.I used enable secret command
to assign a password.
To configure the ip address of the Fast
Ethernet connection, I use the necessity commands.

Next step I have to configure an ospf with the
process ID of 1.Also, I set the router ID
1.1.1.1 which is written in the lab file.To
assign the router id I use router-id
command.Then, I set the network ip adresses
and areas.I had to use the wildcard mask. A
wildcard mask allows or denies all the traffic
from a network IP address. The wildcard mask
tells the router which bits in the IP address
need to match the access list and which do not.
Enabling passive interfaces in our network devices mean
that:

OSPF continues to announce or advertise the interface’s
connected network.

OSPF routers stop sending OSPF Hellos on the interface.

On the interface, OSPF no longer processes any received
Hellos.

Passive interfaces are commonly used to reduce the amount
of routing protocol traffic on a network, or to prevent the
routing protocol from propagating to specific areas of the
network.

Passive interfaces can be configured on a Cisco router using
the "passive-interface" command under the routing protocol
configuration mode.
In DNS Server 2, I wrote an basic index which you see
from the figure on right that says ‘Welcome to University
of Siena’. You can see this page when you connect to the
web server and then write the ip address of the DNS
server on related laptops and pcs.

In DNS Server 1 , it’s an automatic page about cisco
packet tracer.It is written in html.
Ospf Router Types

Backbone Router

This is a router which resides in backbone area. The backbone area
is set to area 0. The routers in Area 0 in this project are R2 and R3.

Area Border Router (ABR)

Area Border Router is a router that has interfaces attached to 2 or
more areas. It can route between areas. ABRs are exit points for
the area, which means that routing information destined for another
area can get there only via the ABR of the local area. In this case
area border routers are R1, R2 and R3.

Internal Router

This is a router that has all of its interfaces in the same area. The
internal router in this lab is R4.
There are several types of OSPF routes:

Inter-area routes: These routes are used to reach destinations within
another area of an OSPF routing domain. They are advertised by the
Area Border Router (ABR) and installed in the routing table of routers
within the area. Inter-area routes are represented in the routing table
with the prefix "O IA" (OSPF inter-area).

Intra-area routes: These routes are used to reach destinations within
the same area of an OSPF routing domain. They are advertised by the
routers within the area and installed in the routing table of routers
within the area. Intra-area routes are represented in the routing table
with the prefix "O" (OSPF intra-area)

To display OSPF routing tables on a router.

What is the indication of O IA?

A way would be to use the "show ip route" command, which will display
the entire routing table for the router. Inter-area routes will be identified
with the prefix "O IA" in the routing table.

MD5 authentication provides a mechanism to ensure that
the routing updates exchanged between routers are
authentic. It does this by adding a message digest (or hash)
to the OSPF routing updates. The message digest is
calculated using a shared secret key, and it is included in
the OSPF packets. When a router receives an OSPF packet,
it calculates the message digest using the shared secret key
and compares it to the message digest included in the
packet. If the two message digests match, the router
considers the packet to be authentic and processes the
routing information and in this project the key is
seminar2022.

It's a good idea to verify that OSPF is functioning correctly
before configuring OSPF authentication because it makes
troubleshooting easier, ensures network stability, helps ease
the configuration process and avoids unnecessary changes.
Designated Router (DR) and Backup Designated Router (BDR)

In OSPF, a DR (Designated Router) and a BDR
(Backup Designated Router) are elected on a
multi-access network, such as a broadcast or a
non-broadcast multi-access (NBMA) network, to reduce
the number of adjacencies and the amount of OSPF
control traffic on the network.

The DR is the router that is responsible for sending and
receiving OSPF routing updates to and from all other
routers on the network. The BDR is the backup router
that takes over the role of the DR if the DR becomes
unavailable.

The DR and BDR are elected based on the highest
OSPF router priority and the highest router ID. If the
priorities are the same, the router with the highest IP
address will become the DR. If there is a tie in both
priority and router ID, the router
