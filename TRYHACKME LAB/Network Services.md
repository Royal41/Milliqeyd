# SMB nədir?

SMB - Server Message Block Protocol - şəbəkədəki fayllara, printerlərə, serial portlara və digər resurslara girişi bölüşmək üçün istifadə olunan müştəri-server (client-server)  rabitə protokoludur.

Serverlər fayl sistemlərini və digər resursları (printerlər, adlandırılmış borular, API) şəbəkədəki müştərilər üçün əlçatan edir. 
Müştəri kompüterlərinin öz sabit diskləri ola bilər, lakin onlar da serverlərdə paylaşılan fayl sistemlərinə və printerlərə daxil olmaq istəyirlər.

SMB protokolu cavab sorğusu protokolu kimi tanınır, yəni əlaqə yaratmaq üçün müştəri və server arasında çoxlu mesaj ötürməsi deməkdir. 
Müştərilər serverlərə TCP/IP (əslində RFC1001 və RFC1002-də göstərildiyi kimi TCP/IP üzərindən NetBIOS), NetBEUI və ya IPX/SPX istifadə edərək qoşulur.


![image](https://github.com/Royal41/Milliqeyd/assets/157361440/e677a13f-f1cc-46af-9721-eabca233653f)


Bir əlaqə qurduqdan sonra müştərilər serverə paylaşımlara daxil olmaq, faylları açmaq, 
faylları oxumaq və yazmaq və ümumiyyətlə fayl sistemi ilə etmək istədiyiniz hər cür şeyi etməyə imkan verən əmrlər (SMB) göndərə bilərlər. 
Bununla belə, SMB vəziyyətində bu işlər şəbəkə üzərindən edilir.

-------

# SMB-ni nə idarə edir?

Windows 95-dən bəri Microsoft Windows əməliyyat sistemləri müştəri və server SMB protokol dəstəyini daxil etmişdir. 
SMB protokolunu dəstəkləyən açıq mənbə serveri Samba Unix sistemləri üçün buraxılmışdır.

SMB hansı protokol növüdür?

SMB protokolu cavab sorğusu protokolu kimi tanınır, yəni əlaqə yaratmaq üçün müştəri və server arasında çoxlu mesaj ötürməsi deməkdir.

Cavab: cavab/sorğu (response/request)

-----------
# Enumerating SMB -(SMB Sadalama)

Enumeration-potensial hücum vektorlarını tapmaq və istismara kömək etmək üçün hədəf haqqında məlumat toplamaq prosesidir.
Bu proses hücumun uğurlu olması üçün vacibdir, çünki ya işləməyən, ya da sistemi çökdürə biləcək istismarlarla vaxt itirmək enerji itkisi ola bilər. Enumaration istifadəçi adlarını, parolları, şəbəkə məlumatlarını, host adlarını, proqram məlumatlarını, xidmətləri və ya Attacker üçün dəyərli ola biləcək hər hansı digər məlumatları toplamaq üçün istifadə edilə bilər.

------------
# SMB

Tipik olaraq, serverdə faylları görmək və ya ötürmək üçün qoşula və istifadə edilə bilən SMB paylaşma diskləri var. 
SMB çox vaxt həssas məlumatları kəşf etmək istəyən təcavüzkar üçün əla başlanğıc nöqtəsi ola bilər – bəzən bu paylaşımlara nə daxil olduğuna təəccüblənərsiniz. 

-----------

# Port Skanlama (Port Skanining)

Enumeration ilk addımı, hədəf maşının xidmətləri, tətbiqləri, strukturu və əməliyyat sistemi haqqında mümkün qədər çox məlumat tapmaq üçün port taraması aparmaqdır.
Əgər port skanına hələ baxmamısınızsa, mən burada Nmap otağına baxmağı məsləhət görürəm

-----

# Enum4Linux

Enum4linux həm Windows, həm də Linux sistemlərində SMB paylarını sadalamaq üçün istifadə edilən bir vasitədir. Bu, əsasən Samba paketindəki alətlər ətrafında bir sarğıdır və SMB ilə əlaqəli hədəfdən məlumatı tez çıxarmağı asanlaşdırır. O, standart olaraq Parrot və Kali-də quraşdırılıb, lakin onu quraşdırmaq lazımdırsa, bunu rəsmi github- dan edə bilərsiniz .


Enum4Linux-un sintaksisi gözəl və sadədir: 
      "enum4linux [seçimlər] ip"

ETİKET             FUNKSİYASI

-U istifadəçi siyahısını əldə edir
-M maşın siyahısını əldə edir
-N ad siyahısı zibilini əldə edir (-U və-M-dən fərqli)
-S paylaşma siyahısını əldə edir
-P parol siyasəti məlumatını alır
-G qrup və üzv siyahısını alır

-----

