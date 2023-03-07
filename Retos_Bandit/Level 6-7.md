# Level 6-7

## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size
## Datos de Acceso
ssh bandit6@bandit.labs.overthewire.org -p 2220
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit6@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit6@bandit.labs.overthewire.org's password:
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
## Notas Adicionales
- -user: Patron de busqueda que indica el usuario al que pertenece el archivo
- -group: Parton de busqueda que indica el grupo al que pertenece el archivo
- 2>/dev/null: Envia los errores del comando al dispositivo null, por lo que no se mostrarán en pantalla
- / : Indica a find iniciar la busqueda desde la raiz
## Referencias

