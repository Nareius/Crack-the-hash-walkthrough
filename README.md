# Crack-the-hash-walkthrough

Hi in this walkthrough I am going to help you complete the ctf room crack the hask of tryhackme

# Task 1
In this room you are going to use a website that helps you crack hashes automatically for example
https://crackstation.net/

# Question 1
48bb6e862e54f2a795ffc4e541caed4d

By inputting the hash in the website you get the answer
(easy) which was hashed in md5

# Question 2
CBFDAC6008F9CAB4083784CBD1874F76618D2A97 

The answer for this one is going to be
(password123)

# Question 3
1C8BFE8F801D79745C4631D09FFF36C82AA37FC4CCE4FC946683D7B336B63032

The answer for this one is going to be
(letmein)

# Question 4
$2y$12$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom
Now this is going to get a little bit trickier and you are going to need to run hashid in your terminal and identify what type of hash it is
```
hashid -m "\$2y\$12\$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom"
```

You will find the type of the hash like this
bcrypt [Hashcat Mode:3200]

```
hashcat -m 3200 "\$2y\$12\$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom" /path/rockyou.txt
```
After waitting a little bit you get the answer 
(bleh)

# Question 5
279412f945939ba78ce0758d3fd83daa

Again using crackstation we get the answer
(Eternity22)

# Task 2
# Question 6
Hash: F09EDCB1FCEFC6DFB23DC3505A882655FF77375ED8AA2D1C13F640FCCC2D0C85

The answer will be
(paule)

# Question 7
1DFECA0C002AE40B8619ECF94819CC1B

The answer will be
(n63umy8lkf4i)

# Question 8
Hash: $6$aReallyHardSalt$6WKUTqzq.UQQmrm0p/T7MPpMbGNnzXPMAXi4bJMl9be.cfi3/qxIf.hsGpS41BqMhSrHVXgMpdjS6xeKZAs02.
Salt: aReallyHardSalt

Again in this on you are going to be using your terminal
```
hashid -m "\$6\$aReallyHardSalt\$6WKUTqzq.UQQmrm0p/T7MPpMbGNnzXPMAXi4bJMl9be.cfi3/qxIf.hsGpS41BqMhSrHVXgMpdjS6xeKZAs02."
```

```
hashcat -m 1800 "\$6\$aReallyHardSalt\$6WKUTqzq.UQQmrm0p/T7MPpMbGNnzXPMAXi4bJMl9be.cfi3/qxIf.hsGpS41BqMhSrHVXgMpdjS6xeKZAs02." /path/rockyou.txt
```

And the answer will be 
(waka99)

# Question 9
Hash: e5d8870e5bdd26602cab8dbe07a942c8669e56d6
Salt: tryhackme
```
hashid -m e5d8870e5bdd26602cab8dbe07a942c8669e56d6:tryhackme /path/rockyou.txt
```

The finall answer will be 
(481616481616)

Thank you for your patience by reading this. I hope I have helped with this walkthrough on completing this room
