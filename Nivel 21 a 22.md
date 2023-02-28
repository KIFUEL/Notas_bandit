## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** Try connecting to your own network daemon to see if it works as you think
## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit21**
ssh:  bandit21@bandit.labs.overthewire.org -p 2220
password: **NvEJF7oVjkddltPSrdKEFOllh9V1IBcq**
## Solución

``` bash
bandit21@bandit:~$
bandit21@bandit:~$ ls -la /etc/cron.d
total 56
drwxr-xr-x   2 root root  4096 Feb 21 22:04 .
drwxr-xr-x 108 root root 12288 Feb 21 22:04 ..
-rw-r--r--   1 root root    62 Feb 21 22:02 cronjob_bandit15_root
-rw-r--r--   1 root root    62 Feb 21 22:02 cronjob_bandit17_root
-rw-r--r--   1 root root   120 Feb 21 22:03 cronjob_bandit22
-rw-r--r--   1 root root   122 Feb 21 22:03 cronjob_bandit23
-rw-r--r--   1 root root   120 Feb 21 22:03 cronjob_bandit24
-rw-r--r--   1 root root    62 Feb 21 22:03 cronjob_bandit25_root
-rw-r--r--   1 root root   201 Jan  8  2022 e2scrub_all
-rwx------   1 root root    52 Feb 21 22:04 otw-tmp-dir
-rw-r--r--   1 root root   102 Mar 23  2022 .placeholder
-rw-r--r--   1 root root   396 Feb  2  2021 sysstat

bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat /tmp//t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
bandit21@bandit:~$

```

## Notas Adicionales


password: **WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff**


## Referencias