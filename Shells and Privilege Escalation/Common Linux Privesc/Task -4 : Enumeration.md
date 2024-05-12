# Link On TryHackMe: [Common Linux Privesc](https://tryhackme.com/r/room/commonlinuxprivesc)


## Task - 4: Enumeration 

**Firstly connect with target machine ssh user3@IP and enter password**

**Q: What is the target's hostname?**

Answer: polobox

Hint: After connecting you can see the hostname user3@polobox

**Q: Look at the output of /etc/passwd how many "user[x]" are there on the system?**

Answer: 8

Hint: cat /etc/passwd

**Q: How many available shells are there on the system?**

Anser: 4

Hint: cat /etc/shells

**Q: What is the name of the bash script that is set to run every 5 minutes by cron?**

Answer: autoscript.sh 

Hint : change to user4 and ls on desktop

**Q: What critical file has had its permissions changed to allow some users to write to it?**

Answer: /etc/passwd

Hint: ls -la /etc/passwd

