# HTML'i Hazırlayalım

İlk yapacağımız şey HTML sayfamızı hazırlamak olacak. Şekillendirme kısımına daha sonra geçeceğiz. Şimdi daha önce indirip kurduğumuz ya da zaten kullandığımız kod editörü ile *index.html* dosyasını açalım. İçine HTML şablonumuzu yazacağız. Bu noktada kopyala yapıştır yapmanızı önermesem de kabul edilebilir. Ancak buradan sonraki aşamalarda kopyala/yapıştır yazmak yerine dökümandan bakarak kendinizin yazması daha sağlıklı olacaktır. Hatta bazı noktaları değiştirmekten/fazlasını eklemekten çekinmeyin. Eğer bu dökümanı bir etkinlikte uyguluyorsanız zaten sizinle ilgilenen deneyimli birisi var demektir. Olası bir hata durumunda ona danışabileceğinizi aklınızdan çıkarmayın. Eğer dökümanı evde uyguluyorsanız olası bir durumda Twitter üzerinden [**@bugraisguzar**](www.twitter.com/bugraisguzar) (bu dökümanı hazırlayan *Kodlama Gönüllüleri* gönüllüsü) ile iletişime geçerek sorularınızı sorabilirsiniz. Ya da **ben@bisguzar.com** adresine mail atabilirsiniz.

~~~html
<html>
<head>
	<title>Ben Buğra İşgüzar</title>
	<link rel="stylesheet" href="style.css">
</head>
<body>

</body>
</html
~~~

Başlangıç için *index.html* sayfamızı bu şekilde düzenleyelim. Ben *title* yani başlık kısımına kendi adımı yazmayı tercih ettim. Siz de kendi adınızla değiştirebilir, *benim sitem, ilk sitem* gibi istediğiniz herhangi bir başlığı koyabilirsiniz. Yaratıcılığınıza kalmış!

Burada dikkat etmemiz geken kısım `<link rel="stylesheet" href="style.css">` satırı. bu satırda CSS dosyamızı çağırdığımızı daha önce öğrenmiştik. HTML ile CSS dosyalarımız aynı dizinde bulunduğu için *href* niteliğine direk dosyanın adını değer olarak verebiliriz. Şimdi sayfamızın içeriğini oluşturmaya başlayabiliriz. Bu aşamadan sonra yazdığımız kodların tamamını *body* etiketinin içeriği olarak yazacağız.

