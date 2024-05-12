# Link on TryhackeMe: [Password Attacks](https://tryhackme.com/r/room/passwordattacks)

## This room belongs to red teaming > initial Access > passwrod attacks

## Task -1 : Only Reading

## Task -2 : Password Attacking Techniques

**Q: Which type of password attack is performed locally?**

Answer: password cracking

## Task -3 : Password Profiling #1

**Q: What are the default login credentials (in the format of username:password) for a Juniper Networks ISG 2000 device? Make sure to check the hint.**

Answer: netscreen:netscreen

## Task - 4: Password Profiling #2 

**Q: Run the following crunch command:crunch 2 2 01234abcd -o crunch.txt. How many words did crunch generate?**

Answer: 81 

Command: cewl -w wordlist.txt -d 8 -m 5 https://clinic.thmredteam.com/

**Q: What is the crunch command to generate a list containing THM@% and output to a file named tryhackme.txt?**

Answer: crunch 5 5 -t "THM^" -o tryhackme.txt

## Task - 5: Offline Attacks -

**Q: Considering the following hash: 8d6e34f987851aa599257d3831a1af040886842f. What is the hash type?**

Answer: sha-1

Command:  hash-identifier 8d6e34f987851aa599257d3831a1af040886842f

**Q: Perform a dictionary attack against the following hash: 8d6e34f987851aa599257d3831a1af040886842f. What is the cracked value? Use rockyou.txt wordlist.**

Answer: sunshine

Solution: first save the hash into a file and run this command: hashcat -m 100 hash.txt /usr/share/wordlists/rockyou.txt

**Q: Perform a brute-force attack against the following MD5 hash: e48e13207341b6bffb7fb1622282247b.**
**What is the cracked value? Note the password is a 4 digit number: [0-9][0-9][0-9][0-9]****

Answer: 1337

Command : save the hash into a file and run this command hashcat -m 0 -a 3 -o MD5.txt hash.txt ?d?d?d?d.
It will write the answer in MD5.txt file , read it
