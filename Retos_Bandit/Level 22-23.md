# Level 22-23

## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.
## Datos de Acceso
ssh bandit22@bandit.labs.overthewire.org -p 2220
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit22@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit22@bandit.labs.overthewire.org's password:
bandit22@bandit:~$ ls /etc/cron.d
cronjob_bandit15_root  cronjob_bandit23       e2scrub_all
cronjob_bandit17_root  cronjob_bandit24       otw-tmp-dir
cronjob_bandit22       cronjob_bandit25_root  sysstat
bandit22@bandit:~$ cat /etc/cron.d/cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:~$ whoami
bandit22
bandit22@bandit:~$ myname=bandit23
bandit22@bandit:~$ echo $(echo I am user $myname | md5sum | cut -d ' ' -f 1)
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
```
## Notas Adicionales

## Referencias

