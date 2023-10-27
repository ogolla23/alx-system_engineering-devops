DESCRIPTION

This is a spread-out web setup that aims to lighten the load on the main server by sharing some of the burden with a duplicate server. This is made possible with the help of another server whose job is to evenly distribute the workload 
between the two servers 

ABOUT THIS INFRASTRUCTURE

The load balancer’s distribution algorithm: The HAProxy load balancer uses the Round Robin distribution algorithm. 
Think of it like a game of “pass the parcel”, where each server gets a turn to handle requests, one after the other. 
This keeps things fair and balanced because each server gets an equal chance to work.

The setup enabled by the load balancer: The HAProxy load balancer sets up an Active-Passive system. 
It’s like a tag team in wrestling. In an Active-Active setup, all servers (or wrestlers) are in the ring at the same time. 
But in an Active-Passive setup, one server (or wrestler) is active while the other waits outside the ring, ready to tag in 
if needed.

How a database Primary-Replica (Master-Slave) cluster works: A Primary-Replica setup is like a teacher-student relationship. 
The Primary server (or teacher) can both give information (write) and provide information (read), while the Replica server 
(or student) can only provide information (read). Whenever the teacher writes something new on the board, the student copies 
it down.

The difference between the Primary node and the Replica node in regard to the application: The Primary node is like a writer 
who creates all the new content for a website, while the Replica node is like a reader who can only view and share this content,
which reduces the reading load on the writer.

ISSUES WITH THE INFRASTRUCTURE.

Multiple Single Points Of Failure (SPOF): This is like having several weak links in a chain. For instance, if the main 
MySQL database server breaks down, the whole website would be stuck and unable to make changes (like adding or removing users). 
The server with the load balancer and the application server that connects to the main database server are also weak links that 
could break the chain.

Security issues: The data sent over the network isn’t locked in a safe (encrypted using an SSL certificate), so thieves 
(hackers) can easily take a peek. There’s also no security guard (firewall) to block unwanted visitors (unauthorized IPs).

No monitoring: We have no way of checking on each server’s health since they’re not being monitored. It’s like having 
several plants but not checking if they need water or sunlight.
