---
title: "The structure of the Palmetto Cluster"
teaching: 15
exercises: 0
questions:
- "How can I access the Palmetto cluster from my local machine?"
objectives:
- "Logging into Palmetto from a local Mac / Windows computer."
---

Basic structure of the cluster:

<img src="../fig/palmetto-structure.png" alt="Structure of the Palmetto Cluster" style="height:350px">

The computers that make up the Palmetto cluster are called *nodes*. Most of the nodes on Palmetto are *compute nodes*, 
that can perform fast calculations on large amounts of data. There is also a special node called the *login node*; it runs the server, 
which works like the interface 
between the cluster 
and the outside world. The people with Palmetto accounts can log into the server by running a client (such as `ssh`) on their local machines. 
Our client program passes our login credentials to this server, and if we are allowed to log in, the server runs a shell for us. 
Any commands that we enter into this shell are executed not by our own machines, but by the login node.

Another special node is the *scheduler*; Palmetto users can get from the
login node to the compute nodes by submitting a request to the scheduler, and the scheduler will assign them to the most appropriate compute node.
Palmetto also has a few so-called "service" nodes, which serve special purposes like transfering code and data to and from the cluster, and hsting web applications.

To see the hardware specifications of the compute nodes, please type

~~~
$ cat /etc/hardware-table
~~~
{: .bash}


This will print out a text file with the hardware info. Please make sure you type exactly as shown; Linux is case-sensitive space-sensitive, 
and typo-sensitive. The output will look something like this:

BLAH BLAH





hardware table
whatsfree
Login and compute nodes
node ownership
condominium model