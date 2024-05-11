# Note : This room does not exist on this module , but these exercises are related with this topic. 

## Link on TryHackMe : [Crack the hash](https://tryhackme.com/r/room/crackthehash)

### Task - 1 : Level one

### Can you complete the level 1 tasks by cracking the hashes?

**Q: 48bb6e862e54f2a795ffc4e541caed4d**

Answer: easy

solution: firstly identify the type of hash (format) and then crack with john or hashcat. 
**[More Details on this rep ](https://github.com/imahmedmunir/Complete-Beginner-TryHackMe/tree/main/Cryptography/John%20the%20Ripper)**

**Q: CBFDAC6008F9CAB4083784CBD1874F76618D2A97**

Answer: password123 

command : john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt

**Q: 1C8BFE8F801D79745C4631D09FFF36C82AA37FC4CCE4FC946683D7B336B63032**

Answer: letmein

Command : john --format=Raw-SHA256 --wordlist=/usr/share/wordlists/rockyou.txt hash.txt

**Q: $2y$12$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom**

Answer: bleh 

Command : hashcat -m 3200 hash.txt /usr/share/wordlists/rockyou.txt

**Q: 279412f945939ba78ce0758d3fd83daa**

Answer; Eternity22

## Task -2 : Level two 

**Q: F09EDCB1FCEFC6DFB23DC3505A882655FF77375ED8AA2D1C13F640FCCC2D0C85**

Answer: paule

john --wordlist=/usr/share/wordlists/rockyou.txt --format=raw-sha256  hash.txt

**Q: 1DFECA0C002AE40B8619ECF94819CC1B**

Answer: n63umy8lkf4i


command: john --wordlist=/usr/share/wordlists/rockyou.txt --format=nt  hash.txt

**Q: $6$aReallyHardSalt$6WKUTqzq.UQQmrm0p/T7MPpMbGNnzXPMAXi4bJMl9be.cfi3/qxIf.hsGpS41BqMhSrHVXgMpdjS6xeKZAs02.**

Answer: waka99

Hint: ignore the salt , it is already embedded in question

**Q: e5d8870e5bdd26602cab8dbe07a942c8669e56d6:tryhackme**

Answer: 481616481616

Hint: Add the salt at last and use the code 160 if you're doing it with hashcat as following:
hashcat -m 160 "e5d8870e5bdd26602cab8dbe07a942c8669e56d6:tryhackme" /usr/share/wordlists/rockyou.txt
