Opening up ports is something that comes up often in setting up a production environment.

Port 80 is reserved for root.  It is usually set up for the main website so that visitors to a site don't have to put the port number at the end.
For example, www.yourwebsite.com:3000
Instead, the visitor goes to www.yourwebsite.com

Example port set up for SSL:
iptables -I INPUT -p tcp --dport 443 -j ACCEPT

You can check what ports are set up using the "iptables" unix command or if you're on AWS, you would set up a security group and create an inbound protocol.
