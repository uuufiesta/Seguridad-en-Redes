# Level 1-2

## Objetivo
Find the password reading a dashed file called "-"

## Datos de Acceso
ssh bandit0@bandit.labs.overthewire.org -p 2220
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit1@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit1@bandit.labs.overthewire.org's password:

bandit1@bandit:~$ cat < -
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
## Notas Adicionales
- cat <: Para leer dashed files
## Referencias
