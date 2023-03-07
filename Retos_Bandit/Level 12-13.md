# Level 12-13

## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de Acceso
ssh bandit12@bandit.labs.overthewire.org -p 2220
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit12@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit12@bandit.labs.overthewire.org's password:
bandit12@bandit:~$ cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
## Notas Adicionales

## Referencias

