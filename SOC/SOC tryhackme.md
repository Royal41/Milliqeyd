SOC:

Təhlükəsizlik Əməliyyatları Mərkəzi ( SOC )

## Təhlükəsizlik Əməliyyatları Mərkəzi ( SOC ) zərərli kibertəhlükəsizlik hadisələrini aşkar etmək üçün şəbəkəni və onun sistemlərini izləyən kibertəhlükəsizlik mütəxəssisləri komandasıdır.

 # SOC üçün əsas maraq sahələrindən bəziləri bunlardır:

1) Zəifliklər ( Vulnerabilities ): Sistem zəifliyi (zəifliyi) aşkar edildikdə, müvafiq yeniləmə və ya yamaq quraşdırmaqla onu aradan qaldırmaq vacibdir. 
Düzəliş mövcud olmadıqda, təcavüzkarın ondan istifadə etməsinin qarşısını almaq üçün lazımi tədbirlər görülməlidir. 
Zəifliklərin aradan qaldırılması SOC üçün həyati maraq kəsb etsə də , bu, mütləq onlara həvalə edilmir.

2)Siyasət pozuntuları ( Policy violations ): Biz təhlükəsizlik siyasətini şəbəkə və sistemlərin qorunması üçün tələb olunan qaydalar toplusu kimi düşünə bilərik. 
Məsələn, istifadəçilər məxfi şirkət məlumatlarını onlayn saxlama xidmətinə yükləməyə başlayarsa, bu, siyasətin pozulması ola bilər.

3)İcazəsiz fəaliyyət ( Unauthorized activity ): İstifadəçinin giriş adı və parolunun oğurlandığı və təcavüzkarın onlardan şəbəkəyə daxil olmaq üçün istifadə etdiyi halı nəzərdən keçirək. 
SOC belə bir hadisəni aşkar etməli və daha çox zərər görməzdən əvvəl onu mümkün qədər tez bloklamalıdır .

4)Şəbəkə müdaxilələri ( Network intrusions ): Təhlükəsizliyiniz nə qədər yaxşı olsa da, hər zaman müdaxilə şansı var. 
İstifadəçi zərərli linkə kliklədikdə və ya təcavüzkar ictimai serverdən istifadə etdikdə müdaxilə baş verə bilər.
 İstənilən halda, müdaxilə baş verdikdə, daha çox zərərin qarşısını almaq üçün onu mümkün qədər tez aşkar etməliyik.

------------------

# Rəqəmsal Məhkəmə Ekspertizası və İnsidentlərə Cavab ( Digital Forensics and Incident Response )  ( DFIR ):

Bu bölmə Rəqəmsal Məhkəmə Ekspertizası və İnsident Cavab ( DFIR ) haqqındadır və biz:

1.Rəqəmsal Məhkəmə
2.Hadisəyə cavab
3.Zərərli proqramların təhlili

--------------------

---# Rəqəmsal Məhkəmə

Məhkəmə ekspertizası cinayətləri araşdırmaq və faktları müəyyən etmək üçün elmin tətbiqidir. Kompüterlər və smartfonlar kimi rəqəmsal sistemlərin istifadəsi və yayılması ilə əlaqədar cinayətləri araşdırmaq üçün məhkəmə ekspertizasının yeni bir qolu yarandı: sonradan rəqəmsal məhkəmə ekspertizasına çevrilən kompüter kriminalistikası .

Müdafiə təhlükəsizliyində rəqəmsal məhkəmə ekspertizasının diqqəti hücum və onun icraçıları və əqli mülkiyyət oğurluğu, 
kibercasusluq və icazəsiz məzmuna sahiblik kimi digər sahələrin dəlillərinin təhlilinə keçir. 
Nəticə etibarilə, rəqəmsal məhkəmə ekspertizası müxtəlif sahələrə diqqət yetirəcək, məsələn:

1.Fayl Sistemi: Sistem yaddaşının rəqəmsal məhkəmə ekspertizasının təsvirini (aşağı səviyyəli surəti) təhlil etmək, quraşdırılmış proqramlar, yaradılmış fayllar, qismən üzərinə yazılmış fayllar və silinmiş fayllar kimi bir çox məlumatı aşkar edir.
2.Sistem yaddaşı: Təcavüzkar öz zərərli proqramını yaddaşda diskdə saxlamadan işlədirsə, 

sistem yaddaşının məhkəmə təsvirini (aşağı səviyyəli surəti) götürmək onun məzmununu təhlil etmək və hücum haqqında öyrənmək üçün ən yaxşı yoldur.
3.Sistem qeydləri: Hər bir müştəri və server kompüterində baş verənlər haqqında müxtəlif log faylları saxlanılır.
 Log faylları sistemdə baş verənlər haqqında çoxlu məlumat verir.
 Təcavüzkar izlərini təmizləməyə çalışsa belə, bəzi izlər qalacaq.
4.Şəbəkə qeydləri: Şəbəkəni keçən şəbəkə paketlərinin qeydləri hücumun baş verib-verməməsi və bunun nə ilə nəticələndiyi ilə bağlı daha çox suallara cavab verməyə kömək edəcək.


----------

---# Hadisəyə cavab ( Incident Response ):

İnsident adətən məlumatların pozulmasına və ya kiberhücuma aiddir; lakin bəzi hallarda səhv konfiqurasiya, müdaxilə cəhdi və ya siyasətin pozulması kimi daha az kritik bir şey ola bilər. 

Kiberhücuma misal olaraq şəbəkəmizi və ya sistemlərimizi əlçatmaz edən təcavüzkar, ictimai vebsaytı pozmaq (dəyişdirmək) və məlumatların pozulması (şirkət məlumatlarının oğurlanması) daxildir. 

Kiberhücuma necə cavab verərdiniz ? İnsident cavabı belə bir işi idarə etmək üçün izlənilməli olan metodologiyanı müəyyən edir. 

Məqsəd zərəri azaltmaq və mümkün olan ən qısa müddətdə bərpa etməkdir. İdeal olaraq, hadisəyə cavab verməyə hazır bir plan hazırlayacaqsınız.


# Hadisəyə cavab prosesinin dörd əsas mərhələsi bunlardır:

1) Hazırlıq: Bunun üçün təlim keçmiş və insidentləri idarə etməyə hazır komanda tələb olunur. İdeal olaraq, ilk növbədə hadisələrin qarşısını almaq üçün müxtəlif tədbirlər görülür.

2)Aşkarlama və Təhlil: Komanda hər hansı hadisəni aşkar etmək üçün lazımi resurslara malikdir; üstəlik, onun şiddətini öyrənmək üçün aşkar edilmiş hər hansı hadisəni əlavə təhlil etmək vacibdir.

3)Saxlama, Silinmə və Bərpa: Hadisə aşkar edildikdən sonra onun digər sistemlərə təsirini dayandırmaq, onu aradan qaldırmaq və təsirlənmiş sistemləri bərpa etmək çox vacibdir. 
Məsələn, bir sistemin kompüter virusu ilə yoluxduğunu gördükdə, virusun digər sistemlərə yayılmasını dayandırmaq (tutmaq), virusu təmizləmək (kök etmək) və sistemin düzgün bərpasını təmin etmək istərdik.

4)Hadisədən sonrakı fəaliyyət: Uğurlu bərpa edildikdən sonra hesabat hazırlanır və gələcək oxşar hadisələrin qarşısını almaq üçün öyrənilən dərs paylaşılır.

![image](https://github.com/Royal41/Milliqeyd/assets/157361440/71c1d3b1-2caa-42d6-a85c-266ce9e465c3)

--------

---# Zərərli proqramların təhlili(Malware Analysis):

Zərərli proqram zərərli proqram deməkdir. Proqram təminatı diskdə saxlaya və ya şəbəkə vasitəsilə göndərə biləcəyiniz proqramlara, sənədlərə və fayllara aiddir. Zərərli proqram bir çox növləri əhatə edir, məsələn:

1)Virus özünü proqrama bağlayan kod parçasıdır (proqramın bir hissəsidir).
Bir kompüterdən digərinə yayılmaq üçün nəzərdə tutulmuşdur; üstəlik, kompüterə yoluxduqdan sonra faylları dəyişdirmək, üzərinə yazmaq və silməklə işləyir. 
Nəticə kompüterin yavaşlamasından tutmuş istifadəyə yararsız hala çevrilir.

2)Trojan Horse bir arzu olunan funksiyanı göstərən, lakin onun altında zərərli funksiyanı gizlədən proqramdır. 
Məsələn, qurban, təcavüzkarın sistemi üzərində tam nəzarəti təmin edən kölgəli veb saytdan video pleyer yükləyə bilər.

3)Ransomware istifadəçi fayllarını şifrələyən zərərli proqramdır. Şifrələmə şifrələmə parolunu bilmədən faylları oxunmaz edir.
Təcavüzkar istifadəçi “fidyə” ödəməyə hazırdırsa, istifadəçiyə şifrələmə parolunu təklif edir.

![image](https://github.com/Royal41/Milliqeyd/assets/157361440/7e8f3160-55ab-4cac-9df7-48cea6714fd4)


Zərərli proqramların təhlili müxtəlif vasitələrdən istifadə edərək bu cür zərərli proqramlar haqqında öyrənmək məqsədi daşıyır:

1)Statik analiz zərərli proqramı işə salmadan yoxlayaraq işləyir. 
Adətən, bunun üçün montaj dili (prosessorun təlimat dəsti, yəni kompüterin fundamental təlimatları) üzrə möhkəm bilik tələb olunur.

2)Dinamik analiz zərərli proqramı idarə olunan mühitdə işlətməklə və onun fəaliyyətinə nəzarət etməklə işləyir. 
Bu, zərərli proqramın işləyərkən necə davrandığını müşahidə etməyə imkan verir.


