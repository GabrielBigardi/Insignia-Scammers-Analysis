# Insignia Scammers App Analysis

# Insignia_Beta.exe file  
## Basic Analysis  
Open ups a CMD with a message "Starting Game"  
Open a connection to the website "www.ipconfig.to" everytime you open it, probably doing some API call to get data about your IP address.  
Don't make any other connections, found no others TCP/UDP/SOCKET connections going on.  
  
## DLLs being used  
* I don't know if it's for faking purposes or is it actually being used  
  
GfnRuntimeSdk.dll  
icui18n.dll  
icuuc.dll  
libavcodec-58.dll  
libavformat-58.dll  
libavresample-4.dll  
libavutil-56.dll  
libswscale-5.dll  
  
## Detected Virus Type  
### Hybrid Analysis  
TR/Redcap.gwfdf  
  
### DrWeb  
Trojan.PWS.Discord.287  
A Trojan-PWS is very similar to a Trojan-Spy, but is geared mainly towards stealing account log-in details, including passwords (the PWS stands for password stealer). In addition, some Trojan-PWSs may also include spying and data-stealing routines.  
  
### Kaspersky  
UDS:Trojan-PSW.Win32.Disco.Inu  
  
### AVG/ Avast  
Win64:Malware-gen  
  
## PE Deep Analysis  
### Mine  
application/x-dosexec  
  
### PE Rich Header  
Visual Studio 2015 - 14.0  
  
### Debug Path  
"C:\Users\admin\.nexe\16.7.0\out\Release\node.pdb"  
  
### Version  
CompanyName: ACME Corp  
ProductName: GameSetup  
File Description: Game build with Unity  
Legal Copyright: Copyright - Unity Games 2022  
Original File Name: default.exe  
  
### Interesting Strings  
\RPC Control\ConsoleLPC-0x0000000000000ACC--19088472741253897169-1469468468507862506-721687533740726435-19133884371930542178  
\Sessions\1\Windows\ApiPort  
  
## Found Websites related to  
### 100% sure it's their domain  
superfuniestindianparty.rip (185.174.136.147)  
  
### Unknown ips related to (may be discord servers or other things)  
162.159.136.232  
172.217.162.206  
162.159.138.232  
162.159.133.232  
104.16.168.131  
  
## superfuniestindianparty.rip whois  
Name: OpenTLD B.V. (freenom)  
Whois Server: whois.opentld.com  
Referral URL: http://www.opentld.com  
Expires On: 2023-01-28  
Registered On: 2022-01-28  
Updated On: 2022-02-02  
  
## superfuniestindianparty.rip nameservers  
ns01.freenom.com 54.171.131.39  
ns02.freenom.com 52.19.156.76  
ns03.freenom.com 104.155.27.112  
ns04.freenom.com 104.155.29.241  
  
## Summary  
They are using the node.js to code the Discord Token Stealer and the framework "nexe" to convert a simple node app to .exe.  
This app first check if there's any Discord in your registry, it won't send any requests if you don't have it installed, if you have Discord installed it will send your Discord Token (immutable) to the domain superfuniestindianparty.rip.  
They are using Visual Studio 2015 - 14.0.  
Their working directory is "C:\Users\admin\.nexe\16.7.0\out\", user named "admin", probably on some virtual machine.  
The file doesn't seems to persist or have any kind of keylogger into it.  
They are using Freenom to have a free domain and also using freenom nameservers.  
