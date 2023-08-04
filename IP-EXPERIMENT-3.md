# IP LAB ASSIGNMENT 3
1. Let’s begin our exploration of HTTP by downloading a very simple HTML file - one that is very 
short and contains no embedded objects. Do the following:  
1. Start up your web browser.  
2. Start the Wireshark packet sniffer, as described in the Introductory lab (but don’t yet begin packet 
capture). Enter “http” (just the letters, not the quotation marks) in the display-filter-specification 
window, so that only captured HTTP messages will be displayed later in the packet-listing window. 
(We’re only interested in the HTTP protocol here, and don’t want to see the clutter of all captured 
packets).  
3. Wait more than one minute (we’ll see why shortly), and then begin Wireshark packet capture.  
4. Enter the following into your browser 
http://gaia.cs.umass.edu/wireshark-labs/HTTP-wireshark-file1.html  
Your browser should display a very simple, one-line HTML file.  
5. Stop Wireshark packet capture.

## By looking at the information in the HTTP GET and response messages, answer the following questions.

### 1. Is your browser running HTTP version 1.0 or 1.1? What version of HTTP is the server running? 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/1f5c9b35-7104-4ed8-acff-9f95afd8a5c0)
>From the Above Screenshot, Both Browser and Server is running HTTP 1.1

### 2. What languages (if any) do your browser indicate that it can accept to the server?
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/923bb5a6-79b4-461a-96bd-273c974faa08)
> From the Above Screenshot our browser indicates that it accepts en-US language to the server.

### 3. What is the IP address of your computer? Of the gaia.cs.umass.edu server?  
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/53a6a5da-81ef-4b8b-b4f3-8266e097966e)
>From the Above Screenshot,
>IP Address of Computer: 10.11.137.245
>IP Address of gaia.cs.umass.edu server: 128.119.245.12

### 4. What is the status code returned from the server to your browser? 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/91bcc682-5957-4a58-bebc-49511450dec1)
>From the Above Screenshot,
>The status code returned from the server to your browser is HTTP/1.1 200 OK\

### 5. When was the HTML file that you are retrieving last modified at the server?  
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/44679496-0cc5-4ae2-9676-83cde6681ff6)
>From the Above Screenshot,
>The HTML file that are retrieved last modified at the server is Last-Modified: Fri, 04 Aug 2023 05:59:02 GMT\r\n

### 6. How many bytes of content are being returned to your browser? 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/5ae2cc4c-e7a9-43b9-9e2a-0125b34ac985)
>From the Above Screenshot,
>The Content length is 128. (File Data:128 bytes).

### 7. By inspecting the raw data in the packet content window, do you see any headers within the data that are not displayed in the packet-listing window? If so, name one. 

