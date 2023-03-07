# Level 17-18

## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**
## Datos de Acceso
ssh bandit17@bandit.labs.overthewire.org -p 2220
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit17@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit17@bandit.labs.overthewire.org's password:
bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< f9wS9ZUDvZoo3PooHgYuuWdawDFvGld2
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
```
## Notas Adicionales
diff: Nos encuentra las diferencias entre 2 documentos
## Referencias

