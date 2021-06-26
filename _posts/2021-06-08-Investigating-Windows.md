---
layout: post
image: /assets/images/InvestigatingWindows.png
image1: /assets/images/Windows/1.png
image2: /assets/images/Windows/2.png
image3: /assets/images/Windows/3.png
image4: /assets/images/Windows/4.png
image5: /assets/images/Windows/5.png
image6: /assets/images/Windows/6.png
image7: /assets/images/Windows/7.png
image8: /assets/images/Windows/8.png
image9: /assets/images/Windows/9.png
image10: /assets/images/Windows/10.png
image11: /assets/images/Windows/11.png
image12: /assets/images/Windows/12.png
image13: /assets/images/Windows/13.png
image14: /assets/images/Windows/14.png
image15: /assets/images/Windows/15.png
image16: /assets/images/Windows/16.png
image17: /assets/images/Windows/17.png
image18: /assets/images/Windows/18.png
image20: /assets/images/Windows/20.png
categories: TryHackMe
---
# *Welcome To  Investigating Windows 'writeup'*
* <p style='color:red'>  by : Ahmedhammad </p>
```
```
## --info 

******
* room name : Investigating Windows
* category  : Windows Forensics   
* Link : 
[https://tryhackme.com/room/investigatingwindows](https://tryhackme.com/room/investigatingwindows)

* This is a challenge that is exactly what is says on the tin, there are a few challenges around investigating a windows machine that has been previously compromised.

```
```
<h2 style='color:blue'>  Starting Point </h2>

----------------------------------------------


Task 1  : Investigating Windows 

<h3 style='color:red'> Qesution 1 : Whats the version and year of the windows machine ?</h3>
<h3 style='color:green'> Correct Answer  : Windows Server 2016  </h3> 

*  So many ways to know about the OS info  
I going  to use Powershell Command and do  pipe and grep same like Linux by use  Select-String Module, to get the result easy way
 <p style='color:white'>  * system info | Select-String windows </p>
![]({{ page.image1 | relative_url }})

----------------------------------------------------------------------------


<h3 style='color:red'> Qesution 2 : Which user logged in last ?</h3>
<h3 style='color:green'> Correct Answer  : Administrator  </h3> 
I am  login as Administrtor so last login Administrator  
<p style='color:white'>  net user administrator  | findstr /B /C:"last logon"</p>
![]({{ page.image2 | relative_url }})
 
 ---------------------------------------------------------------------------

<h3 style='color:red'> Qesution 3 : When did John log onto the system last?
Answer format: MM/DD/YYYY H:MM:SS AM/PM </h3>
<h3 style='color:green'> Correct Answer  : 03/02/2019 5:48:32 PM  </h3> 
* I going to  use same command but change the user name to john :
<p style='color:white'>  net user john | findstr /B /C:"last logon"</p>

![]({{ page.image3 | relative_url }})

----------------------------------------------------------------------------

<h3 style='color:red'> Qesution 4 : What IP does the system connect to when it first starts?</h3>
<h3 style='color:green'> Correct Answer  : 10.34.2.3  </h3> 
When the machine boots up, the IP address popup in the cmd window. another way the IP address  store in the register key run  
it  makes the connection established every reboot   
so,  
I am going to check the register key   
open cmd type  regedit   
navigate to the   
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run  


![]({{ page.image4 | relative_url }})

-------------------------------------------------------------------------------------

<h3 style='color:red'> Qesution 5 : What two accounts had administrative privileges (other than the Administrator user)?
Answer format: username1, username2
</h3>
<h3 style='color:green'> Correct Answer  : Jenny, Guest </h3> 
by Powershell, I use the module Get-LocalGroupName to allow me to list administrator group  
Get-LocalGroupName  -Name administrators

![]({{ page.image5 | relative_url }})

-------------------------------------------------------------------------------------


<h3 style='color:red'> Qesution 6 : Whats the name of the scheduled task that is malicous.</h3>
<h3 style='color:green'> Correct Answer  :  Clean file system</h3> 
 I will use
  <p><p style='color:yellow'>schtasks /query </p>to list all the tasks and direct the output to file call task.xml at desktop so I can read the tasks  
 after checking all Tasks  I found task call clean file system is malicious task   
 if you Check the action for this Task you will find the PowerShell natcat script   
 so this, not a Normal task</p>  

![]({{ page.image6| relative_url }})

![]({{ page.image7| relative_url }})

-------------------------------------------------------------------


<h3 style='color:red'> Qesution 7 : What file was the task trying to run daily?</h3>
<h3 style='color:green'> Correct Answer  : nc.ps1 </h3> 
as  I read the action of this task, this task  to run the NC PowerShell script
file name nc.ps1

![]({{ page.image8 | relative_url }})

-------------------------------------------------------------------------

<h3 style='color:red'> Qesution 8 : What port did this file listen locally for?</h3>
<h3 style='color:green'> Correct Answer  : 1348  </h3> 

Also, on the action Section, the port it found as an argument  
so the Full command is nc.ps1 -l 1348 
it means the netcat listener at this port for any coming connection  

![]({{ page.image8 | relative_url }})

----------------------------------------------------------------


<h3 style='color:red'> Qesution 9 : When did Jenny last logon? </h3>
<h3 style='color:green'> Correct Answer  : Never  </h3> 

I going to  use same command but change the user name to Jenny :
<p style='color:white'>  net user Jenny | findstr /B /C:"last logon"</p>

![]({{ page.image9 | relative_url }})

-----------------------------------------------------------------------------------

<h3 style='color:red'> Qesution 10 : At what date did the compromise take place?</h3>
<h3 style='color:green'> Correct Answer  : 03/02/2019 </h3> 

 I going to  open the computer management then I will open the task scheduled  
so  all Tasks are list by the time  
so GameOver task is the task run the first-time run on 03/02/2019, And it will run every 5 minutes 
this task will call mim.exe to hashdump the password and add output to file at same dir, the first time run it this first time the machine  get a compromise to take   place  

![]({{ page.image12 | relative_url }})

![]({{ page.image18 | relative_url }})

----------------------------------------------------------------------------------------------------------


<h3 style='color:red'> Qesution 11 : At what time did Windows first assign special privileges to a new logon?
Answer format: MM/DD/YYYY HH:MM:SS AM/PM</h3>
<h3 style='color:green'> Correct Answer  : 03/02/2019 4:04:49 PM  </h3> 
I am going to open Google then I  search for a Specia privileges login id  
so I found a Microsoft page explaining So the numeric id of the Special login is 4672 
so I will filter all security logs, I saw so many task id 4672  
use the hint is 00/00/0000 0:00:49 PM 
so the answer is  
03/02/2019 4:04:49 PM 


![]({{ page.image10 | relative_url }})

![]({{ page.image11 | relative_url }})

<h3 style='color:red'> Qesution 12 : What tool was used to get Windows passwords?</h3>
<h3 style='color:green'> Correct Answer  : Mimikatz  </h3> 

![]({{ page.image20 | relative_url }})


<h3 style='color:red'> Qesution 13 : What was the attackers external control and command servers IP?</h3>
<h3 style='color:green'> Correct Answer  : 76.32.97.132  </h3> 
the host file has the IP address as First DNS, So I will cat host file to see what is the change on it 
so we have some changes on the host file, so 127.0.0.1 is the loopback localhost, and another IP  added by hacker tool so
he adds for google.com 76.32.97.132, so any time to go open google will go for this address, not  a google IP 
to be suer open terminal and type whois 76.32.97.132 the result no google

![]({{ page.image14 | relative_url }})

![]({{ page.image13 | relative_url }})

----------------------------------------------------------------------------------------------------------------

<h3 style='color:red'> Qesution 14 : What was the extension name of the shell uploaded via the servers website?</h3>
<h3 style='color:green'> Correct Answer  : .jsp  </h3> 
check file inetpub\wwwroot by cat command
the file extension .jsp 
<p style='color:yellow'>javascript</p>
 
![]({{ page.image15 | relative_url }})

----------------------------------------------------------------------------------

<h3 style='color:red'> Qesution 15 : What was the last port the attacker opened?</h3>
<h3 style='color:green'> Correct Answer  : 1337 </h3> 
check the firewall for port allow incoming connection I found 1337 especial port 

![]({{ page.image16 | relative_url }})

-----------------------------------------------------------------------------------------------

<h3 style='color:red'> Qesution 16 : Check for DNS poisoning, what site was targeted? </h3>
<h3 style='color:green'> Correct Answer  : google.com  </h3> 

as the host file  the target is  google.com
 
![]({{ page.image17 | relative_url }})



------------------------------------------------------------------------------------

## The End 



