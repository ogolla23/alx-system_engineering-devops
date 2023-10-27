DESCRIPTION 

This is a setup with three servers that is safe, watched over, and sends out coded traffic.

ABOUT THIS INFRASTRUCTURE

Firewalls: 
Firewalls are like security guards for the network. They stand between the internal and 
external network and stop unwanted visitors from getting in.

SSL certificate: 
The SSL certificate is like a secret code. It scrambles the traffic between the web servers 
and the outside network to stop eavesdroppers from spying on the traffic and stealing valuable information. 
The SSL certificates ensure privacy, integrity, and identification.

Monitoring clients: 
Monitoring clients are like health check-ups for the servers. They keep an eye on how the 
servers are doing, check their overall health, and alert the administrators if something’s not right. 
The monitoring tool keeps an eye on the servers and gives important information about how the servers 
are doing to the administrators. It automatically checks if the servers are reachable, measures how 
fast they respond, and alerts for problems like missing or corrupt files, security risks, and many other issues.

ISSUES WITH THIS INFRASTRUCTURE.

If SSL stops at the load balancer level, it would leave the traffic between the load balancer and the web servers uncoded.

Having only one MySQL server is a problem because it can’t grow bigger if needed and can be a single 
point of failure for the web infrastructure.

Having servers with all the same parts would make those parts fight for resources on the server like CPU, 
Memory, I/O, etc., which can lead to poor performance and also make it hard to find where a problem is coming from. 
A setup like this isn’t easily scalable
