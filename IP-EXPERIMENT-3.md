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

### 8. Inspect the contents of the first HTTP GET request from your browser to the server. Do you see an 
“IF-MODIFIED-SINCE” line in the HTTP GET? 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/55d6115a-cb46-4c68-9960-c91dd8035447)
>From the Above Screenshot, IF-MODIFIED-SINCE line is not present in the first HTTP GET request from browser to the server.

### 9. Inspect the contents of the server response. Did the server explicitly return the contents of the file? How can you tell?  
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/8900b47e-aad2-4a9a-a06a-c14e2564228a)
>From the Above Screenshot, Server is explicitly returning the contents of the file that can be viewed in Line-based text data: text/html (10 lines)

### 10. Now inspect the contents of the second HTTP GET request from your browser to the server. Do you see an “IF-MODIFIED-SINCE:” line in the HTTP GET? What information follows the “IF-MODIFIED SINCE:” header? 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/8dc6c129-b076-4a83-bd9c-d22ce90a286c)
>From the Above Screenshot, IF-MODIFIED-SINCE line is present, If-Modified-Since: Fri, 04 Aug 2023 05:59:02 GMT\r\n

### 11. What is the HTTP status code and phrase returned from the server in response to this second HTTP GET? Did the server explicitly return the file’s contents? Explain.
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/6984c089-8759-495d-8f36-940c1cf4f684)
>From the Above Screenshot, the HTTP status and phrase returned from the server in response is HTTP/1.1 304 Not Modified\r\n

### 12. How many HTTP GET request messages did your browser send? Which packet number in the trace contains the GET message for the Bill or Rights?  
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/c1706569-a300-40e7-ab80-18b39847d91e)
>From the Above Screenshot, 2 HTTP GET request messages is sent to the server, Packet number 204 Contains the GET message for the Bill or Rights.

### 13. Which packet number in the trace contains the status code and phrase associated with the response to the HTTP GET request?  
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/eeaa3afe-d207-4625-8023-60ab02eefc50)
>From the Above Screenshot, Packet number 224 contains the status code 200 and phrase associated with the response to the HTTP GET request is HTTP/1.1 200 OK (text/html)

### 14. What is the status code and phrase in the response? 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/78ef34d9-9600-4a41-9129-8535cedbb5d7)
>From the Above Screenshot, The Status code and phrase in the response is 200 OK

### 15. How many data-containing TCP segments were needed to carry the single HTTP response and the text of the Bill of Rights? 
![image](https://github.com/giridharan-6701/IP_Lab_Assignment_2/assets/94190302/9dea5dd1-33f4-433d-a56f-8f3bc41c19aa)
>From the Above Screenshot, 4 data TCP Segment is needed to carry the single HTTP Response 1460,1460,1460,480 for a total of 4860 Bytes.

