# README
This repo contains some interesting stuff including tools, cheatsheets, articles that can be useful for penetration testing or smth.

### Tools

#### Information Gathering
* [theHarvester](http://tools.kali.org/information-gathering/theharvester) - tool used to gather emails, subdomains, hosts, employee names, open ports and banners from different public sources like search engines, PGP key servers and SHODAN computer database.
* [fierce](http://tools.kali.org/information-gathering/fierce) - a reconnaissance tool. Fierce is a PERL script that quickly scans domains (usually in just a few minutes, assuming no network lag) using several tactics.
* [nikto](https://tools.kali.org/information-gathering/nikto) - one more web application scanner (installed in Kali)
* [skipfish](http://tools.kali.org/web-applications/skipfish) - an active web application security reconnaissance tool.
* [dnsmap](http://tools.kali.org/information-gathering/dnsmap) - sub-domain enumeration tool.
* [searchsploit](http://tools.kali.org/information-gathering/exploitdb) - utility to search the Exploit Database archive.
* [dnsenum](http://tools.kali.org/information-gathering/dnsenum) - script to enumerate DNS information.
* [DNSRecon](http://tools.kali.org/information-gathering/dnsrecon) - one more DNS enumeration script.
* [enum4linux](http://tools.kali.org/information-gathering/enum4linux) - tool for enumerating data from Windows and Samba hosts.
* [BlindElephant.py](http://tools.kali.org/web-applications/blindelephant) - tool for web application fingerprinting
* [myip.ms](https://myip.ms/) - whois lookup with OS and Browser fingerprint
* **Metasploit** modules:
   * [auxiliary/scanner/netbios/nbname](https://www.offensive-security.com/metasploit-unleashed/scanner-netbios-auxiliary-modules/) - to enumerate host name

#### Exploitation
* **rinetd** - Port forwarding tool
```
Usage: /etc/rinetd.conf
change bind address, bind port, connect address, connect port, than restart as a service (/etc/init.d/rinetd restart)
```

* **Web server default log directories for log poisoning and LFI**
```
/etc/httpd/logs/access_log - Apache/2.4.6 (CentOS)
/etc/httpd/logs/error_log - Apache/2.4.6 (CentOS)
```
* **Metasploit modules/payloads:**
```
exploit/multi/handler - module that can accept various incoming payloads
linux/x86/shell/reverse_tcp - STAGED reverse tcp shell for Linux
linux/x86/shell_reverse_tcp - NON-STAGED reverse tcp shell for Linux
windows/meterpreter/reverse_https - meterpreter that looks like https traffic
```

#### Post Exploitation
* **Metasploit modules/payloads:**
```
post/windows/gather/credentials/gpp - Windows Gather Group Policy Preference Saved Passwords
```

#### Password attacks
* pwdump - Windows utility that exposes the LM and NTLM password hashes of local user accounts from the Security Account Manager (SAM)
[Download](https://www.dropbox.com/s/ixs1ac0xgl245ea/pwdump.zip?dl=0) //
[Wiki](https://en.wikipedia.org/wiki/Pwdump)
* WCE (Windows Credential Editor) - security tool that allows one to perform several attacks to obtain clear text passwords and hashes from a compromised Windows host.
[Download](https://www.dropbox.com/s/lncton1vtm3fwzp/wce_v1_3beta.zip?dl=0)
* mimikatz - tool to extract plaintext passwords, hashes, pin codes and kerberos tickets. [Download](https://github.com/gentilkiwi/mimikatz/releases/)
```
mimikatz # privilege::debug
mimikatz # sekurlsa::logonpasswords
```

* Hob0Rules - Password cracking rules for Hashcat based on statistics and industry patterns. [Download](https://github.com/praetorian-inc/Hob0Rules)

#### Password Lists
* Passwords from Russian resources (collected by @simonuvarov)
[Download](https://github.com/simonuvarov/password-lists)

#### Utilities
* Plink - console SSH client for Windows.
[Download](https://www.dropbox.com/s/g42q3pkrlioym75/plink.exe?dl=0)

#### Articles
* Basic Linux privilege escalation.
[Read](https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/)
* Windows Privilege Escalation Fundamentals
[Read](http://www.fuzzysecurity.com/tutorials/16.html)
* MSSQLi Cheatsheet
[Read](https://www.exploit-db.com/papers/12975/)
* Pentest Tips and Tricks, 1
[Read](https://jivoi.github.io/2015/07/01/pentest-tips-and-tricks/)
* Pentest Tips and Tricks, 2
[Read](https://jivoi.github.io/2015/08/21/pentest-tips-and-tricks-number-2/)
* Pentest Bookmarks 
[Read](https://code.google.com/archive/p/pentest-bookmarks/wikis/BookmarksList.wiki)
* Introductory Intel x86
[Read](http://opensecuritytraining.info/IntroX86.html)
* Buffer Overflow Reddit Tutorial
[Read](https://www.reddit.com/r/hacking/comments/1wy610/exploit_tutorial_buffer_overflow/)
* Corelan Exploit Writing Tutorial
[Read](https://www.corelan.be/index.php/2009/07/19/exploit-writing-tutorial-part-1-stack-based-overflows/)
* Introduction to Software Exploits
[Read](http://opensecuritytraining.info/Exploits1.html)

#### Labs
* [Exploit-Exercises](https://exploit-exercises.com/) - a variety of virtual machines for learning different computer security issues such as privilege escalation, vulnerability analysis, exploit development, debugging, reverse engineering, and general cyber security issues.
* [Metasploitable](https://sourceforge.net/projects/metasploitable/files/Metasploitable2/) - an intentionally vulnerable Linux virtual machine. This VM can be used to conduct security training, test security tools, and practice common penetration testing techniques. 
* [Protostar](https://exploit-exercises.com/protostar/) - Protostar introduces the following in a friendly way:
Network programming, Byte order, Handling sockets, Stack overflows, Format strings, Heap overflows.
* [Narnia](http://overthewire.org/wargames/narnia) - lab accessed by SSH

#### Online Services
* [TempMail](https://temp-mail.ru/) - interesting service for creating temporary email for registration during penetration testing
* [RecieveFreeSMS](http://receivefreesms.com/) - service for receiving SMS during penetration testing
* [Privatoria](https://privatoria.net) - service with out-of-box VPN+TOR (3.9$ per month)
* [Censys](https://censys.io/) - free Shodan analog

