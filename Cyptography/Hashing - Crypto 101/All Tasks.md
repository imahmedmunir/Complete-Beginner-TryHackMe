# Link on TryHackMe : [Hashing-Crypto 101](https://tryhackme.com/r/room/hashingcrypto101)

## Task -1 : key terms

### Is base64 encryption or encoding?
Answer: encoding

## Task -2: what is a hash function

### What is the output size in bytes of the MD5 hash function?
Answer: 16 

### Can you avoid hash collisions? (Yea/Nay)
Answer: Nay

### If you have an 8 bit hash output, how many possible hashes are there?
Answer: 256


## Task-3: Uses of hashing

### Crack the hash "d0199f51d2728db6011945145a1b607a" using the rainbow table manually.
Answer: Basketball  (already given in the table provided in explanation by TryHackMe)

### Crack the hash "5b31f93c09ad1d065c0491b764d04933" using online tools
Answer: tryhackme ( go to this site [site](https://hashes.com/en/decrypt/hash))

### Should you encrypt passwords? Yea/Nay
Answer: Nay

## Task- 4: Recognising password hashes

### How many rounds does sha512crypt ($6$) use by default?
Answer: 5000

### What's the hashcat example hash (from the website) for Citrix Netscaler hashes?
Answer: 1765058016a22f1b4e076dccd1c3df4e8e5c0839ccded98ea (visit this Hashcat Site)

### How long is a Windows NTLM hash, in characters?
Answer: 32

## Task -5 : Password Cracking

### Crack this hash: $2a$06$7yoU3Ng8dHTXphAg913cyO6Bjs3K5lBnwq5FJyA6d01pMSrddr1ZG
Answer: 85208520

Solution: First Identify the type of hash (format) by going to any online tool like [Hashes](https://hashes.com/en/tools/hash_identifier) or use hash-identifier on kali Linux 
          then use the Hashcat or John the ripper to crack the hash
Hash Identified as : bcrypt
using hashcat to find the numeric code used in hashcat to crack bcrypt hashes:
                                                                                         
┌──(root㉿kali)-[~/Desktop]
└─# hashcat --help | grep bcrypt
   3200 | bcrypt $2*$, Blowfish (Unix)                               | Operating System

Found 3200 and let's decrypt it now ...................run following command 
                                                                                                                                                                                                  
┌──(root㉿kali)-[~/Desktop]
└─# hashcat -m 3200 hash.txt /usr/share/wordlists/rockyou.txt  (you'll get your answer)

### Crack this hash: 9eb7ee7f551d2f0ac684981bd1f1e2fa4a37590199636753efe614d4db30e8e1 
Answer: halloween 

Hint: repeat the same process (it's SHA256)
┌──(root㉿kali)-[~/Desktop]
└─# hashcat -m 1400  hash.txt /usr/share/wordlists/rockyou.txt

9eb7ee7f551d2f0ac684981bd1f1e2fa4a37590199636753efe614d4db30e8e1:halloween

### Crack this hash: $6$GQXVvW4EuM$ehD6jWiMsfNorxy5SINsgdlxmAEl3.yif0/c3NqzGLa0P.S7KRDYjycw5bnYkF5ZtB8wQy8KnskuWQS3Yr1wQ0
Answer: spaceman

Hint: repeat the process

### Bored of this yet? Crack this hash: b6b0d451bbf6fed658659a9e7e5598fe
Answer: funforyou

Hint: use online hash cracker websites, one of them provided above

## Task - 6: Hashing for integrity checking

### What's the SHA1 sum for the amd64 Kali 2019.4 ISO? http://old.kali.org/kali-images/kali-2019.4/
Answer: 186c5227e24ceb60deb711f1bdc34ad9f4718ff9

### What's the hashcat mode number for HMAC-SHA512 (key = $pass)?
Answer: 1750


