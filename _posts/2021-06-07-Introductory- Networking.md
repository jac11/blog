---
layout: post
image: /assets/images/IntroductoryNetworking.png
image1: /assets/images/network/1.png
image2: /assets/images/network/2.png
image3: /assets/images/network/3.png
image4: /assets/images/network/4.png
image5: /assets/images/network/5.png
image6: /assets/images/network/6.png
image7: /assets/images/network/7.png
image8: /assets/images/network/8.png
image9: /assets/images/network/9.png
image10: /assets/images/network/10.png
image11: /assets/images/network/11.png
image12: /assets/images/network/12.png
image13: /assets/images/network/13.png
image14: /assets/images/network/14.png
image15: /assets/images/network/15.png
image16: /assets/images/network/16.png
image17: /assets/images/network/17.png
image18: /assets/images/network/18.png
image19: /assets/images/network/19.png
categories: TryHackMe
---
# *Welcome To  Introductory Networking tryhackme room 'writeup'*
* <p style='color:red'>  by : Ahmedhammad </p>
```
```
## --info 

******
* room name : Introductory Networking
* category : Network
* link :
[https://www.tryhackme.com/room/introtonetworking](https://www.tryhackme.com/room/introtonetworking)

## - The topics that we're going to cover in this room are:
* The OSI Model
* The TCP/IP Model
* How these models look in practice
* An introduction to basic networking tools

```
```
<h2 style='color:blue'>  Starting Point </h2>
_______________________________________________

## task1 : Introduction 
<h3 style='color:red'> Qesution 1 : Let's get started!</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3> 
![]({{ page.image1 | relative_url }})

_______________________________________________

## Task 2 : The OSI Model: An Overview 

<h3 style='color:red'> Qesution 1 : Which layer would choose to send data over TCP or UDP? </h3>
<h3 style='color:green'> Correct Answer  : 4 </h3> 
Layer 4  Transport :
 first purpose is to choose the protocol over which the data is to be transmitted. The two most common protocols in the transport layer are TCP (Transmission Control Protocol) and UDP (User Datagram Protocol); with TCP the transmission is connection-based which means that a connection between the computers is established and maintained for the duration of the request.
 ![]({{ page.image2 | relative_url }})

<h3 style='color:red'> Qesution 2 : Which layer checks received packets to make sure that they haven't been corrupted?</h3>
<h3 style='color:green'> Correct Answer  : 2 </h3> 
The data link layer also serves an important function when it receives data, as it checks the received information to make sure that it hasn't been corrupted during transmission, which could well happen when the data is transmitted by layer 1: the physical layer. 

<h3 style='color:red'> Qesution 3 : In which layer would data be formatted in preparation for transmission?</h3>
<h3 style='color:green'> Correct Answer  : 2  </h3> 
Additionally, it's also the job of the data link layer to present the data in a format suitable for transmission.
![]({{ page.image3 | relative_url }})

<h3 style='color:red'> Qesution 4 : Which layer transmits and receives data?</h3>
<h3 style='color:green'> Correct Answer  : 1 </h3> 
It's the job of the physical layer to convert the binary data of the transmission into signals and transmit them across the network, as well as receiving incoming signals and converting them back into binary data
![]({{ page.image4 | relative_url }})

<h3 style='color:red'> Qesution 5 : Which layer encrypts, compresses, or otherwise transforms the initial data to give it a standardised format?</h3>
<h3 style='color:green'> Correct Answer  : 6 </h3> 
The presentation layer translates the data into a standardised format, as well as handling any encryption, compression or other transformations to the data. With this complete.
![]({{ page.image5 | relative_url }})


<h3 style='color:red'> Qesution 6 : Which layer tracks communications between the host and receiving computers?</h3>
<h3 style='color:green'> Correct Answer  : 5 </h3> 
This is what allows you to make multiple requests to different endpoints simultaneously without all the data getting mixed up (think about opening two tabs in a web browser at the same time)! When the session layer has successfully logged a connection between the host and remote computer the data is passed down to Layer 
![]({{ page.image6 | relative_url }})

<h3 style='color:red'> Qesution 7 : Which layer accepts communication requests from applications? </h3>
<h3 style='color:green'> Correct Answer  : 7  </h3> 
The application layer of the OSI model essentially provides networking options to programs running on a computer.
![]({{ page.image7 | relative_url }})

<h3 style='color:red'> Qesution 8 : Which layer handles logical addressing?</h3>
<h3 style='color:green'> Correct Answer  : 3  </h3> 
At this stage we're working with what is referred to as Logical addressing (i.e. IP addresses) which are still software controlled. Logical addresses are used to provide order to networks, categorising them and allowing us to properly 
![]({{ page.image8 | relative_url }})

<h3 style='color:red'> Qesution 9 : When sending data over TCP, what would you call the "bite-sized" pieces of data? </h3>
<h3 style='color:green'> Correct Answer  : Segments </h3>
the transport layer then divides the transmission up into bite-sized pieces (over TCP these are called segments, over UDP they're called datagrams), which makes it easier to transmit the message successfully  

<h3 style='color:red'> Qesution 10 : [Research] Which layer would the FTP protocol communicate with?</h3>
<h3 style='color:green'> Correct Answer  : 7 </h3> 
FTP runs on the application layer 

![]({{ page.image9 | relative_url }})
<h3 style='color:red'> Qesution 11 : Which transport layer protocol would be best suited to transmit a live video?</h3>
<h3 style='color:green'> Correct Answer  : UDP  </h3> 

With UDP, the opposite is true; packets of data are essentially thrown at the receiving computer -- if it can't keep up then that's its problem (this is why a video transmission over something like Skype can be pixelated if the connection is bad)

_______________________________________________


## Task 3 :  Encapsulation

<h3 style='color:red'> Qesution 1 : How would you refer to data at layer 2 of the encapsulation process (with the OSI model)?</h3>
<h3 style='color:green'> Correct Answer  : Frames  </h3> 
![]({{ page.image10 | relative_url }})

<h3 style='color:red'> Qesution 2 : How would you refer to data at layer 4 of the encapsulation process (with the OSI model), if the UDP protocol has been selected?</h3>
<h3 style='color:green'> Correct Answer  : Datagrams  </h3> 
over TCP these are called segments, over UDP they're called datagrams

<h3 style='color:red'> Qesution 3 : What process would a computer perform on a received message?</h3>
<h3 style='color:green'> Correct Answer  : De-encapsulation  </h3> 
When the message is received by the second computer, it reverses the process -- starting at the physical layer and working up until it reaches the application layer, stripping off the added information as it goes. This is referred to as de-encapsulation. 
![]({{ page.image11| relative_url }})

<h3 style='color:red'> Qesution 4 : Which is the only layer of the OSI model to add a trailer during encapsulation?</h3>
<h3 style='color:green'> Correct Answer  : Data Link  </h3> 

<h3 style='color:red'> Qesution 5 : Does encapsulation provide an extra layer of security (Aye/Nay)?</h3>
<h3 style='color:green'> Correct Answer  : Aye </h3> 
The data link layer also adds a piece on at the end of the transmission, which is used to verify that the data has not been corrupted on transmission; this also has the added bonus of increased security, as the data can't be intercepted and tampered with without breaking the trailer. This whole process is referred to as encapsulation; the process by which data can be sent from one computer to another.

![]({{ page.image12 | relative_url }})

-----------------------------------------------------------------
## Task 4 : The TCP/IP Model

<h3 style='color:red'> Qesution 1 : Which model was introduced first, OSI or TCP/IP?</h3>
<h3 style='color:green'> Correct Answer  : TCP/IP  </h3>
![]({{ page.image13 | relative_url }})

<h3 style='color:red'> Qesution 2 : Which layer of the TCP/IP model covers the functionality of the Transport layer of the OSI model (Full Name)?</h3>
<h3 style='color:green'> Correct Answer  : Transport  </h3>


<h3 style='color:red'> Qesution 3 :Which layer of the TCP/IP model covers the functionality of the Session layer of the OSI model (Full Name)?</h3>
<h3 style='color:green'> Correct Answer  : Application </h3>


<h3 style='color:red'> Qesution 4 : The Network Interface layer of the TCP/IP model covers the functionality of two layers in the OSI model. These layers are Data Link, and?.. (Full Name)?</h3>
<h3 style='color:green'> Correct Answer  : Physical  </h3>


<h3 style='color:red'> Qesution 5 : Which layer of the TCP/IP model handles the functionality of the OSI network layer?</h3>
<h3 style='color:green'> Correct Answer  : Internet </h3>
![]({{ page.image14 | relative_url }})

<h3 style='color:red'> Qesution 6 : What kind of protocol is TCP?</h3>
<h3 style='color:green'> Correct Answer  : Connection-based  </h3>
TCP is a connection-based protocol.

<h3 style='color:red'> Qesution 7: What is SYN short for?</h3>
<h3 style='color:green'> Correct Answer  : Synchronise </h3>
When you attempt to make a connection, your computer first sends a special request to the remote server indicating that it wants to initialise a connection. This request contains something called a SYN (short for synchronise) bit.

<h3 style='color:red'> Qesution 8 : What is the second step of the three way handshake?</h3>
<h3 style='color:green'> Correct Answer  : SYN/ACK </h3>
client send SYN --- server will replay SYN/ACK 
![]({{ page.image15 | relative_url }})

<h3 style='color:red'> Qesution 9 : What is the short name for the "Acknowledgement" segment in the three-way handshake?</h3>
<h3 style='color:green'> Correct Answer  : ACK  </h3>
acknowledgement bit called ACK

----------------------------------------------------------------------

## Task 5 : Networking Tools Ping 

<h3 style='color:red'> Qesution 1 : What command would you use to ping the bbc.co.uk website?</h3>
<h3 style='color:green'> Correct Answer  : ping bbc.co.uk  </h3>


<h3 style='color:red'> Qesution 2 : Ping muirlandoracle.co.uk What is the IPv4 address??</h3>
<h3 style='color:green'> Correct Answer  : 217.160.0.152 </h3>
ping muirlandoracle.co.uk
PING muirlandoracle.co.uk (217.160.0.152) 56(84) bytes of data.
64 bytes from 217-160-0-152.elastic-ssl.ui-r.com (217.160.0.152): icmp_seq=1 ttl=55 time=122 ms
64 bytes from 217-160-0-152.elastic-ssl.ui-r.com (217.160.0.152): icmp_seq=2 ttl=55 time=122 ms


<h3 style='color:red'> Qesution 3: What switch lets you change the interval of sent ping requests?</h3>
<h3 style='color:green'> Correct Answer  : -i </h3>
open terminal the type man ping 

![]({{ page.image16 | relative_url }})

<h3 style='color:red'> Qesution 4 : What switch would allow you to restrict requests to IPv4?</h3>
<h3 style='color:green'> Correct Answer  : -4  </h3>
open terminal and type ping --help

![]({{ page.image17 | relative_url }})

<h3 style='color:red'> Qesution 5 : What switch would give you a more verbose output?</h3>
<h3 style='color:green'> Correct Answer  : -v  </h3>
open terminal and type ping --help

![]({{ page.image18 | relative_url }})


----------------------------------------------------------

## Task 6 : Networking Tools Traceroute 

<h3 style='color:red'> Qesution 1: use traceroute on tryhackme.com / Can you see the path your request has taken?</h3>
<h3 style='color:green'> Correct Answer  : No answer needed </h3>


<h3 style='color:red'> Qesution 2: What switch would you use to specify an interface when using Traceroute?</h3>
<h3 style='color:green'> Correct Answer  : -i </h3>

open terminal and type traceroute --help 

<h3 style='color:red'> Qesution 3: What switch would you use if you wanted to use TCP SYN requests when tracing the route?</h3>
<h3 style='color:green'> Correct Answer  : -T </h3>

open terminal and  type traceroute --help 

![]({{ page.image19 | relative_url }})

<h3 style='color:red'> Qesution 4: [Lateral Thinking] Which layer of the TCP/IP model will traceroute run on by default (Windows)?</h3>
<h3 style='color:green'> Correct Answer  : Internet </h3>

----------------------------------------------------------------------

## Task 7  : Networking Tools WHOIS 

<h3 style='color:red'> Qesution 1: Perform a whois search on facebook.com / Can you see the path your request has taken?</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3>

<h3 style='color:red'> Qesution 2: What is the registrant postal code for facebook.com?</h3>
<h3 style='color:green'> Correct Answer  : 94025 </h3>


<h3 style='color:red'> Qesution 3: When was the facebook.com domain first registered?</h3>
<h3 style='color:green'> Correct Answer  : 29/03/1997 </h3>

<h3 style='color:red'> Qesution 4: Perform a whois search on microsoft.com</h3>
<h3 style='color:green'> Correct Answer  : No answer needed </h3>

<h3 style='color:red'> Qesution 5: Which city is the registrant based in?</h3>
<h3 style='color:green'> Correct Answer  : Redmondd </h3>

<h3 style='color:red'> Qesution 6: [OSINT] What is the name of the golf course that is near the registrant address for microsoft.com?</h3>
<h3 style='color:green'> Correct Answer  : Bellevue Golf Course </h3>

<h3 style='color:red'> Qesution 7: What is the registered Tech Email for microsoft.com?</h3>
<h3 style='color:green'> Correct Answer  : msnhst@microsoft.com </h3>


---------------------------------------------------------------------

## Task 8  : Networking Tools Dig  

<h3 style='color:red'> Qesution 1: What is DNS short for?</h3>
<h3 style='color:green'> Correct Answer  : Domain Name System</h3>

<h3 style='color:red'> Qesution 2: What is the first type of DNS server your computer would query when you search for a domain?</h3>
<h3 style='color:green'> Correct Answer  : Recursive </h3>

<h3 style='color:red'> Qesution 3: What type of DNS server contains records specific to domain extensions (i.e. .com, .co.uk*, etc)*? Use the long version of the name.</h3>
<h3 style='color:green'> Correct Answer  : Top-Level Domain</h3>


<h3 style='color:red'> Qesution 4: Where is the very first place your computer would look to find the IP address of a domain?</h3>
<h3 style='color:green'> Correct Answer  : Local Cache </h3>


<h3 style='color:red'> Qesution 5: [Research] Google runs two public DNS servers. One of them can be queried with the IP 8.8.8.8, what is the IP address of the other one?</h3>
<h3 style='color:green'> Correct Answer  : 8.8.8.8 </h3>

<h3 style='color:red'> Qesution 6: If a DNS query has a TTL of 24 hours, what number would the dig query show?</h3>
<h3 style='color:green'> Correct Answer  : 86400 </h3>

-------------------------------------------------------------------------------

## Task 9  :  Networking Tools Dig 

<h3 style='color:red'> Qesution 1: Read the final thoughts</h3>
<h3 style='color:green'> Correct Answer  : No answer needed </h3>

--------------------------------------------------------------------------

## the End 
 
