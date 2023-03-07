# Level 25-26

## Objetivo
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.
## Datos de Acceso
ssh bandit25@bandit.labs.overthewire.org -p 2220
p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
## Solución
``` bash
C:\WINDOWS\system32>ssh bandit25@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit25@bandit.labs.overthewire.org's password:
bandit25@bandit:~$  ssh -i bandit26.sshkey bandit26@localhost -p 2220
:e /etc/bandit_pass/bandit26
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```
## Notas Adicionales

## Referencias

