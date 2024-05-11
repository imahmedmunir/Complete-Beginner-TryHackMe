## Task - 5 :  Cracking Windows Authentication Hashes

### What do we need to set the "format" flag to, in order to crack this?
Answer: nt

## What is the cracked value of this password?
Answer: mushroom

Command : john --format=nt --wordlsit=/usr/share/wordlist/rockyou.txt hash.txt

## Task - 6 : Cracking /etc/shadow Hashes 

### What is the root password?
Answer: 1234

Command : john --wordlist=/usr/share/wordlists/rockyou.txt  unshadowed.txt

## Task - 7: Single Crack Mode

### What is Joker's password?
Answer: Jok3r

solution: before cracking hash add the user name before hash of passwrod with colon ":" separating it.
like it's asked joker so, joker:here goes hash
Find type of hash 

command : john --single --format=hashtype  file.txt

## Task - 8 : Custom Rules

### What do custom rules allow us to exploit?
Anser: password complexity predicability

### What rule would we use to add all capital letters to the end of the word?
Answer: az"[A-Z]"

### What flag would we use to call a custom rule called "THMRules"
Answer: --rule=THMRules

