Context:  One host has a condition preventing direct communication with internet hosts.  This condition could be a simple firewall rule, or it could be a routing rule, for example due to use of a VPN.

Problem:  The host should accept SSH connections from the internet.

Solution:  Proxy.  First forward the unique SSH port for the target host through the NAT gateway to a proxy host, then deploy this role to the proxy host.

Incoming connections will be proxied to the target host.  Provided the proxy host is on the LAN, connections should succeed.

Bugs:  This could be more generically named and written, but my first use case happens to be my file server in its capacity as a backup target.

