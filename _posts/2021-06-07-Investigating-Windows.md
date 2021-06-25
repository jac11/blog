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

![]({{ page.image1 | relative_url }})


<h3 style='color:red'> Qesution 2 : Which user logged in last ?</h3>
<h3 style='color:green'> Correct Answer  : Administrator  </h3> 

![]({{ page.image2 | relative_url }})


<h3 style='color:red'> Qesution 3 : When did John log onto the system last?
Answer format: MM/DD/YYYY H:MM:SS AM/PM </h3>
<h3 style='color:green'> Correct Answer  : 03/02/2019 5:48:32 PM  </h3> 

![]({{ page.image3 | relative_url }})


<h3 style='color:red'> Qesution 4 : What IP does the system connect to when it first starts?</h3>
<h3 style='color:green'> Correct Answer  : 10.34.2.3  </h3> 

![]({{ page.image4 | relative_url }})

<h3 style='color:red'> Qesution 5 : What two accounts had administrative privileges (other than the Administrator user)?
Answer format: username1, username2
</h3>
<h3 style='color:green'> Correct Answer  : Jenny, Guest </h3> 

![]({{ page.image5 | relative_url }})


<h3 style='color:red'> Qesution 6 : Whats the name of the scheduled task that is malicous.</h3>
<h3 style='color:green'> Correct Answer  :  Clean file system</h3> 

![]({{ page.image6| relative_url }})

![]({{ page.image7| relative_url }})
<h3 style='color:red'> Qesution 7 : What file was the task trying to run daily?</h3>
<h3 style='color:green'> Correct Answer  : nc.ps1 </h3> 

![]({{ page.image8 | relative_url }})

<h3 style='color:red'> Qesution 8 : What port did this file listen locally for?</h3>
<h3 style='color:green'> Correct Answer  : 1348  </h3> 

![]({{ page.image8 | relative_url }})


<h3 style='color:red'> Qesution 9 : When did Jenny last logon? </h3>
<h3 style='color:green'> Correct Answer  : Never  </h3> 

![]({{ page.image9 | relative_url }})


<h3 style='color:red'> Qesution 10 : At what date did the compromise take place?</h3>
<h3 style='color:green'> Correct Answer  : 03/02/2019 </h3> 

![]({{ page.image12 | relative_url }})



<h3 style='color:red'> Qesution 11 : At what time did Windows first assign special privileges to a new logon?
Answer format: MM/DD/YYYY HH:MM:SS AM/PM</h3>
<h3 style='color:green'> Correct Answer  : 03/02/2019 4:04:49 PM  </h3> 

![]({{ page.image10 | relative_url }})

![]({{ page.image11 | relative_url }})

<h3 style='color:red'> Qesution 12 : What tool was used to get Windows passwords?</h3>
<h3 style='color:green'> Correct Answer  : Mimikatz  </h3> 

![]({{ page.image0 | relative_url }})


<h3 style='color:red'> Qesution 13 : What was the attackers external control and command servers IP?</h3>
<h3 style='color:green'> Correct Answer  : 76.32.97.132M  </h3> 

![]({{ page.image14 | relative_url }})


<h3 style='color:red'> Qesution 14 : What was the extension name of the shell uploaded via the servers website?</h3>
<h3 style='color:green'> Correct Answer  : .jsp  </h3> 

![]({{ page.image15 | relative_url }})


<h3 style='color:red'> Qesution 15 : What was the last port the attacker opened?</h3>
<h3 style='color:green'> Correct Answer  : 1337 </h3> 

![]({{ page.image16 | relative_url }})



<h3 style='color:red'> Qesution 16 : Check for DNS poisoning, what site was targeted? </h3>
<h3 style='color:green'> Correct Answer  : google.com  </h3> 

![]({{ page.image17 | relative_url }})



------------------------------------------------------------------------------------

## The End 



