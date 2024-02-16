## MAC Flooding Nedir? Nasıl Önlenir?

#MAC Flooding, en yaygın ağ saldırılarından biridir. Diğer web saldırılarından farklı olarak MAC Flooding, ağdaki herhangi bir host makineye saldırma yöntemi değil, 
ağ anahtarlarına saldırma yöntemidir. 
Ancak saldırının kurbanı ağdaki bir ana bilgisayardır. MAC Flooding’in ne olduğunu ve nasıl önleyebileceğimizi göreceğiz.



# MAC Flooding nedir?


Mac Flooding diğer adıyla “Mac Adres Taşması” saldırı tekniği özet olarak; 
Switch’deki CAM Table (mac adres table/deposu da diyebiliriz.) tablosu sahte MAC adresleriyle doldurarak Switch’de bozulmalara,
karışıklıklara ve en önemlisi paketleri doğru yönlendirememesi sağlanır.(Mac adres tablolarının da bir kapasitesi ve belli bir miktar RAM değeri bulunuyor.)

Daha sonra Switch bu duruma dayanamayıp gelen paketleri spesifik bir adrese değil de tüm makinelere göndermeye başlar. 
Yani Hub yapısına geçer. Hal böyle olunca ağdaki trafiği ve işlemleri diğer makineler dışında saldırgan makineye de gönderir. 
Saldırı devam ettikçe ağdaki cihazların internet trafiğinde yavaşlamalar ve ağa bağlı makinelerde düşüşler yaşanır. 

---Bu saldırı tekniğindeki en önemli kilit noktalar Switch ve Hub’tır.--- 

Bunları detaylı olarak aşağıda inceleyeceğiz.


# MAC FLOODİNG SALDIRISI NASIL YAPILIR?

Mac Flooding saldırılarında bir çok araç kullanılabilir. Bunlar: Yersinia4, Ettercap3, THC Parasite5 ve macof’dur. 
Aralarında en popüler ve kullanımı basit olan macof, Linux dağıtımlarında default olarak geliyor. 


		#macof -h

[-s src] -> Kaynak IP adresi
[-d dst] -> Hedef IP adresi
[-e tha] -> Aranan MAC adresi
[-x sport] -> Kaynak TCP portu
[-y dport] -> Hedef TCP portu
[-i interface] -> Ethernet arayüzü
[-n times] -> Yollanacak paket sayısı



misal ucun :

		# macof -i ens33 -n 1000

-i parametresi ile ağ arayüzümüzü(ens33) belirledik ve -n ile de paket sayısını(1000 adet) belirledik.




# MAC FLOODİNG SALDIRISI ANALİZİ


Mac Flooding saldırılarındaki trafiği Wireshark ile incelersek gözümüze çarpan ilk durumlardan bir tanesi hedef ve kaynak IP adreslerinin sahteliği olacaktır. 
Bu IP’lerin yerel ağdaki IP’ler ile hiçbir bağlantısı gözükmüyor. Bu saldırılardaki paketler bozuk da olabiliyor ve Wireshark renk durumlarıyla tepki verebiliyor.



Ayrıca Statistics > Conversations bölümündeki tabloyu incelediğimizde aynı şekilde adreslerin sahteliği, paketlerin ve byte boyutunun, 
belli bir oranda/ stabil olması ve paket transferleri arasındaki zaman farkının azlığına baktığımızda, normal bir trafikte böyle bir tablo olmayacağı için, 
bir flood işleminin gerçekleştiğini anlayabiliriz.



Statistics > I/O Graph sekmesini açarsak, ağımızdaki paket sayısının belirli bir süre içerisinde anormal bir artış olması da saldırının kanıtları arasında gösterilebilir.



# MAC FLOODİNG SALDIRISI’NDAN NASIL KORUNURUZ?

Mac Flooding 2. katman saldırıları arasında yer almaktadır. 
2 katman saldırıları Local Ağ’da yapıldığı için güvenlik duvarı ya da diğer güvenlik sistemleri tarafından engellenememektedir. 
Genelde bu koruma sistemleri 2. katman ve üstü için geliştirilmiştir bu yüzden 2. katmanda Local Ağ’da gerçekleşecek bir saldırıyı güvenlik sistemleri engelleyemiyor ama 
spesifik olarak Mac Flooding saldırısı için önlemler alabiliriz, bunlar;

Switch yapısının IP-Mac adresi eşleşmelerini port sayısınca yapılmasıdır. 
Bu yapıldığı taktir de saldırgan makine Switch’in giriş yerine farklı bir IP-Mac eşleşmesine sahip ARP isteği gönderemeyecek.
Switch’in giriş yerine birim sürede gelen ARP isteğini sınırlandırmak. Sınır aşıldığında bunu bir ARP saldırısı olarak algılayabilir ve iletişimi durdurabilir.


------Qizilll

MAC Adres Tablosu doldu ve yeni MAC adreslerini kaydedemiyor. Bu, anahtarın arızalı bir açık moda girmesine yol açacak ve anahtar artık bir ağ hub’ı gibi davranacaktır. 
Gelen verileri bir yayın gibi tüm portlara iletecektir. Bakalım MAC Flooding saldırısı ile saldırganın faydaları nelermiş.


Saldırgan ağın bir parçası olduğu için, saldırgan kurban makineye yönelik veri paketlerini de alacaktır. 
Böylece saldırgan, kurbanın ve diğer bilgisayarların iletişiminden hassas verileri çalabilecektir. Bu hassas verileri yakalamak için genellikle bir paket analizörü kullanılır.


-----

ARP Spoofing

ARP Spoofing, saldırganın sahte ARP Mesajları (Adres Çözümleme Protokolü) gönderdiği ve böylece saldırganın MAC adresinin ağdaki meşru bir kullanıcının 
IP adresiyle ilişkilendirildiği bir saldırıdır. Adres Çözümleme Protokolü, İnternet Protokolü tarafından genellikle IPv4 tarafından bir makinenin IP adresini, 
Ethernet adresi olarak da adlandırılan MAC adresi gibi fiziksel bir adresle eşleştirmek için kullanılan bir protokoldür.


ARP Spoofing, Ağ Katmanı Adres Protokolü (ARP) üzerinde bir tür saldırıdır. Bu saldırı, saldırganın ağdaki diğer cihazları kandırarak, 
kendi MAC adresini belirli bir IP adresine karşılık gelen doğru MAC adresi olarak sunmasıyla gerçekleşir.

İşleyişi şu şekildedir:

ARP İletilerinin Taklit Edilmesi: Saldırgan, ağdaki diğer cihazları kandırmak için ARP paketlerini manipüle eder. 
Genellikle, saldırgan hedeflenen cihazın IP adresi için ARP isteği gönderir ve kendi MAC adresini hedeflenen IP adresiyle eşleştirir.

Yanıt Alma: Saldırganın sahte ARP yanıtı, hedef cihaz tarafından geri alınır. Bu yanıt, hedef cihazın ARP önbelleğine sahte MAC adresini ekler.

Trafik Yönlendirme: Artık hedef cihaz, saldırganın MAC adresini hedeflenen IP adresiyle ilişkilendirir. Bundan sonra, hedef cihazın tüm ağ trafiği, saldırganın cihazına yönlendirilir.

Veri Yakalama ve Man-in-the-Middle Saldırıları: Saldırgan, ağdaki tüm iletişimi izleyebilir, değiştirebilir veya hatta kesintiye uğratabilir. Bu, kullanıcıların hassas bilgilerini çalmak veya ağ trafiğini manipüle etmek için kullanılabilir.

ARP Spoofing saldırılarına karşı korunma yöntemleri arasında ARP izleme ve güvenilirlik denetimleri, ARP tablosunun elle veya otomatik olarak güncellenmesi, ARP izleme araçlarının kullanılması ve ağ trafiğinin şifrelenmesi bulunur. Bu önlemler, ARP Spoofing saldırılarının etkilerini azaltmaya yardımcı olabilir.
