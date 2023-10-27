DESCRIPTION:

This web setup is a bigger version of the one described earlier. In this version, 
all weak links have been removed and each of the main parts (web server, application server, and database servers) 
have been moved to their own GNU/Linux servers. The secret code protection (SSL) doesn’t stop at the load-balancer 
and each server’s network is protected with a security guard (firewall) and they’re also watched over (monitored).

ABOUT THIS INFRASTRUCTURE

Firewall between each server:

This is like having a security guard for each server to protect it from unwanted visitors, 
instead of just one guard for a single server.

ISSUES WITH THIS INFRASTRUCTURE.
High maintenance costs: Moving each of the main parts to its own server means that more servers 
would have to be bought and the company’s electricity bill would go up with the addition of new servers.
Some of the company’s money would have to be used to buy the servers and pay for the electricity needed 
to keep all the servers (new and old ones) running.
