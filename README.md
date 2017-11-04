# MHN-Honeypots
> Three different honeypots were setup using Google Cloud Virtual Machines: Dionaea, Cowrie, Elastichoney. 

## Dionaea
* Dionaea is intended to trap malware by exposing a variety of services offered by a network including SIP, FTP, MYSQL, and SMB. My Dionaea instance loggged 9244 connection attempts from countries all over the world. 

### Issues 
* I was unable to capture any malware samples. In fact, upon performing a google search, a lot of users reported that the Dionaea honeypot does not capture any malware samples when used as part of the Modern Honeypot Network. Many users reported capturing malware when setting up instances of Dionaea separate from the Modern Honeypot Network. 
https://github.com/threatstream/mhn/issues/417

* I even tried attack Dionaea myself using various metasploit modules, but Dionaea did not record any binaries. 

## Cowrie
## Elastichoney

