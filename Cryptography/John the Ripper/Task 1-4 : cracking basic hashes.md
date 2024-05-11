# Link on TryHackMe: [John the Ripper](https://tryhackme.com/r/room/johntheripper0)


## Task-1 is Reading only

## Task -2 : What is the most popular extended version of John the Ripper?
Answer : jumbo john

## Task -3 What website was the rockyou.txt wordlist created from a breach on?
Answer: rockyou.com

## Task -4 : Cracking Basic Hashes

### What type of hash is hash1.txt?
Answer: md5  

Hint: use hash-identifier command on Kali linux or use [online tool](https://hashes.com/en/tools/hash_identifier)

### What is the cracked value of hash1.txt?
Answer: biscuit

solution: on kali linux , use the rockyou.txt wordlist with format of hash as identified as earlier
Hash Identified: MD5

john --format=raw-md5  --wordlist=/usr/share/wordlists/rockyou.txt hash1.txt

### What type of hash is hash2.txt?
Answer: sha1

### What is the cracked value of hash2.txt
Answer: kangeroo

Hint: repeat the same process by identifying hash fomart

### hat type of hash is hash3.txt?
Answer: sha256 

### What is the cracked value of hash3.txt
Answer: microphone

Hint: repeat the process

### What type of hash is hash4.txt?
Answer: whirlpool

### What is the cracked value of hash4.txt
Answer: colossal (don't use raw word this time on command)
