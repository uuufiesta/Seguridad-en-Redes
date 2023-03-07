# Level 5-6

## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

-   human-readable
-   1033 bytes in size
-   not executable
## Datos de Acceso
ssh bandit5@bandit.labs.overthewire.org -p 2220
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit5@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit5@bandit.labs.overthewire.org's password:
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ find -readable -size 1033c -type f
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
## Notas Adicionales
- find: Busca archivos en el sistema
- -readable: Patron de busqueda que indica que tiene que ser un archivo legible
- -size: Patron de busqueda que indica que tiene que tener cierto tamaño
- -type: Patron de busqueda que indica el tipo de archivo que tiene que ser
## Referencias

