DESCRIPTION

This is a basic web infrastructure that supports a website accessible at www.foobar.com. The server’s network lacks protective measures such as firewalls or SSL certificates. Each element of the system, including the database and application server, 
utilizes the resources (CPU, RAM, and SSD) allocated by the server

ABOUT INFRASTRUCTURE

A server is a computer hardware or software that provides services to other computers, 
which are usually referredto as clients.

The role of the domain name is to provide a human-friendly alias for an IP address. 
For example, the domain name www.wikipedia.org is easier to recognize and remember 
than 91.198.174.192. The IP address and domain name alias is mapped in the Domain Name System (DNS).

The type of DNS record www is in www.foobar.com is an A record. This can be checked by running dig 
www.foobar.com. Note: the results might be different but for the infrastructure 
in this design, an A record is used. An A record—also known as a DNS host record, stores a 
hostname and its corresponding IPv4 address.

The role of the web server is to accept requests via HTTP or secure HTTP (HTTPS) and respond with the 
content of the requested resource or an error message.
The role of the application server is to install, operate and host applications and associated 
services for end users, IT services and organizations and facilitates the hosting and delivery 
of high-end consumer or business applications.

The role of the database is to maintain a collection of organized information that can easily be 
accessed, managed and updated.

The server uses the TCP/IP protocol suite to communicate with the client 
(computer of the user requesting the website). This is a set of rules that dictate how data is 
exchanged over the internet.

ISSUES WITH THIS INFRASTRUCTURE.

Single Point Of Failure (SPOF): This is like having only one road to get to a destination. 
If something happens to that road (like the MySQL database server going down), you can’t reach your 
destination (the entire site would be down).

Downtime during maintenance: Imagine this as a shop that has to close down completely when it needs 
to be cleaned or repaired. Since there’s only one server, the website would be closed (experiencing downtime) 
during maintenance.

Difficulty in scaling with increased traffic: This is like a small shop that gets crowded and slow when 
too many customers come in at once. Because one server contains all the required components, 
it can quickly run out of resources or slow down when it starts receiving a lot of requests.


