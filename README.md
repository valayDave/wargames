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
- Create a shell script inside a folder in the the tmp folder and also a text file inside the same folder. ```chmod 777``` both the files. 
- the shell script should cat the password in the bandit_pass folder for user bandit24 into a text file in the tmp directory
- cp the shell script from current tmp folder to ```/var/spool/bandit24``` to make a copy of the script that will execute with the cron job. 
- The password is available in the text file in the tmp folder. 

### Level 24 : 

- Password : UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ

- Using Brute force with netcat to add check for the password. 

- ```for i in {0000..9999}; do     echo "UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i"; done | nc localhost 30002 > /tmp/valay/bandit25.txt```

### Level 25 : 

- Password : `uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG`: Private Key given on lvl 25 for level 26. 
- Script to get password : 
```sh
for i in {0000..9999}; 
do     
    echo "UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i"; 
done | nc localhost 30002 > /tmp/valay/bandit25.txt

```

### Level 26 :

- Password : ```5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z```
- The ssh is modified to launch the ```more``` command and then exit. So resizing the window works for the more command. Once the window is small enough a size the more command works and the shell session doesnt exist. The more can convert to vi by pressing ```v``` in the more interface. 
- Using the ```:e /etc/bandit_pass/bandit26``` in the more interface gets us the password file for 26. 
- On top of that vi can offer an access to the shell from there. once can set shell in a variable in vi to call the shell. issue the command : ```:set shell=/bin/bash``` to the vi. Once set calling ```:shell``` to vi will open the shell for the user. 

### Level 27 

- Password : ```3ba3118a22e93127a4ed485be72ef5ea``` 
- Git clone of repository gave the output. 

### Level 28 

- Password : ```0ef186ac70e04ea33b4c1853d2526fa2```
- Password stored in the git history of the repository. 

### Level 29 

- Password : ```bbc96594b4e001778eee9975372716b2```