# MAC spoofing-(  )


MAC spoofing, bir şəbəkə cihazının (əsasən bir kompüterin və ya şəbəkə interfeys kartının) fiziki ünvanını (MAC ünvanı da deyilir) sahte bir ünvanla əvəzləmə prosesidir. MAC ünvanı, şəbəkə cihazlarının unikal kimlik nömrəsidir və əsasən digər cihazlarla əlaqə qurarkən istifadə olunur.

MAC spoofing, əsasən şəbəkədəki izləmə və ya izlənmə fəaliyyətlərini gizlətmək, foydalanıcı məlumatlarına qulluq etmə hücumları törətmək və ya şəbəkəyə icazəsiz daxil olmaq kimi məqsədlərlə istifadə oluna bilər. Bir hücumçı, sahte bir MAC ünvanı istifadə edərək şəbəkə trafikini izləyə, bloklamağa və ya icazəsiz bir cihaz kimi görünməyə çalışa bilər.

Bu cür hücumlara qarşı qorunmaq üçün, şəbəkə idarəçiləri əsasən MAC ünvanı filtrələmə, port təhlükəsizliyi və şəbəkə izləmə kimi təhlükəsizlik tədbirlərindən istifadə edirlər. Ancaq, mürəkkəb bir şəbəkədə, MAC spoofing əleyhinə tam qorunma təmin etmək çətin ola bilər.


# Qeyd:

Şəbəkə daxilində MAC ünvanlarının saxtalaşdırılmasının qarşısını almaq üçün şəbəkə təhlükəsizliyi mütəxəssisləri Cisco IOS Switch-lərdə Dinamik ARP Təftişini (DAI) tətbiq edə bilərlər .




# Təsadüfi MAC ünvanı yaratmaq və interfeysə təyin etmək üçün aşağıdakıları etməliyik:

1.Komandanı istifadə edərək interfeysi məntiqi olaraq aşağı salın ifconfig wlan0 down

		root@kali;~# ifconfig wlan0 down



2.Komandadan istifadə edərək göstərilən interfeysdə cari və daimi MAC ünvanlarını yoxlayın 
		
		root@kali;~# macchanger –-show wlan0 


3.macchanger --random wlan0MAC yaratmaq və interfeysimizə təyin etmək üçün əmrdən istifadə edin wlan0:

		root@kali;~# macchanger --random wlan0


4.Komanda istifadə edərək interfeysi yenidən aktivləşdirin ifconfig wlan0 up:

		root@kali;~# ifconfig wlan0 up


# Qeyd
macchanger –-helpBundan əlavə, bütün mövcud variantları görmək üçün əmrdən istifadə edə bilərsiniz .


# Windows 10-da MAC spoofing:

Windows 10-da fiziki ünvanı dəyişdirin və əvvəlki versiya olduqca asandır. Növbəti addıma keçməzdən əvvəl sizə deyəcəm Windows 10-da MAC ünvanını necə yoxlamaq olar? 

1.--CMD (əmr əmri) açın və aşağıdakı əmri yerinə yetirin--

		ipconfig / all


2: Press Windows Key + X on the keyboard and click on network connections.

3: Choose an adapter and right-click on it, then click on properties.

4: Click on Configure 

5.A new window will be popup, click on the Advanced tab

Select Network address property in left-hand side property bar
(Yeni bir pəncərə açılacaq, Qabaqcıl sekmesini vurun

Sol tərəfdəki xüsusiyyət panelində Şəbəkə ünvanı xüsusiyyətini seçin)

6.Check on Value and fill in the new MAC address value. and click on OK.

7.So check again MAC address by using the same command ipconfig /all



# Qeyd: 
Bu müvəqqəti MAC saxtakarlığıdır, ona görə də orijinal Fiziki ünvanınızı əldə etmək istəyirsinizsə, sadəcə tərs prosesdən istifadə edin
