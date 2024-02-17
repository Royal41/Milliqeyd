# ARP SPOOFING (ARP POISONING) nedir?

# ARP , bir IP adresinin hangi MAC adresine ait olduğunu bulmaya yarar.


ARP (Address Resolution Protocol) 
Türkçe karşılığıyla Adres Çözümleme Protokolü yerel ağdaki IP adresi bilinen fakat MAC adresi bilinmeyen bir cihazın MAC adresini öğrenmesi için kullanılan bir protokoldür.

Bildiğimiz gibi yerel ağda bilgisayarlar MAC adresleriyle haberleşirler eğer IP adresi bilinip MAC adresi bilinmiyorsa ARP protokolü başlatılır.


# ARP PROTOKOLÜ NASIL ÇALIŞIR?

Bir bilgisayar diğerine ulaşmak istediğinde elbette karşı öncelikle karşı tarafın kim olduğunu bilmesi gerekir. 
Network ortamında birbirleri ile iletişim kuran her cihazın bir ağ kart(network interface card) bulunmaktadır. 
Bir bilgisayar diğerine ulaşmak istediğinde karşı tarafı bilmesi gerekir.

---------------

Kullanıcı ; isterse belli bir IP adresiyle ,isterse de bilgisayar ismi ile iletişime geçmek istesin ,ağ kartları (network interface card) sadece MAC adresleriyle haberleşebilir. 
Cihazlar birbirlerinin ağ kartlarının üzerindeki fiziksel adreslerini MAC adresi) bilmeden iletişim kuramazlar.
Başka bir ifadeyle ; bir networkte bir cihaz , başka bir cihaz ile haberleşmek istediğinde , haberleşeceği cihazın MAC adresini bilmesi gerekir.

---------------

Bu yüzden bir cihaz başka bir cihaz ile iletişime geçmeden önce ARP sürecini başlatarak , iletişime geçeceği cihazın MAC adresini öğrenir.

İnternette bilgileri bazı requestler yani istekler yollayarak bilgiler sağlıyoruz. 
O da gidiyor internette hangi siteyse ona gönderiyor ve bize bazı cevaplar gönderiyor.


![image](https://github.com/Royal41/Milliqeyd/assets/157361440/715bec5b-e8c3-47da-9907-3ef250dfcf16)

Yani hedef cihazımız gelsin kendi isteğini saldırganın bilgisayarına yapsın, ben o isteği alayım modeme (router) ileteyim. 
Modem cevabı saldırgan bilgisayara versin. 
Ben o cevabı aldıktan sonra geri benim hedef cihazıma ileteyim istiyorum.

Peki ben neden böyle bir şey yapmak istiyorum? Eğer bu bilgi transferi benim üzerimden olursa o zaman ben tüm bu giden gelen bilgilerin hepsini rahatlıkla görebilir ve inceleyebilirim.
İşte ortadaki adam yani Man-in-the-middle (MITM) bu yüzden var.


Saldırgan kendini hedefin ve modemin ortasına koymaya çalışıyor ve bunu yapmak için ele geçirdiği MAC adreslerini kullanıyor


-------

Saldırgan gidecek hedef cihazına diyecek ki benim MAC adresim modemin MAC adresiyle aynı , daha doğrusu; hedef bilgisayara diyecek ki ben modemim. 
Modeme de diyecek ki ben hedef cihazım.

-------


Ama aslında saldırgan ikisi de değil, saldırgan ortadaki adam. Saldırganın apayrı bir MAC adresi var. Fakat bu iki cihazı da kandıracağım diyecek.


Yani saldırgan bu 2 cihazı da kandıracak ve kendini ortaya konumlayacak ki gelen giden tüm trafik kendisinin üzerinden geçsin.


Böylece aslında kimse bir şey anlamayacak. Yani ne modem anlayacak ne de hedef bilgisayar. 
Çünkü hedef bilgisayardaki kişi internete girecek, maile giriyor vs. istediği her şeye giriyor.


Şüphelenmesi için herhangi bir sebep mevcut değil fakat saldırgan o sırada hedef bilgisayarın yaptığı her şeyi görebilir hale gelecek ve böylece tüm bilgilerini ele geçirecek.

İnternette ne yapıyor , nereyi geziyor , şifresi nedir vs. bu tarz bilgileri rahatlıkla çalabilecek.



