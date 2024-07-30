# Free Cyber-Resources

## Learning Resource
---
1. YouTube Channels
	- [The Cyber Mentor](https://www.youtube.com/@TCMSecurityAcademy)
	- [InfoSec Pat](https://www.youtube.com/@InfoSecPat)
	- [Spot Technologies](https://www.youtube.com/@spottechnologies)
	- [Tyler Ramsbey](https://www.youtube.com/@TylerRamsbey)
	- [Derron C](https://www.youtube.com/@derronc)
	- [Ryan John](https://www.youtube.com/@ryan_phdsec)
	- [Rana Khalil](https://www.youtube.com/@RanaKhalil101)
	- [HackerSploit](https://www.youtube.com/@HackerSploit)
	- [IppSec](https://www.youtube.com/@ippsec)
	- [Hank Hackerson](https://www.youtube.com/@HankHacksHackers)
	
2. Websites
	* [TryHackMe](https://tryhackme.com/)
	* [HackTheBox](https://hackthebox.com/)
	* [WebSploit](https://websploit.org)

3. Github repos
   	* [The-Art-of-Hacking](https://github.com/The-Art-of-Hacking/h4cker)
   	  

## Practicing labs
---
1. Labs that can be installed on **Kali** and **Parrot os**
	- [OWASP Juice-shop](https://github.com/juice-shop/juice-shop)
	- [WebSploit Labs](https://websploit.org/)

2. Web labs
	- [PentesterLab](https://pentesterlab.com/)
	- [PortSwigger](https://portswigger.net/web-security)
	- [OverTheWire](https://overthewire.org/wargames/)

---

# intentionally vulnerable containers

**After you have installed Kali Linux or Parrot OS in a VM, run the following command from a
terminal window (inside of the VM) to setup your environment:**
```
curl -sSL https://websploit.org/install.sh | sudo bash
```
This command will install all the tools, Docker, the intentionally vulnerable containers, and
numerous cybersecurity resources.

when the script is done installing

**Move to the /usr/local/bin/** folder and create a file using
```
sudo nano containers2
``` 

**Paste this stript**

```
#!/bin/bash
# Author: Omar Santos @santosomar
# Lame script to display the running containers in WebSploit

clear
echo -e "\n\e[96mWebSploit\e[39m"
echo -e "by Omar Santos @santosomar"
echo -e "-------------------------------------"
echo -e "Internal Hacking Networks: 10.6.6.0/24 and 10.7.7.0/24"
echo -e "Your bridge networks:"
ip -c -brie a | grep 10.6.6.1
ip -c -brie a | grep 10.7.7.1

echo -e "
The following are the WebSploit vulnerable containers and associated IP addresses and ports.
+------------------------+--------------------+
|     Container          | IP Address & ports |
+------------------------+--------------------+
| webgoat                |  10.6.6.11:8080    |
| juice-shop             |  10.6.6.12:3000    |
| dvwa                   |  10.6.6.13:80      |
| mutillidae_2           |  10.6.6.14:80,3306 |
| dvna                   |  10.6.6.15:        |
| hackazon               |  10.6.6.16:80      |
| hackme-rtov            |  10.6.6.17:80      |
| mayhem                 |  10.6.6.18:22,80   |
| rtv-safemode           |  10.6.6.19:80      |
| galactic-archives      |  10.6.6.20:5000    |
| yascon-hackme          |  10.6.6.21:80      |
| secretcorp-branch1     |  10.6.6.22:80      |
| gravemind              |  10.6.6.23:        |
| dc30_01                |  10.6.6.24:22,3000 |
| dc30_01                |  10.6.6.25:        |
| y-wing                 |  10.6.6.26:3000    |
| dc31_01                |  10.7.7.21:22      |
| dc31_02                |  10.7.7.22:8888    |
| dc31_03                |  10.7.7.23:9090    |
+------------------------+--------------------+ "

echo -e "The following are the \e[92mrunning \e[39mcontainers with their associated ports:"
docker ps --format "table {{.Names}}\t{{.Ports}}\t{{.Status}}"

```

after that you must change the file permissions using
```
sudo chmod +x containers2
```
go to home and type
```
containers2
```
this will list all the containers with their addresses and ports they run on
like this

![image](https://github.com/AmweCodex/Cyber-Resources/assets/134791541/a3daf5d1-8ccd-41a2-ad46-27258f13d8f5)

