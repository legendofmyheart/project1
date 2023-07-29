Welcome to the IP_Lab_Assignment_2!

## 1. Understand PING and document it, then answer the following question:
PING Command is used to the reachability of the host, for example, I want to open www.google.com before entering the URL in the Browser I want to check whether www.google.com is reachable or not. For this Purpose, I can use ping command to check whether www.google.com is reachable.In Simple Words, PING Command can be used to check whether the communication between devices happens or not.

### Use ping on google.com and document your results on the output you received. [Find the IP address, Time to live value, and round-trip time value from the results you got].
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/e00524d3-2fd4-4c5a-b938-1108c76edf37)

By Performing PING Command for the given URL www.google.com, The Following Values is Obtained:

IP Address(www.google.com): - 142.250.67.36

Time to live Value (TTL): - 57
TTL in PING Command describes the number of hops the data packets take to reach the destination host in this case www.google.com. The Default Value of TTL is 255, It gets decremented while traversing through each router, If TTL decrements to 0, The data packets will be dropped.

Round Trip Time Value (in Milliseconds): - Minimum = 8ms, Maximum = 9ms, Average = 8ms.
RTT in PING Command is used to measure the time taken by the data packets to reach the destination host. One advantage of measuring this value is that we can check the network latency.

### By default, ping will send 4 packets to check the details, here you must send 8 packets to 
check the output over google.com. Explain the purpose of doing it.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/addaa84d-1fe6-4b62-8b4c-76c0d8fb8eaf)

The purpose of doing ping -n 8 www.google.com is that we can analyze more about the network performance and network latency and by sending incremental value of data packets can help us analyze about data packets loss.

### Ping your local host. Explain the purpose of doing it.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/9cdac284-c21d-4750-9c0e-c970ca1bc98e)

The main purpose of performing ping command in our local host is to check whether the TCP/IP Stack is performing well or not. It is Basic network troubleshooting command to check connectivity issues like TCP/IP Performing properly or not whether there is a problem in network software. For example, you detect a network connectivity issue while send a ICMP echo request packets to the destination, first step of troubleshooting is to check whether the local system network connectivity, for this we can use ping command on our local host to check there is a problem in our network before checking the external network connection.

## 2. Read the Unix manual page for traceroute OR help for tracert. Experiment with the various options. Describe the three things that you found most useful in the result. 

TRACERT Command displays the path that data packets hops from different networks to reach the destination host.

### Try tracert over google.com 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/47706a01-f3dd-4913-b37b-542f334a8972)

### Type tracert -d google.com
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/9beb91e2-e587-4a02-a09a-9630e3384a8d)

### How many hops is your machine away from google.com?
From the Above Diagram, Data packet makes 10 hops to reach the destination host(www.google.com)

### Wait for a while and execute the same command again. Is the output the same as the 
first time? Observe and compare the difference and explain the reason. 



## 3. You have to read about NETSTAT from the manual page or help, before answering the below questions:

NETSTAT abbreviation is Network Statistics command used to display information regarding network statistics that is it displays All TCP Active Connection, Port in which the computer is listening, Ethernet Statistics that contain number of packets sent and received and the routing table of each protocol like tcp, udp, etc.

### Use netstat to display information about the routing table. 
To display information about routing table we can use -r flag (netstat -r).
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/84d363b1-5f62-4139-9042-576373bce9b7)

### Use netstat to display about ethernet statistics. 
To Display information about ethernetet statistics we can use -e flag in netstat (netstat -e).
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/e0f4f69c-8d21-4c0c-be04-a732bec2fe85)

## What is the purpose of NSLOOKUP? Answer the following questions below: 
NSLOOKUP command is used to resolve Domain name with its corresponding IP address.

### Use nslookup to find out the internet address of the domain amrita.edu.
We can use the following command to find out internet address of the domain amrita.edu (nslookup amrita.edu)
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/9cd3333f-606b-463c-9786-e35e915c3cec)

### What is the mail exchanger for the domain google.com.
To find out the mail exchanger for the domain google.com we can use the following nslookup command with the flag -type=MX (MX abbreviates Mail Exchanger) that is used to find out the mail exchanger for the mentioned domain.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/b674bd3a-f972-4f47-ba65-121f3787a8f5)

### What is the name server for amrita.edu
To Find the name server for amrita.edu we can use nslookup command with the following flag nslookup -type=NS amrita.edu NS abbreviates for Name Server.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/291f1302-88e4-4061-8da6-b4448ad98ac2)

## What is ARP and RARP? Answer the following questions below: 
ARP (Address Resolution Protocol) is used to map the IP Address with the corresponding MAC address. In the Other hand RARP (Reverse Address Resolution Protocol) is used to map MAC Address with the Corresponding IP Address.

### Use arp command to find the gateway address and host systems hardware address.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/617fa359-9f82-4d31-83d9-e14112f90822)
From the Above Screenshot Gateway Address is 192.168.1.1

### How do you find the arp entries for a particular interface?


