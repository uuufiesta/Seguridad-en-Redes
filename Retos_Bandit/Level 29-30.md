# Level 29-30

## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.
## Datos de Acceso
ssh bandit29@bandit.labs.overthewire.org -p 2220
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit29@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit29@bandit.labs.overthewire.org's password:
bandit29@bandit:~$ mkdir /tmp/pari
bandit29@bandit:~$ cd /tmp/pari
bandit29@bandit:/tmp/pari$ git clone ssh://bandit29git@localhost:2220/home/bandit29-git/repo
bandit29@bandit:/tmp/pari$ cd repo
bandit29@bandit:/tmp/pari/repo$ ls
README.md
bandit29@bandit:/tmp/pari/repo$ cat README.md 
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/pari/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/pari/repo$ git diff remotes/origin/dev
diff --git a/README.md b/README.md
index a4b1cf1..1af21d3 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for bandit30 of bandit.
 ## credentials
 
 - username: bandit30
-- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
+- password: <no passwords in production!>
 
diff --git a/code/gif2ascii.py b/code/gif2ascii.py
deleted file mode 100644
index 8b13789..0000000
--- a/code/gif2ascii.py
+++ /dev/null
@@ -1 +0,0 @@
-
```
## Notas Adicionales

## Referencias

