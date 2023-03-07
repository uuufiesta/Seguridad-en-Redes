# Level 18-19

## Objetivo
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.
## Datos de Acceso
ssh bandit18@bandit.labs.overthewire.org -p 2220
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
## Solución
``` bash
C:\Users\SKU 1084303565\Documents\Universidad\8vo Semestre\Seguridad en redes de internet>ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```
## Notas Adicionales

## Referencias

