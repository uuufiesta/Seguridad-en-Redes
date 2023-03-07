# Level 16-17

## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de Acceso
ssh bandit16@bandit.labs.overthewire.org -p 2220
JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit16@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit16@bandit.labs.overthewire.org's password:
bandit16@bandit:~$ nmap localhost -p 31000-32000
Starting Nmap 7.80 ( https://nmap.org ) at 2023-03-06 03:34 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.000098s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.07 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Mar  4 13:56:53 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Mar  4 13:56:53 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Mar  4 13:55:53 2023 GMT; NotAfter: Mar  4 13:56:53 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEQqZ5JDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMzA0MTM1NTUzWhcNMjMwMzA0MTM1NjUzWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC0
dpk5mzBbza2eECYqzO7xdgsCzPEGOubDZkoBQnwnetIfYeDfY+4+ZHr9JMX8aDJy
ke8TvxkWzxgCcuzp2F0X5sc8YCMZRQYiiWVBvKz/J3BpLaVfOaMeQnbQEvmHa/JY
HfjOuc++ejiQu+hAyhgplrY4KbVJ5817nHQyynpPIFN7IgXa63HNQQDYSlR0L0BM
HW34AOIznwOT34d+uoTLBp7zfYi5yNMrZw+WsTsYwZo3QvqJjxSnOBy9Tooz0oc8
kbarZvVS97APia+dhaXWRpupxozDKiENN9x/aWFL2ZYeWJL3hgtNuioPjLuxfayr
AXmpU5DENZfGec1Bt/SrAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQAW
66o9T/rT26TxFbE/d4XNjtI/axzGUKyITLZtrcPa1CDARC0ScmbvA4p6KApKeFrc
5i09sP0dNB55SVKXxTFaMI+uSsu5cbZwq+HKgNXM7hwCuAkTi/lfv1rWEFOuLAm+
SU6prh1EQXKmmxwlmAlFRuuozLVVY866aLoJ9meYTw4kmgSoXH/bOvoOXxXA26U5
hqEmZSRFGHPh7m7TEZP/K/eEuTjVCBC+SRGiAAHuj9Ex1V7VNl6QSuZ+fuMie6d0
QAIaB915UtrinaueP6mI8pxjxJ6g5qAc5STZ/mM1gXZMJ1N1j0N7hO0RgP7RxFxH
YqQE464Y3vKKVybqjJCD
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: F94741E786CF8CD39384891DBE2C5D41AC54BB9C112B5AF31772C6223201240B
    Session-ID-ctx:
    Resumption PSK: A2607D50030946E6F57E4D11588D5644B748DFDCDB333A5A1EA6403275EB2AD6CEE285C82C91BE1D25D776B7B567A677
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 41 ab fb dd 86 d6 53-b7 84 7a 8a d0 a9 25 8b   .A.....S..z...%.
    0010 - 28 7a 18 2c 75 0d 73 7e-43 44 ac 5e c4 c4 22 f7   (z.,u.s~CD.^..".
    0020 - 23 d4 b8 7c 77 7e b3 80-04 dc c4 53 a0 ac 5b 21   #..|w~.....S..[!
    0030 - 9e 82 f9 cb 29 25 28 c4-8c 48 c7 79 ab 71 9c 5c   ....)%(..H.y.q.\
    0040 - 20 f0 88 d9 16 d8 bc a8-04 26 03 63 04 49 0e ef    ........&.c.I..
    0050 - c4 7b 32 b3 14 b9 36 8e-20 36 d4 b7 83 4a a0 3d   .{2...6. 6...J.=
    0060 - 8a 7d b6 d4 e4 f7 e6 64-44 77 d6 19 67 82 97 d2   .}.....dDw..g...
    0070 - 8e c0 3d 1b 80 e7 25 39-cb 4a 65 82 d0 9e 7b ad   ..=...%9.Je...{.
    0080 - f8 79 28 7a 06 72 12 dc-34 cd cd 27 32 3f 7b 6a   .y(z.r..4..'2?{j
    0090 - cd f4 2d 93 07 56 92 4a-2b 3a 07 a4 f3 24 84 dc   ..-..V.J+:...$..
    00a0 - af 1a 76 12 26 f8 d9 79-65 f0 91 b8 28 3e 4d 91   ..v.&..ye...(>M.
    00b0 - c6 63 e7 d7 c3 cf 9a 7a-51 7f 07 96 51 e7 bc 63   .c.....zQ...Q..c
    00c0 - ef 4d 58 45 df 7b 24 95-ed 91 7d 96 68 19 cc 3a   .MXE.{$...}.h..:

    Start Time: 1678074021
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: F0C136C35AA83E340EB54FA212B9DFC6FEFA2AFC7578BC0875900A7D3813DE76
    Session-ID-ctx:
    Resumption PSK: 803CED1748E5233A88511AC490B03753C81440824B5FC0496322EE808B2AEBF21FB5BC70F73399849BB837450B4301FA
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 41 ab fb dd 86 d6 53-b7 84 7a 8a d0 a9 25 8b   .A.....S..z...%.
    0010 - 48 37 2e af 06 12 9a 98-25 95 03 05 7b 42 fb 75   H7......%...{B.u
    0020 - 18 3a 73 25 d3 45 a8 84-40 da 9f f2 ec 50 c9 44   .:s%.E..@....P.D
    0030 - e0 b5 46 25 f4 87 41 72-15 96 62 4a 8d 1c bf 71   ..F%..Ar..bJ...q
    0040 - 83 65 60 88 0e 21 30 82-45 85 16 42 0e cb 0d cb   .e`..!0.E..B....
    0050 - fe ec 58 9e ba 34 70 2c-0a c5 c9 20 d6 7f b6 ce   ..X..4p,... ....
    0060 - d9 07 af 1d c4 e8 b0 2f-ad 06 56 1d 0a 99 e1 e6   ......./..V.....
    0070 - b0 a0 db 0d 97 c3 1e b6-e1 b1 c6 fc 2c db 6a 2e   ............,.j.
    0080 - c6 35 92 9c 9a 98 1c d3-11 7d 0c 54 21 80 e5 0d   .5.......}.T!...
    0090 - 6b 37 42 fc f7 40 91 84-25 2e f5 0f ea ff 5a a9   k7B..@..%.....Z.
    00a0 - 30 c3 25 6c 74 a3 fc ff-3d da e6 fe 08 56 ac 80   0.%lt...=....V..
    00b0 - 11 8a 7d a6 f5 b3 e1 27-f7 14 82 38 ac db 4f 48   ..}....'...8..OH
    00c0 - a6 71 5f 8a 27 f9 d2 75-0f 9a 79 23 bb b9 82 7a   .q_.'..u..y#...z

    Start Time: 1678074021
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
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

closed
bandit16@bandit:~$ exit
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
```
## Notas Adicionales

## Referencias

