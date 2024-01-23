 ## privilege escalation nedir?

 
Əsas odur ki, Privilege Eskalasiyası adətən daha aşağı icazə hesabından daha yüksək icazəli hesaba keçidi əhatə edir. Daha texniki cəhətdən bu, adətən istifadəçilər tərəfindən məhdudlaşdırılan resurslara icazəsiz giriş əldə etmək üçün əməliyyat sistemində və ya tətbiqdə zəifliyin, dizayn qüsurunun və ya konfiqurasiyaya nəzarətin istismarıdır.

 ##  (Sadalama)- nedir?
  #Enumeration hər hansı bir sistemə daxil olduqdan sonra atmalı olduğunuz ilk addımdır. Siz root səviyyəli girişlə nəticələnən kritik zəiflikdən istifadə etməklə sistemə daxil olmuş ola bilərsiniz və ya sadəcə olaraq aşağı imtiyazlı hesabdan istifadə edərək əmrlər göndərməyin yolunu tapmış ola bilərsiniz.


 ## hostname

  # Komanda hostname hədəf maşının host adını qaytaracaq.

 ## uname -a
  
  #Sistem tərəfindən istifadə edilən kernel haqqında bizə əlavə təfərrüat verən sistem məlumatını çap edəc

 ## /proc/version

 #Proc fayl sistemi (procfs) hədəf sistem prosesləri haqqında məlumat verir.

  #Linux version 5.4.0-91-generic (builddate@lgw01-amd64-044) (gcc version 9.3.0 (Ubuntu 9.3.0-17ubuntu1~20.04)) #102-Ubuntu SMP Fri Apr 16 12:43:43 UTC 2021

##/etc/issue

 /etc/issue. Bu fayl adətən əməliyyat sistemi haqqında bəzi məlumatları ehtiva edir, lakin asanlıqla fərdiləşdirilə və ya dəyişdirilə bilər. 

## ps əmri

#Komanda ps Linux sistemində işləyən prosesləri görmək üçün effektiv bir yoldur. ps Terminalınıza yazmaq cari qabıq üçün prosesləri göstərəcək.

(Proses Vəziyyəti) çıxışı ps aşağıdakıları göstərəcək;

PID: Proses identifikatoru (proses üçün unikal)
TTY: İstifadəçi tərəfindən istifadə edilən terminal növü
Vaxt: Proses tərəfindən istifadə edilən CPU vaxtının miqdarı (bu prosesin işlədiyi vaxt DEYİL)
CMD: Əmr və ya icra edilə bilən işləmə (heç bir komanda xətti parametrini GÖSTERMƏYƏCƏK)


"PS" əmri bir neçə faydalı seçim təqdim edir.  

ps -A: Bütün çalışan proseslərə baxın
ps axjfps axjf: Proses ağacına baxın ( aşağıda işləyənə qədər ağacın formalaşmasına baxın )


ps aux: aux Seçim bütün istifadəçilər üçün prosesləri göstərəcək (a), prosesi başlatmış istifadəçini göstərəcək (u) və terminala qoşulmayan prosesləri göstərəcək (x). 

## suid emri ile getcap in ferqi(getcap= capability)

ferqi odur ki suid daha tehlukelidir cunki suid verdikde ister yazmaq ister silmek istersede edit etmek funk olur .
ama ki getcap da ise ne isteyirikse onuda vere bilerik misal olaraq ister read isterse writter isterse executue ede bilerik yeni sahib ne verirse onuda goturur



## env
 #Komanda env ətraf mühitin dəyişənlərini göstərəcək.

 PATH dəyişəninin kompilyatoru və ya skript dili (məsələn, Python) ola bilər ki, bu da hədəf sistemdə kodu işlətmək üçün istifadə edilə bilər və ya imtiyazların artırılması üçün istifadə edilə bilər.


## İd
#Komanda id istifadəçinin imtiyaz səviyyəsi və qrup üzvlükləri haqqında ümumi məlumat verəcəkdir.


Yadda saxlamaq lazımdır ki, id əmr aşağıda göstərildiyi kimi başqa bir istifadəçi üçün eyni məlumatı əldə etmək üçün də istifadə edilə bilər.

id root ve ya id sadece


## netstat
Mövcud interfeyslər və şəbəkə marşrutları üçün ilkin yoxlamadan sonra mövcud kommunikasiyalara nəzər salmağa dəyər. Komanda netstatmövcud əlaqələr haqqında məlumat toplamaq üçün bir neçə fərqli seçimlə istifadə edilə bilər.


netstat -a: bütün dinləmə portlarını və qurulmuş əlaqələri göstərir.
netstat -atvə ya netstat -aumüvafiq olaraq TCP və ya UDP protokollarını siyahıya almaq üçün istifadə edilə bilər.
netstat -l: “dinləmə” rejimində portların siyahısı. Bu portlar açıqdır və daxil olan əlaqələri qəbul etməyə hazırdır.

##netstat -s: 
şəbəkədən istifadə statistikasını protokolla sıralayın (aşağıda) Bu, həmçinin  çıxışı xüsusi protokola məhdudlaşdırmaq üçün -t və ya seçimləri ilə də istifadə edilə bilər.-u

## find Command

Faylları tapın:

find . -name flag1.txt: cari kataloqda “flag1.txt” adlı faylı tapın
find /home -name flag1.txt: /home qovluğunda “flag1.txt” fayl adlarını tapın
find / -type d -name config: “/” altında config adlı qovluğu tapın
find / -type f -perm 0777: 777 icazəsi olan faylları tapın (bütün istifadəçilər tərəfindən oxuna bilən, yazıla bilən və icra edilə bilən fayllar)
find / -perm a=x: icra edilə bilən faylları tapın
find /home -user frank: “/home” altında “frank” istifadəçisi üçün bütün faylları tapın
find / -mtime 10: son 10 gündə dəyişdirilmiş faylları tapın
find / -atime 10: son 10 gündə daxil olmuş faylları tapın
find / -cmin -60: son bir saat ərzində dəyişdirilmiş faylları tapın (60 dəqiqə)
find / -amin -60: son bir saat ərzində fayllara girişi tapın (60 dəqiqə)
find / -size 50M: 50 MB ölçüsündə faylları tapın

