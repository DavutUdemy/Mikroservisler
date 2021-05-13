# Mikroservisler
Makaleye :Proje uzerinden Mikroservisler.docx ulasabilirsiniz
MikroServisler Teknik Bilgi




Yazilim Dunyasinda iki tane yapi vardir bunlardan biri monolotik digeri ise mikroservisdir
Monolotik mimari cok eskidir ve bir cok firma monolotik mimariden vazgeciyor.Monolotik mimaride her sey bir yerdedir mesela: servisler,controllers,repositoriler,veritabani ve bir cok sey bir dosyadadir

Mikroservisde ise uygulamamizda ihtiyac olabilecegi sekilde istediginiz kadar  dagitiyorsunuz ve parcaliyorsunuz.
Mesela uygulamanin kodlarini ayri bir sunucuda barindiriyoruz ,veritabani da ayni sekilde,Static dosyalari ayri bir sunucuda barindiriyoruz ama mikroservis sadece bu amac ile yapilmadi.
 
Her parca icin service katmanlara ayira biliyoruz. Mikroservis dezavantaj ve avantaj gibi bir sey soz konusu degildir.kurumsal sirketseniz mikroservis kullanmaya zorunlusunuz.
Gunumuzde bir cok firma mikroservis kullaniyor bunlardan bir ise Netflixdir.
Mikroservis clean code icin cok iyidir.Cok daha iyi performans alinir.
Mikroservis iliskisel database icin cok iyidir.

 















Gelelim Spring ile mikroservis yapisina

 


Gordugunuz uzere iki tane DB var
Bu iki db birbirine bagli burda mikroservis isimizi cok kolaylastiriyor ve performas kaybina yol acmiyor.

Hystrix:
Eger bizim mikroservisimiz hata alirsa veya response failure olursa kac tane istek atilmis
Hangi mikroservis calismamis 
 ve daha bir cok islemi gormemiz icin burda devreye hystrix giriryor

Config Server:

Bu bizim mikroservislerimizin configurasyonudur.normalde her bir mikroservis icin bir configuration olusturulmali ama bu islem performs kaybina yol acar her bir mikroservis ayari degistirmek gercekten yorucudur 
Bu yuzden config -server kullanilir


Zipkin :
 




Zipkin uygulamamizda hata cikarsa 
nerde hangi service hangi controllerda saat kacda basladi hata saat kacda bitdi ve bunun gibi bir cok sey gosterir.

 





Burda hystrix ile kafa karisikli olabilir bilmemiz gereken hystrix uygulamanin nerde hata olustugunu gostermez.


Son olarak GateWay Deyinmek Istiyorum 
Iki db icinde gateway kullandik.
Atilan requestler gateway yani api son haline gidiyor request ve responselardan gateway sorumludur


USED TECHNOLOGIES :SPRING BOOT SPRING CLOUD SPRING DATA JPA LOMBOK H2 DATABASE ZIPKIN EUREKA HYSTRIX AND  GATEAWAY 
