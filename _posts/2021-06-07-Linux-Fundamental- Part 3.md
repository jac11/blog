---
layout: post
image: /assets/images/LinuxFundamentalsPart3.png
image1: /assets/images/Linux/1.png
image2: /assets/images/Linux/2.png
image3: /assets/images/Linux/3.png
image4: /assets/images/Linux/4.png
image5: /assets/images/Linux/5.png
image6: /assets/images/Linux/6.png
categories: TryHackMe
---
# *Welcome To  Linux Fundamentals Part3 'writeup'*
* <p style='color:red'>  by : Ahmedhammad </p>
```
```
## --info 

******
* room name : LinuxFundamentalsPart3
* category : Linux Fundamental
* link :
[https://tryhackme.com/room/linuxfundamentalspart3](https://tryhackme.com/room/linuxfundamentalspart3)

* Welcome to part three (and the finale) of the Linux Fundamentals module. So far, throughout the series, you have got hands-on with some fundamental concepts and used some important commands. This room is going to showcase some useful utilities and applications that you are likely to use day-to-day. You're also going to advance your Linux-fu skills by learning about automation, package management, and service/application logging. 

Watch the video by tryhackme :  
[https://www.youtube.com/watch?v=bwgaZCb2ft8](https://www.youtube.com/watch?v=bwgaZCb2ft8)

```
```
<h2 style='color:blue'>  Starting Point </h2>
_______________________________________________


## task1 : Introduction 

<h3 style='color:red'> Qesution 1 : Let's proceed!</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3> 

![]({{ page.image1 | relative_url }})

 -------------------------------------------------------------------------------------

## Task 2  : Deploy Your Linux Machine 

<h3 style='color:red'> Qesution 1 : I've logged into the Linux Fundamentals Part 3 machine using SSH and have deployed the AttackBox successfully!</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3> 
 ![]({{ page.image2 | relative_url }})
 ------------------------------------------------------------------------------------------------

 ## Task 3  : Terminal Text Editors 

<h3 style='color:red'> Qesution 1 : Create a file using Nano</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3>

To Create file using nano   
just type nano and the file name you want create      
same like   
nano tryhackme 
 
<h3 style='color:red'> Qesution 2 : Edit "task3" located in "tryhackme"'s home directory using Nano. What is the flag?</h3>
<h3 style='color:green'> Correct Answer  : THM{TEXT_EDITORS}  </h3>
ls 
nano task3
THM{TEXT_EDITORS}

________________________________________________________________________________________________________________________________________

## Task 4 :  General/Useful Utilities 

<h3 style='color:red'> Qesution 1 : Ensure you are connected to the deployed instance (10.10.79.225)</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3>
 
<h3 style='color:red'> Qesution 2 : Now, use Python 3's "HTTPServer" module to start a web server in the home directory of the "tryhackme" user on the deployed instance.</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3>


<h3 style='color:red'> Qesution 3 : Download the file http://10.10.79.225:8000/.flag.txt onto the TryHackMe AttackBox

What are the contents?
</h3>
<h3 style='color:green'> Correct Answer  :THM{WGET_WEBSERVER}  </h3>


![]({{ page.image3 | relative_url }})

<h3 style='color:red'> Qesution 4 : Create and download files to further apply your learning -- see how you can read the documentation on Python3's "HTTPServer"module. 

Use Ctrl + C to stop the Python3 HTTPServer module once you are finished.
.</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3>

-----------------------------------------------------------------------------------------


## Task 5 : Processes 101

<h3 style='color:red'> Qesution 1 : Read me!</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3>
 
<h3 style='color:red'> Qesution 2 : If we were to launch a process where the previous ID was "300", what would the ID of this new process be?</h3>
<h3 style='color:green'> Correct Answer  : 301  </h3>
 
<h3 style='color:red'> Qesution 3 : If we wanted to cleanly kill a process, what signal would we send it ?</h3>
<h3 style='color:green'> Correct Answer  : SIGTERM </h3>
SIGTERM - Kill the process, but allow it to do some cleanup tasks beforehand
![]({{ page.image4 | relative_url }})

<h3 style='color:red'> Qesution 4 : Locate the process that is running on the deployed instance (10.10.79.225). What flag is given?</h3>
<h3 style='color:green'> Correct Answer  : THM{PROCESSES}  </h3>
ps -uax | grep THM
![]({{ page.image5 | relative_url }})
<h3 style='color:red'> Qesution 5 : What command would we use to stop the service "myservice"?</h3>
<h3 style='color:green'> Correct Answer  : systemctl stop myservice  </h3>
 
to stop service type
systemcty stop 'service name'

![]({{ page.image6 | relative_url }})

<h3 style='color:red'> Qesution 6 : What command would we use to start the same service on the boot-up of the system?</h3>
<h3 style='color:green'> Correct Answer  : systemctl enable myservice  </h3>
to enable service command is 
systemctl enable 'service name'
 
<h3 style='color:red'> Qesution 7 : What command would we use to bring a previously backgrounded process back to the foreground?</h3>
<h3 style='color:green'> Correct Answer  : fg </h3>
fg to make process in background

------------------------------------------------------------------------------------------------------

## Task 6 : Maintaining Your System: Automation 

<h3 style='color:red'> Qesution 1 : Ensure you are connected to the deployed instance and look at the running crontabs.</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3>

<h3 style='color:red'> Qesution 2 : What command would we use to bring a previously backgrounded process back to the foreground?</h3>
<h3 style='color:green'> Correct Answer  : @reboot</h3>
@reboot command allowed to use command every reboot the machine same like 
@reboot macchanger -r wlan0   
this command make you change your mac address every reboot

____________________________________________________________________

## Task 7 : Maintaining Your System: Package Management 

<h3 style='color:red'> Qesution 2 : Since TryHackMe instances do not have an internet connection...this task only requires you to read through the material.</h3>
<h3 style='color:green'> Correct Answer  : No answer needed </h3>

-----------------------------------------------------------------------------------------

## Task 8 : Maintaining Your System: Logs 

<h3 style='color:red'> Qesution 1 : Look for the apache2 logs on the deployable Linux machine</h3>
<h3 style='color:green'> Correct Answer  : No answer needed </h3>

<h3 style='color:red'> Qesution 2 : What is the IP address of the user who visited the site? </h3>
<h3 style='color:green'> Correct Answer  : 10.9.232.111 </h3>

<h3 style='color:red'> Qesution 3 : What file did they access? </h3>
<h3 style='color:green'> Correct Answer  : catsanddogs.jpg </h3>

--------------------------------------------------------------------------

## Task 9 : Conclusions & Summaries 

<h3 style='color:red'> Qesution 1 : Terminate the machine deployed in this room from task 2.  </h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3>



<h3 style='color:red'> Qesution 2 : Continue your learning in other Linux-dedicated rooms</h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3>

------------------------------------------------------------------------------------

## The End 


