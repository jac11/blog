---
layout: post
image: /assets/images/EncryptionCrypto101.png
image1: /assets/images/crypto/1.png
image2: /assets/images/crypto/2.png
image3: /assets/images/crypto/3.png
image4: /assets/images/crypto/4.png
image5: /assets/images/crypto/5.png
image6: /assets/images/crypto/6.png
image7: /assets/images/crypto/7.png
image8: /assets/images/crypto/8.png
image9: /assets/images/crypto/9.png
image10: /assets/images/crypto/10.png
image11: /assets/images/crypto/11.png
image12: /assets/images/crypto/12.png
categories: TryHackMe
---
# *Welcome To the Encryption crypto tryhackme room 'writeup'*
* <p style='color:red'>  by : Ahmedhammad </p>
```
```
## --info 

******
* room name : Encryption-Crypto101
* category : Crypto 
* link :
[https://www.tryhackme.com/room/encryptioncrypto101](https://www.tryhackme.com/room/encryptioncrypto101)

## This room will cover:
* Why cryptography matters for security and CTFs
* The two main classes of cryptography and their uses
* RSA, and some of the uses of RSA
* 2 methods of Key Exchange

```
```
<h2 style='color:blue'>  Starting Point </h2>
_______________________________________________
## task1
<h3 style='color:red'> Qesution 1 : I'm ready to learn about encryption ? </h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3> 
________________________________________________
## task2
<h3 style='color:red'> Qesution 2 : I agree not to complain too much about how theory heavy this room is ? </h3>
<h3 style='color:green'> Correct Answer  : No answer needed  </h3> 
<h3 style='color:red'> Qesution 3 : Are SSH keys protected with a passphrase or a password ?</h3>
<h3 style='color:green'> Correct Answer  :  passphrase </h3> 
![]({{ page.image1 | relative_url }})

------------------------------------------------------------------

## task3
<h3 style='color:red'> Qesution 4 : What does SSH stand for?  ? </h3>
<h3 style='color:green'> Correct Answer  : Secure Shell </h3> 
<h3 style='color:red'> Qesution 5 :How do webservers prove their identity ?</h3>
<h3 style='color:green'> Correct Answer  : certificates </h3> 
![]({{ page.image2 | relative_url }})
<h3 style='color:red'> Qesution 6 : What is the main set of standards you need to comply with if you store or process payment card details ?</h3>
<h3 style='color:green'> Correct Answer  : PCI-DSS </h3> 
![]({{ page.image3 | relative_url }})

----------------------------------------------------------------------
## task4
<h3 style='color:red'> Qesution 7 : What's 30 % 5 ? </h3>
<h3 style='color:green'> Correct Answer  : 0 </h3> 
<h3 style='color:red'> Qesution 8 : What's 25 % 7 ?</h3>
<h3 style='color:green'> Correct Answer  : 4 </h3> 
<h3 style='color:red'> Qesution 9 : What's 118613842 % 9091 ?</h3>
<h3 style='color:green'> Correct Answer  : 3565 </h3> 
will use python as the Hint
![]({{ page.image4 | relative_url }})

-----------------------------------------------------------------------
## task5
<h3 style='color:red'> Qesution 10 : Should you trust DES? Yea/Nay ? </h3>
<h3 style='color:green'> Correct Answer  : Nay </h3> 
![]({{ page.image5 | relative_url }})
<h3 style='color:red'> Qesution 11 : What was the result of the attempt to make DES more secure so that it could be used for longer ?</h3>
<h3 style='color:green'> Correct Answer  : Triple DES </h3> 
![]({{ page.image6 | relative_url }})
<h3 style='color:red'> Qesution 12 : Is it ok to share your public key? Yea/Nay ?</h3>
<h3 style='color:green'> Correct Answer  : Yea </h3> 
you only need to share public key and private key shoud kept as private
![]({{ page.image7 | relative_url }})

-----------------------------------------------------------------------

## task6
<h3 style='color:red'> Qesution 13 :  p = 4391, q = 6659. What is n  ? </h3>
<h3 style='color:green'> Correct Answer  :  29239669 </h3> 
![]({{ page.image8 | relative_url }})

as we can see if you know p and q so n = p*q 
so i will gonna use pyhton to calculated 

![]({{ page.image9 | relative_url }})

<h3 style='color:red'> Qesution 14 : understand enough about RSA to move on, and I know where to look to learn more if I want to. </h3>
<h3 style='color:green'> Correct Answer  : no answer needed </h3> 

-----------------------------------------------------------------------

## task7 
<h3 style='color:red'> Qesution 15 : I understand how keys can be established using Public Key (asymmetric) cryptography . </h3>
<h3 style='color:green'> Correct Answer  :  no answer needed </h3> 

----------------------------------------------------------------------------

## task 8
<h3 style='color:red'> Qesution 16 : I understand how keys can be established using Public Key (asymmetric) cryptography . </h3>
<h3 style='color:green'> Correct Answer  :  CloudFlare </h3> 
![]({{ page.image10 | relative_url }})

---------------------------------------------------------------------------------

## task9 
<h3 style='color:red'> Qesution 17: I recommend giving this a go yourself. Deploy a VM, like Linux Fundamentals 2 and try to add an SSH key and log in with private key. </h3>
<h3 style='color:green'> Correct Answer  :  no answer needed  </h3> 
<h3 style='color:red'> Qesution 18 : Download the SSH Private Key attached to this room. </h3>
<h3 style='color:green'> Correct Answer  : no answer needed</h3> 
<h3 style='color:red'> Qesution 19 : What algorithm does the key use ?  </h3>
<h3 style='color:green'> Correct Answer  :  rsa </h3> 
the answer is the file name you downloaded 'idrsa.id_rsa' as we know about the algoritm ssh use is ' Rivest–Shamir–Adleman ' cryptosystem 
<h3 style='color:red'> Qesution 20 : Crack the password with John The Ripper and rockyou, what's the passphrase for the key ? </h3>
<h3 style='color:green'> Correct Answer  :  delicious </h3> 
first of all to crack the password from the ras file we need to use ssh2jonh.py 
this tools come with john the Ripper the path is /usr/share/jonh/ssh2jonh.py  
the command 
/usr/share/john/ssh2john.py idrsa.id_rsa > idrsa.id.txt        
redirect output to file.txt
then use john the Ripper to crack the password in side the file txt            
john --wordlist=/usr/share/wordlists/rockyou.txt idrsa.id.txt        
the password is : delicious  

![]({{ page.image11 | relative_url }})

---------------------------------------------------------------------------------------

## task 10

<h3 style='color:red'> Qesution 21 : I understand how Diffie Hellman Key Exchange works at a basic level. </h3>
<h3 style='color:green'> Correct Answer  : no answer needed</h3> 

--------------------------------------------------------------------------------------

## task 11 

<h3 style='color:red'> Qesution 22 : Time to try some GPG. Download the archive attached and extract it somewhere sensible. </h3>
<h3 style='color:green'> Correct Answer  : no answer needed</h3> 
<h3 style='color:red'> Qesution 23 : You have the private key, and a file encrypted with the public key. Decrypt the file. What's the secret word ?  </h3>
<h3 style='color:green'> Correct Answer  :  Pineapple </h3> 

* unzip the file use unzip gpg.zip   
* now we have the key and the message
 1. the tryhackme.key
 2. message is message.gpg  
* try to import the key by using
*  sudo gpg --import tryhackme.key  
* use gpg -d message.gpg 
* The secret word is Pineapple

![]({{ page.image12 | relative_url }})

--------------------------------------------------------------------------
## task 12

<h3 style='color:red'> Qesution 22 : I understand that quantum computers affect the future of encryption. I know where to look if I want to learn more. </h3>
<h3 style='color:green'> Correct Answer  : no answer needed</h3> 

--------------------------------------------------------------------------

## the End 
 

