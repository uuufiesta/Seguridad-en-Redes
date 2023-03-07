# Level 7-8

## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos de Acceso
ssh bandit7@bandit.labs.overthewire.org -p 2220
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit7@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit7@bandit.labs.overthewire.org's password:
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
## Notas Adicionales
- grep: filtra la salida a las lineas que coinciden con un patron de texto
## Referencias

