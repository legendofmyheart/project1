Welcome to the IP_Lab_Assignment_2!

## 1. Understand PING and document it, then answer the following question:
PING Command is used to the reachability of the host, for example, I want to open www.google.com before entering the URL in the Browser I want to check whether www.google.com is reachable or not. For this Purpose, I can use ping command to check whether www.google.com is reachable.In Simple Words, PING Command can be used to check whether the communication between devices happens or not.

### Use ping on google.com and document your results on the output you received. [Find the IP address, Time to live value, and round-trip time value from the results you got].
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/e00524d3-2fd4-4c5a-b938-1108c76edf37)

By Performing PING Command for the given URL www.google.com, The Following Values is Obtained:

> IP Address(www.google.com): - 142.250.67.36

>Time to live Value (TTL): - 57

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

### Wait for a while and execute the same command again. Is the output the same as the first time? Observe and compare the difference and explain the reason. 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/6086a0dd-7011-48b2-bd4b-69b331116184)
The Number of hops that is taken initially is different from current hops, This is because there may be an network latency or hardware issues in the path, so number the hops differ on time to time due to any interferences in the path.


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

> From the Above Screenshot Gateway Address is 192.168.1.1

### How do you find the arp entries for a particular interface?
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/73cf0e47-99cb-44aa-b753-817a2a2a7e5c)
> To find the arp entries for a particular interface we can use -a flag along with the IP address
> arp -a 224.0.0.18


### How do delete an arp entry? 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/ca535e64-969d-46b2-a89f-19fd553bb7db)
To Delete an arp entry we can use -d flag. 
> arp -d <IP_ADDR>

### How do you add and arp entry in arpcache? 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/d69e0aab-347f-4c11-bcd4-2df57bc9b9e0)
To add an entry in arpcache we can use -s flag along with ip address and the associated MAC address.
> arp -s 224.0.0.252 01-00-5e-00-00-fc

## 6. Read about TCPDUMP tool [use manual page]. Answer the questions below: (1 marks)

### a. Using tcpdump, get the information about the general incoming network traffic with domain names.

> To get information about the general incoming traffic with domain names we can use the following command:
> sudo tcpdump -v -i eth0 host bbc.com
> -v means verbose output
> -i eth0 specifies the interface in which the incoming traffic need to be captured.
> host bbc.com specifies the domain name.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/9dc10573-167c-418a-b28e-a7b49de91c77)

### b. Using tcpdump, get the information about the general incoming network traffic with ip address on specific interface.

> To get information about the general incoming traffic with ip address on specific interface we can use the following command:
> sudo tcpdump -v -i eth0 "net 10.0.2.1"
> -v means verbose output
> -i eth0 Specifies the interface
>"net 10.0.2.15" specifies the ip address in which the incoming traffic need to be captured.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/cac31eb4-b937-40bf-847d-835ccdf6bce8)


## 7. Use Wireshark (Latest version) to solve the below scenarios
### Use Evidence.pcapng as evidence file to answer the below questions.
### 1. You, as a SOC analyst noted that someone tried to send information (PING) to unknown IP address, and you are suspecting some malicious information might transferred in it. Analyze the traffic file.

### Find the data transferred.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/3e8bc3e8-704a-4b74-8fd2-f04644fd7108)
> To Find the Data transferred, From the Above Statement it is mentioned that Someone tried to send information (PING) to unknown IP Address. PING command sends ICMP Packet, In Filter Column type ICMP to list only the ICMP Packets.

### Find the source and destination IP of that log.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/a71fe56f-b963-4f62-a3ec-148042d282bc)
> To Find the source and destination IP Address of the log navigate to bottom left panel, Click the Internet Protocol Version 4.

### Find the Data length (Bytes) and verify the checksum status on destination.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/e0ab5bfa-fd52-4489-8367-3215de07f0cc)

> In Wireshark, By Default the checksum is disabled, to enable it navigate preferences>advanced Search IP checksum enable it. Now we can be able to check the checksum of the message.

## 2. Now you have found that some kind of file has been downloaded by insider in
unencrypted web traffic. Your task is to

>We can verify the unencrypted web traffic we can search for any HTTP packets.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/b0b8a87b-bdb7-47e9-9446-3613450b703f)

### Find the name and type of file.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/23c7ae92-cba8-4d3f-a450-6385d1318f32)
> File Name: - 1.jpg
> Type of File: - jpeg

### Export that file from that web traffic, then analyze the file for any secret information.
> 1. To Export the file click on File in Left top corner->Click Export Objects->HTTP.
> 2. A New Box will open HTTP Object List, There we can preview the image and also we can download it.
![1](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/d64c46c1-79a8-4f79-a5ee-52a2edde4347)

### Find the hostname in which the file is stored
From the HTTP Object List we can able to see the hostname in which the file is stored.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/268edb3e-f08e-4313-89cc-7a88ff194640)
> Hostname: 192.168.31.67

## 3. Based upon their activities, auditing team has started investigation against them and found that the insider passed some sensitive information via call to someone. The traffic has been captured.
### a. Analyze the traffic and find those conversations and extract the sensitive information in it.
> To Analyze traffic in call we can use VOIP CALLS Options in Telephony Column and we can search for SIP Protocol in Filter Column as this protocol is used in voice communication.
> 1. Search sip in filter column 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/2f82906e-37ac-4195-b12e-2216f45bdacc)

> 2. Click Telephony>VOIP CALLS
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/db4a547f-ee5d-4b5a-955c-d25038c29321)

> 3. To play the VoIP Call Uncheck the Limit Display Filter, Click Play Stream.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/0ee9d6d0-6a96-456e-ba68-5545a6616f24)

> 4. We can also download the audio using export option.

> 5. The information in the Voice call states that "hi customer support this is actually here I would the password to clear this level ok I don't need this password anyone else as in engine Mass Effect beers in Battlefield who is it out thank you alright thank you."

### Find the call-ID when the status of the call is ringing.
> Call-ID: 01caab9b53b12efe00d3493a67ff695d@192.168.31.8:5060

## 4. On further investigation, you have a suspect on some wireless device communications. List out the Bluetooth devices communications from this traffic and find the details about native Bluetooth adapter.

>To List out the Bluetooth Device Communication Navigate Wireless> Bluetooth Devices.
>To Find details about native Bluetooth adapter click on Dropdown and select option other than All interfaces.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/570a46f6-0de4-4bd7-afdc-83ca12aa7b33)

### a. Analyze the captured WPA handshake from this traffic and report in detail about it to your administrator.

### b. Geo locate all the endpoint of wireless devices.
To Locate all the endpoint of wireless devices: -
> Download latest Maxmind database Directories.
> Navigate Edit>Preferences>Name Resolution>Add Downloaded GeoIP File Directory in Maxmind database directories.
