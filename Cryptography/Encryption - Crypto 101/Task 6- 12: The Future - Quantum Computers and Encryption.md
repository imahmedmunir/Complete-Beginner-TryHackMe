## Task -6 : RSA - Rivest Shamir Adleman

### p = 4391, q = 6659. What is n?
Answer: 29239669

## Task - 7 : Establishing Keys Using Asymmetric Cryptography : just reading

## Task - 8 : Digital signatures and Certificates

### Who is TryHackMe's HTTPS certificate issued by?
Answer: E1

## Task - 9 : SSH Authentication

### What algorithm does the key use?
Answer: RSA

### Crack the password with John The Ripper and rockyou, what's the passphrase for the key?
Answer: delicious

**Hint: go this this repo and find more details [John the ripper](https://github.com/imahmedmunir/Complete-Beginner-TryHackMe/tree/main/Cryptography/John%20the%20Ripper)**


## Task - 10 : Explaining Diffie Hellman Key Exchange, just reading 

## Task - 11 : PGP, GPG and AES

### You have the private key, and a file encrypted with the public key. Decrypt the file. What's the secret word?

**Hint: If you're fimiliar with gpg , it's good to go. you can install it and import the key and read the message. Followign commands cna help you.**
**After unzipping the file , you'll have to import it**
**C:\Users\User\Downloads\Tryhackme>gpg --import tryhackme.key
gpg: key FFA4B5252BAEB2E6: public key "TryHackMe (Example Key)" imported
gpg: key FFA4B5252BAEB2E6: secret key imported
gpg: Total number processed: 1
gpg:               imported: 1
gpg:       secret keys read: 1
gpg:   secret keys imported: 1**

Now you can read the message you found after unzipping : 

**C:\Users\User\Downloads\Tryhackme>gpg --decrypt message.gpg
gpg: encrypted with rsa1024 key, ID 2A0A5FDC5081B1C5, created 2020-06-30
      "TryHackMe (Example Key)"
You decrypted the file!
The secret word is Pineapple.**

## Task - 12 : The Future - Quantum Computers and Encryption , just reading
