## Task - 9 : Cracking Password Protected Zip Files

### What is the password for the secure.zip file?
Answer: **pass123**

Command to calculate the hash of the file : 

zip2john secure_zip_file.zip > zip_hash.txt

cracking :
john --wordlist=/usr/share/wordlists/rockyou.txt zip_hash.txt

### What is the contents of the flag inside the zip file?
Answer: THM{w3ll_d0n3_h4sh_r0y4l}

## Task - 10 : Cracking Password Protected RAR Archives

### What is the password for the secure.rar file?
Answer: password

Hint: repeat the same process but this time for : **rar2john**

### What is the contents of the flag inside the zip file?
Answer: THM{r4r_4rch1ve5_th15_t1m3}

## Task - 11 : Cracking SSH Keys with John

### What is the SSH private key password?
Answer: mangoo 

Hint: repeat the same process from task-10 but for this time use : **ssh2john**

## Task - 12 : Further Reading , it's just reading 😊😊
