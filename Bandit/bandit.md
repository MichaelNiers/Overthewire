# Bandit Walkthrough

*Bandit is a wargame that helps to learn and practice security concepts in the form of fun-filled games*

*The game is organised in levels. You start at Level 0 and try to “beat” or “finish” it. Finishing a level results in information on how to start the next level.*

*Below the passwords and solutions for all levels.*

---

**Level 0 --> 1**

> **Level Goal**
>
>The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

```console
bandit0@bandit:~$ cat readme
```

Password:    *boJ9jbbUNNfktd78OOpsqOltutMc3MY1*

---

**Level 1 --> 2**

> **Level Goal**
>
>The password for the next level is stored in a file called - located in the home directory

```console
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
```

Password:    *CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9*

---

**Level 2 --> 3**

> **Level Goal**
>
>The password for the next level is stored in a file called spaces in this filename located in the home directory

```console
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename
```

Password:    *UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK*

---

**Level 3 --> 4**

> **Level Goal**
>
>The password for the next level is stored in a hidden file in the inhere directory.

```console
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Nov 14  2014 .
drwxr-xr-x 3 root    root    4096 Nov 14  2014 ..
-rw-r----- 1 bandit4 bandit3   33 Nov 14  2014 .hidden
bandit3@bandit:~/inhere$ cat .hidden
```

Password:    *pIwrPrtPN36QITSp3EQaw936yaFoFgAB*

---

**Level 4 --> 5**

> **Level Goal**
>
>The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

```console
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls -la
total 48
-rw-r----- 1 bandit5 bandit4   33 Nov 14  2014 -file00
-rw-r----- 1 bandit5 bandit4   33 Nov 14  2014 -file01
-rw-r----- 1 bandit5 bandit4   33 Nov 14  2014 -file02
-rw-r----- 1 bandit5 bandit4   33 Nov 14  2014 -file03
-rw-r----- 1 bandit5 bandit4   33 Nov 14  2014 -file04
-rw-r----- 1 bandit5 bandit4   33 Nov 14  2014 -file05
-rw-r----- 1 bandit5 bandit4   33 Nov 14  2014 -file06
-rw-r----- 1 bandit5 bandit4   33 Nov 14  2014 -file07
-rw-r----- 1 bandit5 bandit4   33 Nov 14  2014 -file08
-rw-r----- 1 bandit5 bandit4   33 Nov 14  2014 -file09
drwxr-xr-x 2 root    root    4096 Oct 19  2016 .
drwxr-xr-x 3 root    root    4096 Nov 14  2014 ..
bandit4@bandit:~/inhere$
bandit4@bandit:~/inhere$ cat ./-file07
```

Password:    *koReBOKuIDDepwhWk7jZC0RTdopnAYKh*

---

**Level 5 --> 6**

> **Level Goal**
>
>The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:


    human-readable
    1033 bytes in size
    not executable


```console
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls -la
total 88
drwxr-x--- 22 root bandit5 4096 Nov 14  2014 .
drwxr-xr-x  3 root root    4096 Nov 14  2014 ..
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere00
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere01
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere02
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere03
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere04
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere05
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere06
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere07
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere08
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere09
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere10
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere11
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere12
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere13
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere14
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere15
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere16
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere17
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere18
drwxr-x---  2 root bandit5 4096 Nov 14  2014 maybehere19
bandit5@bandit:~/inhere$ find . -type f -readable ! -executable -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
```

Password:    *DXjZPULLxYr17uwoI01bNLQbtFemEgo7*

---

**Level 6 --> 7**

> **Level Goal**
>
>The password for the next level is stored somewhere on the server and has all of the following properties:


    owned by user bandit7
    owned by group bandit6
    33 bytes in size


```console
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
```

Password:    *HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs*

---

**Level 7 --> 8**

> **Level Goal**
>
>The password for the next level is stored in the file data.txt next to the word millionth

```console
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt | grep "millionth"
```

Password:    *cvX2JJa4CFALtqS87jk27qwqGhBM9plV*

---

**Level 8 --> 9**

> **Level Goal**
>
>The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

```console
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
```

Password:    *UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR*

---

**Level 9 --> 10**

> **Level Goal**
>
>The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

```console
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep "="
epr~F=K
7?YD=
?M=HqAH
/(Ne=
C=_"
I========== the6
z5Y=
`h(8=`
n\H=;
========== password
========== ism
N$=&
l/a=L)
f=C(
```

Password:    *truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk*

---

**Level 10 --> 11**

> **Level Goal**
>
>The password for the next level is stored in the file data.txt, which contains base64 encoded data

```console
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg==
bandit10@bandit:~$ cat data.txt | base64 --decode
```

Password:    *IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR*

---

**Level 11 --> 12**

> **Level Goal**
>
>The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

```console
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh
bandit11@bandit:~$ cat data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'
```

Password:    *5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu*

---

**Level 12 --> 13**

> **Level Goal**
>
>The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

```console
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ mkdir /tmp/kan1shka9
bandit12@bandit:~$ cp data.txt /tmp/kan1shka9
bandit12@bandit:~$ cd /tmp/kan1shka9
bandit12@bandit:/tmp/kan1shka9$ ls
data.txt
bandit12@bandit:/tmp/kan1shka9$ file data.txt
data.txt: ASCII text
bandit12@bandit:/tmp/kan1shka9$ xxd -r data.txt > data_xxd_reverse
bandit12@bandit:/tmp/kan1shka9$ file data_xxd_reverse
data_xxd_reverse: gzip compressed data, was "data2.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression
bandit12@bandit:/tmp/kan1shka9$ zcat data_xxd_reverse > data_zcat
bandit12@bandit:/tmp/kan1shka9$ file data_zcat
data_zcat: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/kan1shka9$ bzip2 -d data_zcat
bzip2: Can't guess original name for data_zcat -- using data_zcat.out
bandit12@bandit:/tmp/kan1shka9$ file data_zcat.out
data_zcat.out: gzip compressed data, was "data4.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression
bandit12@bandit:/tmp/kan1shka9$ ls
data.txt  data_xxd_reverse  data_zcat.out
bandit12@bandit:/tmp/kan1shka9$ zcat data_zcat.out > data_zcat_2
bandit12@bandit:/tmp/kan1shka9$ file data_zcat_2
data_zcat_2: POSIX tar archive (GNU)
bandit12@bandit:/tmp/kan1shka9$ tar xvf data_zcat_2
data5.bin
bandit12@bandit:/tmp/kan1shka9$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/kan1shka9$ tar xvf data5.bin
data6.bin
bandit12@bandit:/tmp/kan1shka9$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/kan1shka9$ bzip2 -d data6.bin
bzip2: Can't guess original name for data6.bin -- using data6.bin.out
bandit12@bandit:/tmp/kan1shka9$ file data6.bin.out
data6.bin.out: POSIX tar archive (GNU)
bandit12@bandit:/tmp/kan1shka9$ tar xvf data6.bin.out
data8.bin
bandit12@bandit:/tmp/kan1shka9$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression
bandit12@bandit:/tmp/kan1shka9$ zcat data8.bin > data8_zcat
bandit12@bandit:/tmp/kan1shka9$ file data8_zcat
data8_zcat: ASCII text
bandit12@bandit:/tmp/kan1shka9$ cat data8_zcat
```

Password:    *8ZjyCRiBWFYkneahHwxCv3wb2a10RpYL*

---

**Level 13 --> 14**

> **Level Goal**
>
>The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

```console
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ file sshkey.private
sshkey.private: PEM RSA private key
bandit13@bandit:~$ cat sshkey.private
-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAxkkOE83W2cOT7IWhFc9aPaaQmQDdgzuXCv+ppZHa++buSkN+
gg0tcr7Fw8NLGa5+Uzec2rEg0WmeevB13AIoYp0MZyETq46t+jk9puNwZwIt9XgB
ZufGtZEwWbFWw/vVLNwOXBe4UWStGRWzgPpEeSv5Tb1VjLZIBdGphTIK22Amz6Zb
ThMsiMnyJafEwJ/T8PQO3myS91vUHEuoOMAzoUID4kN0MEZ3+XahyK0HJVq68KsV
ObefXG1vvA3GAJ29kxJaqvRfgYnqZryWN7w3CHjNU4c/2Jkp+n8L0SnxaNA+WYA7
jiPyTF0is8uzMlYQ4l1Lzh/8/MpvhCQF8r22dwIDAQABAoIBAQC6dWBjhyEOzjeA
J3j/RWmap9M5zfJ/wb2bfidNpwbB8rsJ4sZIDZQ7XuIh4LfygoAQSS+bBw3RXvzE
pvJt3SmU8hIDuLsCjL1VnBY5pY7Bju8g8aR/3FyjyNAqx/TLfzlLYfOu7i9Jet67
xAh0tONG/u8FB5I3LAI2Vp6OviwvdWeC4nOxCthldpuPKNLA8rmMMVRTKQ+7T2VS
nXmwYckKUcUgzoVSpiNZaS0zUDypdpy2+tRH3MQa5kqN1YKjvF8RC47woOYCktsD
o3FFpGNFec9Taa3Msy+DfQQhHKZFKIL3bJDONtmrVvtYK40/yeU4aZ/HA2DQzwhe
ol1AfiEhAoGBAOnVjosBkm7sblK+n4IEwPxs8sOmhPnTDUy5WGrpSCrXOmsVIBUf
laL3ZGLx3xCIwtCnEucB9DvN2HZkupc/h6hTKUYLqXuyLD8njTrbRhLgbC9QrKrS
M1F2fSTxVqPtZDlDMwjNR04xHA/fKh8bXXyTMqOHNJTHHNhbh3McdURjAoGBANkU
1hqfnw7+aXncJ9bjysr1ZWbqOE5Nd8AFgfwaKuGTTVX2NsUQnCMWdOp+wFak40JH
PKWkJNdBG+ex0H9JNQsTK3X5PBMAS8AfX0GrKeuwKWA6erytVTqjOfLYcdp5+z9s
8DtVCxDuVsM+i4X8UqIGOlvGbtKEVokHPFXP1q/dAoGAcHg5YX7WEehCgCYTzpO+
xysX8ScM2qS6xuZ3MqUWAxUWkh7NGZvhe0sGy9iOdANzwKw7mUUFViaCMR/t54W1
GC83sOs3D7n5Mj8x3NdO8xFit7dT9a245TvaoYQ7KgmqpSg/ScKCw4c3eiLava+J
3btnJeSIU+8ZXq9XjPRpKwUCgYA7z6LiOQKxNeXH3qHXcnHok855maUj5fJNpPbY
iDkyZ8ySF8GlcFsky8Yw6fWCqfG3zDrohJ5l9JmEsBh7SadkwsZhvecQcS9t4vby
9/8X4jS0P8ibfcKS4nBP+dT81kkkg5Z5MohXBORA7VWx+ACohcDEkprsQ+w32xeD
qT1EvQKBgQDKm8ws2ByvSUVs9GjTilCajFqLJ0eVYzRPaY6f++Gv/UVfAPV4c+S0
kAWpXbv5tbkkzbS0eaLPTKgLzavXtQoTtKwrjpolHKIHUz6Wu+n4abfAIRFubOdN
/+aLoRQ0yBDRbdXMsZN/jvY44eM+xRLdRVyMmdPtP8belRi2E2aEzA==
-----END RSA PRIVATE KEY-----
bandit13@bandit:~$ ssh bandit14@localhost -i sshkey.private -p 2220
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
```

Password:    *4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e*

---

**Level 14 --> 15**

> **Level Goal**
>
>The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

```console
bandit14@bandit:~$ nc localhost 30000
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
Correct!
```

Password:    *BfMYroe26WYalil77FoDi9qh59eK5xNr*

---

**Level 15 --> 16**

> **Level Goal**
>
>The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

>Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

```console
bandit14@bandit:~$ openssl s_client -connect localhost:30001 -ign_eof
CONNECTED(00000003)
depth=0 CN = li190-250.members.linode.com
verify error:num=18:self signed certificate
verify return:1
depth=0 CN = li190-250.members.linode.com
verify return:1
---
Certificate chain
 0 s:/CN=li190-250.members.linode.com
   i:/CN=li190-250.members.linode.com
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIC3jCCAcagAwIBAgIJAI5QiWZw4YHbMA0GCSqGSIb3DQEBCwUAMCcxJTAjBgNV
BAMTHGxpMTkwLTI1MC5tZW1iZXJzLmxpbm9kZS5jb20wHhcNMTQxMTE0MTAyODA0
WhcNMjQxMTExMTAyODA0WjAnMSUwIwYDVQQDExxsaTE5MC0yNTAubWVtYmVycy5s
aW5vZGUuY29tMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAsKmy9o5z
WU+1EH7Z3bB5TGQA+16zXDcEJy6tZWZ8CDrRyQXiahendp45BWUc/ZuLDo0+B3Wt
ZXjofmLw/F4fmR+8X1s1fQZX2dFt920qEm7LxqzWd0c7FdHiBwwRrwhkk+3cQpOB
TTGdLWEgpdmwwNZDTUdsDLzjDczPnju6T6p6ArTECztPbmTjfY4QIRtC6capL1Z+
yPJSQVAuAMEX1wTDWTGdm0VV7oW4F5cGZutf6QAP51jdhSyZuGilIPHbnj0l6Qc7
a7+OtEsEGi31aJ8KpRf7LNZ7DXCuoB3Hf75Pd6VjDgoOIagcH0NYqa75gEjBkGzs
ktLWykT7ag7fKwIDAQABow0wCzAJBgNVHRMEAjAAMA0GCSqGSIb3DQEBCwUAA4IB
AQCaZdUNAj8WDEKWdoU3LNXUBJlTJwiWBrh550PbHSQORcCz2K0kiMei1A4ojK2N
dMHFGAqAeUEaxtz92p2BoFpZasAtdSa3u63tBckFhfUolIS1TC7Cj51y19ysTeep
fGPFpuPCVqVPsruei8Z/iqn3bFIhQQdmumeePZQdPMwZSWHNVYC5XODd7PvNDrDu
5MZJjkz4+6LbwwAvyew62meFN2QEsYbK2Brtbhze+IjE27FGWlSw4K3jlwa409MD
MTf4JU41ELaYY8G/LSNDJsBVhhkHzvXR9iCbXxNz3IL0dQDNj7h4LKhBy0q7hvqg
kDzwlmBO4WKSmCAuky44cXmd
-----END CERTIFICATE-----
subject=/CN=li190-250.members.linode.com
issuer=/CN=li190-250.members.linode.com
---
No client certificate CA names sent
---
SSL handshake has read 1714 bytes and written 637 bytes
---
New, TLSv1/SSLv3, Cipher is DHE-RSA-AES256-SHA
Server public key is 2048 bit
Secure Renegotiation IS supported
Compression: NONE
Expansion: NONE
SSL-Session:
    Protocol  : SSLv3
    Cipher    : DHE-RSA-AES256-SHA
    Session-ID: 3D3C8090F26497A5D8EC930C9D4B09A577BE6E4872070FE6FB59CB073B6F9EDA
    Session-ID-ctx:
    Master-Key: E73F17121DE4869A375F9683213BD9C6F742B74819AD2A2AD69A37931DA57499C45CFFDAAEB1AE708EE83C6082EB67A2
    Key-Arg   : None
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    Start Time: 1495332494
    Timeout   : 300 (sec)
    Verify return code: 18 (self signed certificate)
---
BfMYroe26WYalil77FoDi9qh59eK5xNr
Correct!
```

Password:    *cluFn7wTiGryunymYOu4RcffSxQluehd*

---

**Level 16 --> 17**

> **Level Goal**
>
>The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

```console
bandit14@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
depth=0 CN = li190-250.members.linode.com
verify error:num=18:self signed certificate
verify return:1
depth=0 CN = li190-250.members.linode.com
verify return:1
---
Certificate chain
 0 s:/CN=li190-250.members.linode.com
   i:/CN=li190-250.members.linode.com
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIC3jCCAcagAwIBAgIJAI5QiWZw4YHbMA0GCSqGSIb3DQEBCwUAMCcxJTAjBgNV
BAMTHGxpMTkwLTI1MC5tZW1iZXJzLmxpbm9kZS5jb20wHhcNMTQxMTE0MTAyODA0
WhcNMjQxMTExMTAyODA0WjAnMSUwIwYDVQQDExxsaTE5MC0yNTAubWVtYmVycy5s
aW5vZGUuY29tMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAsKmy9o5z
WU+1EH7Z3bB5TGQA+16zXDcEJy6tZWZ8CDrRyQXiahendp45BWUc/ZuLDo0+B3Wt
ZXjofmLw/F4fmR+8X1s1fQZX2dFt920qEm7LxqzWd0c7FdHiBwwRrwhkk+3cQpOB
TTGdLWEgpdmwwNZDTUdsDLzjDczPnju6T6p6ArTECztPbmTjfY4QIRtC6capL1Z+
yPJSQVAuAMEX1wTDWTGdm0VV7oW4F5cGZutf6QAP51jdhSyZuGilIPHbnj0l6Qc7
a7+OtEsEGi31aJ8KpRf7LNZ7DXCuoB3Hf75Pd6VjDgoOIagcH0NYqa75gEjBkGzs
ktLWykT7ag7fKwIDAQABow0wCzAJBgNVHRMEAjAAMA0GCSqGSIb3DQEBCwUAA4IB
AQCaZdUNAj8WDEKWdoU3LNXUBJlTJwiWBrh550PbHSQORcCz2K0kiMei1A4ojK2N
dMHFGAqAeUEaxtz92p2BoFpZasAtdSa3u63tBckFhfUolIS1TC7Cj51y19ysTeep
fGPFpuPCVqVPsruei8Z/iqn3bFIhQQdmumeePZQdPMwZSWHNVYC5XODd7PvNDrDu
5MZJjkz4+6LbwwAvyew62meFN2QEsYbK2Brtbhze+IjE27FGWlSw4K3jlwa409MD
MTf4JU41ELaYY8G/LSNDJsBVhhkHzvXR9iCbXxNz3IL0dQDNj7h4LKhBy0q7hvqg
kDzwlmBO4WKSmCAuky44cXmd
-----END CERTIFICATE-----
subject=/CN=li190-250.members.linode.com
issuer=/CN=li190-250.members.linode.com
---
No client certificate CA names sent
---
SSL handshake has read 1714 bytes and written 637 bytes
---
New, TLSv1/SSLv3, Cipher is DHE-RSA-AES256-SHA
Server public key is 2048 bit
Secure Renegotiation IS supported
Compression: NONE
Expansion: NONE
SSL-Session:
    Protocol  : SSLv3
    Cipher    : DHE-RSA-AES256-SHA
    Session-ID: 20CA4FD2722C9FC893DECEE1CA87C16F698563B7116265F39D48D3D8F6853EAF
    Session-ID-ctx:
    Master-Key: FE0F0C093E12801D5CF052F1734410396EF1D35B1C85BA0DA685ED8A990E62A96221321469CA02D4C7374A628EDEECE8
    Key-Arg   : None
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    Start Time: 1495333239
    Timeout   : 300 (sec)
    Verify return code: 18 (self signed certificate)
---
cluFn7wTiGryunymYOu4RcffSxQluehd
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
```

Password:    *-*

---

**Level 17 --> 18**

> **Level Goal**
>
>There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

>NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

```console
➜  ~ touch sshkey.private
➜  ~ nano sshkey.private
➜  ~ cat sshkey.private
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
➜  ~ chmod 600 sshkey.private
➜  ~ ssh bandit17@bandit.labs.overthewire.org -p 2220 -i sshkey.private
bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ file *
passwords.new: ASCII text
passwords.old: ASCII text
bandit17@bandit:~$ diff passwords.new passwords.old
42c42
---
```

Password:    *kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd*

---

**Level 18 --> 19**

> **Level Goal**
>
>The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

```console
➜  ~ ssh bandit18@bandit.labs.overthewire.org -p 2220
Byebye !
➜  ~ ssh bandit18@bandit.labs.overthewire.org -p 2220 lsThis is the OverTheWire game server. More information on http://www.overthewire.org/wargamesPlease note that wargame usernames are no longer level<X>, but wargamename<X>
e.g. vortex4, semtex2, ...Note: at this moment, blacksun is not available.bandit18@bandit.labs.overthewire.org's password:
readme
➜  ~ ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readmeThis is the OverTheWire game server. More information on http://www.overthewire.org/wargamesPlease note that wargame usernames are no longer level<X>, but wargamename<X>
e.g. vortex4, semtex2, ...Note: at this moment, blacksun is not available.
```

Password:    *IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x*

---

**Level 19 --> 20**

> **Level Goal**
>
>To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

```console
bandit19@bandit:~$ ls
bandit20-do
bandit19@bandit:~$ file bandit20-do
bandit20-do: setuid ELF 32-bit LSB  executable, Intel 80386, version 1 (SYSV), dynamically linked (uses shared libs), for GNU/Linux 2.6.24, BuildID[sha1]=08e74b8e092a91103efaab7916d75f08b887ab4d, not stripped
bandit19@bandit:~$ ls -la bandit20-do
-rwsr-x--- 1 bandit20 bandit19 7370 Nov 14  2014 bandit20-do
bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do id
bandit19@bandit:~$ ./bandit20-do id
uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20) groups=11020(bandit20),11019(bandit19)
bandit19@bandit:~$ ./bandit20-do whoami
bandit20
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
```

Password:    *GbKksEFF4yrVs6il55v6gwY5aVje5f0j*

---

**Level 20 --> 21**

> **Level Goal**
>
>There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

>NOTE: Try connecting to your own network daemon to see if it works as you think

```console
bandit20@bandit:~$ ls -la suconnect
-rwsr-x--- 1 bandit21 bandit20 8006 Nov 14  2014 suconnect
bandit20@bandit:~$ ./suconnect
Usage: ./suconnect <portnumber>
This program will connect to the given port on localhost using TCP. If it receives the correct password from the other side, the next password is transmitted back.
bandit20@bandit:~$
```

Password:    *gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr*

---

**Level 21 --> 22**

> **Level Goal**
>
>A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

```console
bandit21@bandit:~$ ls
bandit21@bandit:~$ cd /etc/cron.d/
bandit21@bandit:/etc/cron.d$ ls -l
total 92
-r--r----- 1 root root  46 Nov 14  2014 behemoth4_cleanup
-rw-r--r-- 1 root root 355 May 25  2013 cron-apt
-rw-r--r-- 1 root root  61 Nov 14  2014 cronjob_bandit22
-rw-r--r-- 1 root root  62 Nov 14  2014 cronjob_bandit23
-rw-r--r-- 1 root root  61 May  3  2015 cronjob_bandit24
-rw-r--r-- 1 root root  62 May  3  2015 cronjob_bandit24_root
-r--r----- 1 root root  47 Nov 14  2014 leviathan5_cleanup
-rw------- 1 root root 233 Nov 14  2014 manpage3_resetpw_job
-rw-r--r-- 1 root root  51 Nov 14  2014 melinda-stats
-rw-r--r-- 1 root root  54 Jun 25  2016 natas-session-toucher
-rw-r--r-- 1 root root  49 Jun 25  2016 natas-stats
-r--r----- 1 root root  44 Jun 25  2016 natas25_cleanup
-r--r----- 1 root root  47 Aug  3  2015 natas25_cleanup~
-r--r----- 1 root root  47 Jun 25  2016 natas26_cleanup
-r--r----- 1 root root  43 Jun 25  2016 natas27_cleanup
-rw-r--r-- 1 root root 510 Oct 29  2014 php5
-rw-r--r-- 1 root root  63 Jul  8  2015 semtex0-32
-rw-r--r-- 1 root root  63 Jul  8  2015 semtex0-64
-rw-r--r-- 1 root root  64 Jul  8  2015 semtex0-ppc
-rw-r--r-- 1 root root  35 Nov 14  2014 semtex5
-rw-r--r-- 1 root root 396 Nov 10  2013 sysstat
-rw-r--r-- 1 root root  29 Nov 14  2014 vortex0
-rw-r--r-- 1 root root  30 Nov 14  2014 vortex20
bandit21@bandit:/etc/cron.d$ cat cronjob_bandit22
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:/etc/cron.d$ file /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
/tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv: ASCII text
bandit21@bandit:/etc/cron.d$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

Password:    *Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI*

---

**Level 22 --> 23**

> **Level Goal**
>
>A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

>NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

```console
bandit22@bandit:~$ ls
bandit22@bandit:~$ cd /etc/cron.d
bandit22@bandit:/etc/cron.d$ ls -l
total 92
-r--r----- 1 root root  46 Nov 14  2014 behemoth4_cleanup
-rw-r--r-- 1 root root 355 May 25  2013 cron-apt
-rw-r--r-- 1 root root  61 Nov 14  2014 cronjob_bandit22
-rw-r--r-- 1 root root  62 Nov 14  2014 cronjob_bandit23
-rw-r--r-- 1 root root  61 May  3  2015 cronjob_bandit24
-rw-r--r-- 1 root root  62 May  3  2015 cronjob_bandit24_root
-r--r----- 1 root root  47 Nov 14  2014 leviathan5_cleanup
-rw------- 1 root root 233 Nov 14  2014 manpage3_resetpw_job
-rw-r--r-- 1 root root  51 Nov 14  2014 melinda-stats
-rw-r--r-- 1 root root  54 Jun 25  2016 natas-session-toucher
-rw-r--r-- 1 root root  49 Jun 25  2016 natas-stats
-r--r----- 1 root root  44 Jun 25  2016 natas25_cleanup
-r--r----- 1 root root  47 Aug  3  2015 natas25_cleanup~
-r--r----- 1 root root  47 Jun 25  2016 natas26_cleanup
-r--r----- 1 root root  43 Jun 25  2016 natas27_cleanup
-rw-r--r-- 1 root root 510 Oct 29  2014 php5
-rw-r--r-- 1 root root  63 Jul  8  2015 semtex0-32
-rw-r--r-- 1 root root  63 Jul  8  2015 semtex0-64
-rw-r--r-- 1 root root  64 Jul  8  2015 semtex0-ppc
-rw-r--r-- 1 root root  35 Nov 14  2014 semtex5
-rw-r--r-- 1 root root 396 Nov 10  2013 sysstat
-rw-r--r-- 1 root root  29 Nov 14  2014 vortex0
-rw-r--r-- 1 root root  30 Nov 14  2014 vortex20
bandit22@bandit:/etc/cron.d$ cat cronjob_bandit23
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bashmyname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)echo "Copying password file /etc/bandit_pass/$myname to /tmp/$mytarget"cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@bandit:/etc/cron.d$ whoami
bandit22
bandit22@bandit:/etc/cron.d$ echo I am user bandit23 | md5sum | cut -d ' ' -f 1
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:/etc/cron.d$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
```

Password:    *jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n*

---

**Level 23 --> 24**

> **Level Goal**
>
>A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

>NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

>NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

```console
bandit23@bandit:~$ cd /etc/cron.d
bandit23@bandit:/etc/cron.d$ ls -l
total 92
-r--r----- 1 root root  46 Nov 14  2014 behemoth4_cleanup
-rw-r--r-- 1 root root 355 May 25  2013 cron-apt
-rw-r--r-- 1 root root  61 Nov 14  2014 cronjob_bandit22
-rw-r--r-- 1 root root  62 Nov 14  2014 cronjob_bandit23
-rw-r--r-- 1 root root  61 May  3  2015 cronjob_bandit24
-rw-r--r-- 1 root root  62 May  3  2015 cronjob_bandit24_root
-r--r----- 1 root root  47 Nov 14  2014 leviathan5_cleanup
-rw------- 1 root root 233 Nov 14  2014 manpage3_resetpw_job
-rw-r--r-- 1 root root  51 Nov 14  2014 melinda-stats
-rw-r--r-- 1 root root  54 Jun 25  2016 natas-session-toucher
-rw-r--r-- 1 root root  49 Jun 25  2016 natas-stats
-r--r----- 1 root root  44 Jun 25  2016 natas25_cleanup
-r--r----- 1 root root  47 Aug  3  2015 natas25_cleanup~
-r--r----- 1 root root  47 Jun 25  2016 natas26_cleanup
-r--r----- 1 root root  43 Jun 25  2016 natas27_cleanup
-rw-r--r-- 1 root root 510 Oct 29  2014 php5
-rw-r--r-- 1 root root  63 Jul  8  2015 semtex0-32
-rw-r--r-- 1 root root  63 Jul  8  2015 semtex0-64
-rw-r--r-- 1 root root  64 Jul  8  2015 semtex0-ppc
-rw-r--r-- 1 root root  35 Nov 14  2014 semtex5
-rw-r--r-- 1 root root 396 Nov 10  2013 sysstat
-rw-r--r-- 1 root root  29 Nov 14  2014 vortex0
-rw-r--r-- 1 root root  30 Nov 14  2014 vortex20
bandit23@bandit:/etc/cron.d$ cat cronjob_bandit24
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:/etc/cron.d$ cat cronjob_bandit24_root
* * * * * root /usr/bin/cronjob_bandit24_root.sh &> /dev/null
bandit23@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bashmyname=$(whoami)cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
 echo "Handling $i"
 timeout -s 9 60 "./$i"
 rm -f "./$i"
    fi
donebandit23@bandit:/etc/cron.d$
```

```console
bandit23@bandit:~$ mkdir /tmp/ooo
bandit23@bandit:~$ nano bandit24.sh
bandit23@bandit:~$ cat bandit24.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 >> /tmp/ooo/level24
bandit23@bandit:/tmp/ooo$ chmod 777 bandit24.sh
bandit23@bandit:/tmp/ooo$ cp bandit24.sh /var/spool/bandit24/
bandit23@bandit:/tmp/ooo$ chmod 777 /tmp/ooo
bandit23@bandit:/tmp/ooo$ ls /var/spool/bandit24/
bandit24.sh
<----After a couple of minutes---->
bandit23@bandit:/tmp/ooo$ ls /var/spool/bandit24/
bandit23@bandit:/tmp/ooo$ ls
bandit24.sh  level24
bandit23@bandit:/tmp/ooo$ cat level24
```
Password:    *UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ*

---

**Level 24 --> 25**

> **Level Goal**
>
>A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

```console
bandit24@bandit:/tmp/24$ nano hammer.sh
#!/bin/bash

for i in {9999..000}
do
	echo "UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i"
done
bandit24@bandit:/tmp/24$ chmod +x hammer.sh
bandit24@bandit:/tmp/24$ ./hammer.sh > bruteforce.sh
<----snip---->
bandit24@bandit:/tmp/24$ cat  bruteforce.sh | nc localhost 30002
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
<----snip---->
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Correct!
The password of user bandit25 is uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG

Exiting.
```

Password:    *uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG*

---

**Level 25 --> 26**

> **Level Goal**
>
>Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

```console
bandit25@bandit:~$ ls
bandit25@bandit:~$ cat bandit26.sshkey
-----BEGIN RSA PRIVATE KEY-----
MIIEpQIBAAKCAQEApis2AuoooEqeYWamtwX2k5z9uU1Afl2F8VyXQqbv/LTrIwdW
pTfaeRHXzr0Y0a5Oe3GB/+W2+PReif+bPZlzTY1XFwpk+DiHk1kmL0moEW8HJuT9
/5XbnpjSzn0eEAfFax2OcopjrzVqdBJQerkj0puv3UXY07AskgkyD5XepwGAlJOG
xZsMq1oZqQ0W29aBtfykuGie2bxroRjuAPrYM4o3MMmtlNE5fC4G9Ihq0eq73MDi
1ze6d2jIGce873qxn308BA2qhRPJNEbnPev5gI+5tU+UxebW8KLbk0EhoXB953Ix
3lgOIrT9Y6skRjsMSFmC6WN/O7ovu8QzGqxdywIDAQABAoIBAAaXoETtVT9GtpHW
qLaKHgYtLEO1tOFOhInWyolyZgL4inuRRva3CIvVEWK6TcnDyIlNL4MfcerehwGi
il4fQFvLR7E6UFcopvhJiSJHIcvPQ9FfNFR3dYcNOQ/IFvE73bEqMwSISPwiel6w
e1DjF3C7jHaS1s9PJfWFN982aublL/yLbJP+ou3ifdljS7QzjWZA8NRiMwmBGPIh
Yq8weR3jIVQl3ndEYxO7Cr/wXXebZwlP6CPZb67rBy0jg+366mxQbDZIwZYEaUME
zY5izFclr/kKj4s7NTRkC76Yx+rTNP5+BX+JT+rgz5aoQq8ghMw43NYwxjXym/MX
c8X8g0ECgYEA1crBUAR1gSkM+5mGjjoFLJKrFP+IhUHFh25qGI4Dcxxh1f3M53le
wF1rkp5SJnHRFm9IW3gM1JoF0PQxI5aXHRGHphwPeKnsQ/xQBRWCeYpqTme9amJV
tD3aDHkpIhYxkNxqol5gDCAt6tdFSxqPaNfdfsfaAOXiKGrQESUjIBcCgYEAxvmI
2ROJsBXaiM4Iyg9hUpjZIn8TW2UlH76pojFG6/KBd1NcnW3fu0ZUU790wAu7QbbU
i7pieeqCqSYcZsmkhnOvbdx54A6NNCR2btc+si6pDOe1jdsGdXISDRHFb9QxjZCj
6xzWMNvb5n1yUb9w9nfN1PZzATfUsOV+Fy8CbG0CgYEAifkTLwfhqZyLk2huTSWm
pzB0ltWfDpj22MNqVzR3h3d+sHLeJVjPzIe9396rF8KGdNsWsGlWpnJMZKDjgZsz
JQBmMc6UMYRARVP1dIKANN4eY0FSHfEebHcqXLho0mXOUTXe37DWfZza5V9Oify3
JquBd8uUptW1Ue41H4t/ErsCgYEArc5FYtF1QXIlfcDz3oUGz16itUZpgzlb71nd
1cbTm8EupCwWR5I1j+IEQU+JTUQyI1nwWcnKwZI+5kBbKNJUu/mLsRyY/UXYxEZh
ibrNklm94373kV1US/0DlZUDcQba7jz9Yp/C3dT/RlwoIw5mP3UxQCizFspNKOSe
euPeaxUCgYEAntklXwBbokgdDup/u/3ms5Lb/bm22zDOCg2HrlWQCqKEkWkAO6R5
/Wwyqhp/wTl8VXjxWo+W+DmewGdPHGQQ5fFdqgpuQpGUq24YZS8m66v5ANBwd76t
IZdtF5HXs2S5CADTwniUS5mX1HO9l5gUkk+h0cH5JnPtsMCnAUM+BRY=
-----END RSA PRIVATE KEY-----
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost
bandit26@bandit:~$ :set shell=/bin/bash
-v
bandit26@bandit:~$ :r /etc/bandit_pass/bandit26
```

Password:    *5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z*

---

**Level 26 --> 27**

> **Level Goal**
>
>Good job getting a shell! Now hurry and grab the password for bandit27!

```console
bandit26@bandit:~$ ls -l
./bandit27-do cat /etc/bandit_pass/bandit27

```

Password:    *3ba3118a22e93127a4ed485be72ef5ea*

---

**Level 27 --> 28**

> **Level Goal**
>
>There is a git repository at ssh://bandit27-git@localhost/home/bandit27-git/repo. The password for the user bandit27-git is the same as for the user bandit27.

>Clone the repository and find the password for the next level.

```console
bandit27@bandit:~$ mkdir /tmp/ban4
bandit27@bandit:~$ cd /tmp/ban4
bandit27@bandit:/tmp/ban4$ git clone "ssh://bandit27-git@localhost/home/bandit27-git/repo"
bandit27@bandit:/tmp/ban4$ ls
bandit27@bandit:/tmp/ban4$ cd repo/
bandit27@bandit:/tmp/ban4/repo$ ls
bandit27@bandit:/tmp/ban4/repo$ cat README
```

Password:    *0ef186ac70e04ea33b4c1853d2526fa2*

---

**Level 28 --> 29**

> **Level Goal**
>
>There is a git repository at ssh://bandit28-git@localhost/home/bandit28-git/repo. The password for the user bandit28-git is the same as for the user bandit28.

>Clone the repository and find the password for the next level.

```console
bandit28@bandit:~$ mkdir /tmp/ban5
bandit28@bandit:~$ cd /tmp/ban5
bandit28@bandit:/tmp/ban5$ git clone "ssh://bandit28-git@localhost/home/bandit28-git/repo"
bandit28@bandit:/tmp/ban4$ ls
bandit28@bandit:/tmp/ban4$ cd repo/
bandit28@bandit:/tmp/ban4/repo$ ls
bandit28@bandit:/tmp/ban4/repo$ cat README
bandit28@bandit:/tmp/ban4/repo$ git show c086d11a00c0648d095d04c089786efef5e01264
```

Password:    *bbc96594b4e001778eee9975372716b2*

---

**Level 29 --> 30**

> **Level Goal**
>
>There is a git repository at ssh://bandit29-git@localhost/home/bandit29-git/repo. The password for the user bandit29-git is the same as for the user bandit29.

>Clone the repository and find the password for the next level.

```console
bandit29@bandit:~$ mkdir /tmp/ban5
bandit29@bandit:~$ cd /tmp/ban5
bandit29@bandit:/tmp/ban5$ git clone "ssh://bandit29-git@localhost/home/bandit29-git/repo"
bandit29@bandit:/tmp/ban5$ ls
repo
bandit29@bandit:/tmp/ban5$ cd repo
bandit29@bandit:/tmp/ban5/repo$ ls
README.md
bandit29@bandit:/tmp/ban5/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/ban5/repo$ git log
bandit29@bandit:/tmp/ban5/repo$ git branch -a
bandit29@bandit:/tmp/ban5/repo$ git checkout remotes/origin/dev
bandit29@bandit:/tmp/ban5/repo$ git log
bandit29@bandit:/tmp/ban5/repo$ git show 
bc833286fca18a3948aec989f7025e23ffc16c07
```

Password:    *5b90576bedb2cc04c86a9e924ce42faf*

---

**Level 30 --> 31**

> **Level Goal**
>
>There is a git repository at ssh://bandit30-git@localhost/home/bandit30-git/repo. The password for the user bandit30-git is the same as for the user bandit30.

>Clone the repository and find the password for the next level.

```console
bandit30@bandit:~$ mkdir /tmp/ban6
bandit30@bandit:~$ cd /tmp/ban6
bandit30@bandit:/tmp/ban6$ git clone "ssh://bandit30-git@localhost/home/bandit30-git/repo"
bandit30@bandit:/tmp/ban6$ ls
repo
bandit30@bandit:/tmp/ban6$ cd repo
bandit30@bandit:/tmp/ban6/repo$ ls
README.md
bandit30@bandit:/tmp/ban6/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/ban6/repo$ git log
commit 3aefa229469b7ba1cc08203e5d8fa299354c496b
Author: Ben Dover <noone@overthewire.org>
Date:   Thu May 7 20:14:54 2020 +0200

    initial commit of README.md
bandit30@bandit:/tmp/ban6/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
bandit30@bandit:/tmp/ban6/repo$ git reflog
3aefa22 HEAD@{0}: clone: from ssh://bandit30-git@localhost/home/bandit30-git/repo
bandit30@bandit:/tmp/ban6/repo$ ls -a
.  ..  .git  README.md
bandit30@bandit:/tmp/ban6/repo$ cd .git
bandit30@bandit:/tmp/ban6/repo/.git$ ls
branches  config  description  HEAD  hooks  index  info  logs  objects  packed-refs  refs
bandit30@bandit:/tmp/ban6/repo/.git$ cat packed-refs
# pack-refs with: peeled fully-peeled
3aefa229469b7ba1cc08203e5d8fa299354c496b refs/remotes/origin/master
f17132340e8ee6c159e0a4a6bc6f80e1da3b1aea refs/tags/secret
bandit30@bandit:/tmp/ban6/repo/.git$ git show f17132340e8ee6c159e0a4a6bc6f80e1da3b1aea
```

Password:    *5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z*

---

**Level 31 --> 32**

> **Level Goal**
>
>There is a git repository at ssh://bandit31-git@localhost/home/bandit31-git/repo. The password for the user bandit31-git is the same as for the user bandit31.

>Clone the repository and find the password for the next level.

```console
bandit31@bandit:~$ mkdir /tmp/ban7
bandit31@bandit:~$ cd /tmp/ban7
bandit31@bandit:/tmp/ban7$ git clone "ssh://bandit31-git@localhost/home/bandit31-git/repo"
bandit31@bandit:/tmp/ban7$ ls
repo
bandit31@bandit:/tmp/ban7$ cd repo
bandit31@bandit:/tmp/ban7/repo$ ls
README.md
bandit31@bandit:/tmp/ban7/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master
May I come in?
bandit31@bandit:/tmp/ban7/repo$ nano key.txt
bandit31@bandit:/tmp/ban7/repo$ bandit31@bandit:/tmp/ban7/repo$ ls
key.txt  README.md
bandit31@bandit:/tmp/ban7/repo$ git add .
bandit31@bandit:/tmp/ban7/repo$ git commit
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean
bandit31@bandit:/tmp/ban7/repo$ ls -a
.  ..  .git  .gitignore  key.txt  README.md
bandit31@bandit:/tmp/ban7/repo$ git add key.txt -f
bandit31@bandit:/tmp/ban7/repo$ git commit
bandit31@bandit:/tmp/ban7/repo$ git push
```

Password:    *56a9bf19c63d650ce78e6ec0354ee45e*

---