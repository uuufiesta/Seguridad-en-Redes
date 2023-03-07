# Level 9-10

## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de Acceso
ssh bandit9@bandit.labs.overthewire.org -p 2220
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit9@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit9@bandit.labs.overthewire.org's password:
bandit9@bandit:~$ strings data.txt -n 10 | grep "=="
c========== the
h;========== password
========== isT
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
## Notas Adicionales

## Referencias

