# Level 15-16

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.
## Datos de Acceso
ssh bandit15@bandit.labs.overthewire.org -p 2220
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit15@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit15@bandit.labs.overthewire.org's password:
bandit15@bandit:~$ openssl s_client -connect localhost:30001
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1
```
## Notas Adicionales

## Referencias

