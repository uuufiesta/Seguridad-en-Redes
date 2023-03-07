# Level 8-9

## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de Acceso
ssh bandit8@bandit.labs.overthewire.org -p 2220
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit8@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit8@bandit.labs.overthewire.org's password:
bandit8@bandit:~$ sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
## Notas Adicionales
- sort: ordena las lineas de texto
- uniq: filtra los repetidos, cuenta los repetidos, filtra los unicos
- -c: cuenta los repetidos
- -d: muestra solo los repetidos
- -u: muestra solo los unicos
## Referencias

