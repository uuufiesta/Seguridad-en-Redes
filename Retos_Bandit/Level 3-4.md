# Level 3-4

## Objetivo
Find the flag in a file called ".hidden"

## Datos de Acceso
ssh bandit3@bandit.labs.overthewire.org -p 2220
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit3@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit3@bandit.labs.overthewire.org's password:
bandit3@bandit:~$ cd ./inhere
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Jan 11 19:19 .
drwxr-xr-x 3 root    root    4096 Jan 11 19:19 ..
-rw-r----- 1 bandit4 bandit3   33 Jan 11 19:19 .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
## Notas Adicionales
- ls -la: nos permite ver archivos ocultos
## Referencias

