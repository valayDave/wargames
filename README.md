# WAR GAMES Results. 

## BANDIT 

### Level 0 
- Basic SSH command to reach and complete level. Read the readme file using. 

### Level 1
- used the ```./``` convention to ```cat``` the filename. 

### Level 2 
- used ```cat spaces\ in\ this\ filename ``` to open file for password. 

### Level 3 

- Steps : 
    - ```cd hidden```
    - ```ls -lah```
    - ```cat .hidden```

### Level 4 

- ```cd inhere && strings ./*``

### Level 5

- TO find the file : ```find ./ -type f -size 1033c -exec ls {} \;```

### Level 6 

- To find the file : ```find / -type f -size 33c -group bandit6 -user bandit7 -exec ls -lh {} \;```

### Level 7 

- ```cat data.txt | grep millionth```

### Level 8 

- ```cat data.txt | uniq | sort -d | uniq -c```

### Level 9

- ```strings data.txt | grep =*``` 

### Level 10 

- ```cat data.txt | base64 --decode```

### Level 11

- ```cat data.txt | tr '[a-z]' '[n-za-m]' | tr '[A-Z]' '[N-ZA-M]' ```

### Level 12 

- password : 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
- ```xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat```
- bzcat : Used to decompress to standard output for bzip2 type files. 
- zcat: Used to uncompress information. 
### Level 13 

- password : 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
- Copy private key to localmachine 
- create key file and chmod it 
- ssh using that key. 

### Level 14. 

- password : 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
- copy 14 password : ```cat /etc/bandit_pass/bandit14```
- post it on : ```telnet localhost 30000```

### Level 15 

- Password : BfMYroe26WYalil77FoDi9qh59eK5xNr
- ```openssl s_client -connect localhost:30001```

### Level 16 

- Password : cluFn7wTiGryunymYOu4RcffSxQluehd

### Level 17

- diff command btw old and new 

### Level 18

- Password : kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
- run commands through ssh. 

### Level 19 

- Password : IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
- ```./bandit20-do cat /etc/bandit_pass/bandit20```

### Level 20 

- Password : GbKksEFF4yrVs6il55v6gwY5aVje5f0j
- ```netcat -vvl 127.0.0.1 -p 1111``` to send messages to the binary which connects on port 1111. 

### Level 21 

- Password : gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
- Check cron file which leads to the sh file and then get the password from there. 

### Level 22 

- Password : Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
- Cron file was putting the password in the tmp folder. For each user it was creating a copy in the tmp folder but in md5 format. So modifying the line in cronfile led to the file which held the password. 

### Level 23

- Password : jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n