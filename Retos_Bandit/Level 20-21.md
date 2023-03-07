# Level 20-21

## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).
## Datos de Acceso
ssh bandit20@bandit.labs.overthewire.org -p 2220
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit20@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit20@bandit.labs.overthewire.org's password:
bandit20@bandit:~$  nc -lnvp 2000 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 2842846
bandit20@bandit:~$ Listening on 0.0.0.0 2000
./suconnect 2000
Connection received on 127.0.0.1 35588
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
bandit20@bandit:~$ 
[1]+  Done                    nc -lnvp 2000 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
```
## Notas Adicionales

## Referencias

