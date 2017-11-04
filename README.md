# MHN-Honeypots
> Three different honeypots were setup using Google Cloud Virtual Machines: Dionaea, Cowrie, Elastichoney. A total of 9253 attacks were recorded from various countries. 

<img src="https://github.com/seaunderwater/MHN-Honeypots/blob/master/attack_summary.png" />


## Dionaea
* Dionaea is intended to trap malware by exposing a variety of services offered by a network including SIP, FTP, MYSQL, and SMB. My Dionaea instance loggged 9244 connection attempts from countries all over the world. 

### Issues 
* I was unable to capture any malware samples. In fact, upon performing a google search, a lot of users reported that the Dionaea honeypot does not capture any malware samples when used as part of the Modern Honeypot Network. Many users reported capturing malware when setting up instances of Dionaea separate from the Modern Honeypot Network. 
https://github.com/threatstream/mhn/issues/417

* I even tried attack Dionaea myself using various nmap and metasploit modules, but Dionaea did not record any binaries. 
  - https://nmap.org/nsedoc/scripts/smb-vuln-cve-2017-7494.html
  - https://github.com/rapid7/metasploit-framework/blob/master/modules/exploits/windows/smb/ms10_061_spoolss.rb


## Cowrie
* Cowrie is a medium interaction SSH and Telnet honeypot designed to log brute force attacks and the shell interaction performed by the attacker. Cowrie includes a full fake filesystem. 

* Unfortunately I did not catch any traffic attempting to brute force Cowrie. 

## Elastichoney
* Elasticsearch has become an extremely popular search and analytics engine over the last few years. I thought it would be really neat to setup a honeypot to catch attackers attempting to attack an elastic instance. 

* Elastichoney takes requests on the /, /_search, and /_nodes endpoints and returns a JSON response that is identical to a vulnerable ES. 

* I was only able to capture 9 instances of attempted connections to the honeypot. 

<img src="https://github.com/seaunderwater/MHN-Honeypots/blob/master/elastichoney.png" />

## Overall Issues

* After several days of capturing traffic, my mhn-admin vm suddenly went offlne. I kept getting a 504 gateway timeout and never got it to work again. Thankfully, I was able to make a snapshot of the original vm's persistent disk and deploy another mh-admin vm. 



