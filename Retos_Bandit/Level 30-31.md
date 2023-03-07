# Level 30-31

## Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.
## Datos de Acceso
ssh bandit30@bandit.labs.overthewire.org -p 2220
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit30@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit30@bandit.labs.overthewire.org's password:
bandit30@bandit:~$ mkdir /tmp/pari
bandit30@bandit:~$ cd /tmp/pari
bandit30@bandit:/tmp/pari$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
bandit30@bandit:/tmp/pari$ cd repo/
bandit30@bandit:/tmp/pari/repo$ ls -la
total 16
drwxrwxr-x 3 bandit30 bandit30 4096 Mar  5 22:32 .
drwxrwxr-x 3 bandit30 bandit30 4096 Mar  5 22:32 ..
drwxrwxr-x 8 bandit30 bandit30 4096 Mar  5 22:32 .git
-rw-rw-r-- 1 bandit30 bandit30   30 Mar  5 22:32 README.md
bandit30@bandit:/tmp/pari/repo$ cat README.md 
just an epmty file... muahaha
bandit30@bandit:/tmp/pari/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```
## Notas Adicionales

## Referencias

