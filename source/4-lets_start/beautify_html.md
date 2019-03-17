# Görünüşü Güzelleştirelim

Şu andan itibaren daha çok hazırladığımız sayfamızın görünüşünü günümüz tasarım anlayışına göre şekillendireceğiz. Bu sayfayı tek başlık altında hazırladığımız için anlam karmaşası yaşayabilirsiniz. Bu gibi durumlarda mentörünüzden destek istemekten çekinmeyin. Dolayısıyla yazdığımız her ufak kod sayfanın görünüşünde farklılık yaratacak. Bu farklılıkları canlı şekilde takip edebilmek için *index.html* sayfasını tarayıcı ile açalım ve açık kalsın. Bu bölümün ilerleyen noktalarında tarayıcıya geri dönüp sayfayı yenileyeceğiz ve yaptığımız değişiklikleri gözlemleyebileceğiz. Yazdığımız CSS kodlarının karşılığını somut olarak anında gördüğümüz zaman kalıcılığı da artacaktır. Bu bölümde yapacağımız tüm işlemleri *style.css* dosyamız üzerinde yapacağız. Dolayısıyla dosyamızı kod editörümüz ile açalım.

Öncelikle sayfamızın genel görüntüsünü düzenleyerek başlayalım. Web siteleri de bir kompozisyondan oluşur. Ve bu kompozisyonu dönemin trendleri belirler. Modern herhangi bir web sitesine girdiğiniz zaman ana içeriğin sayfanın orta taraflarına doğru konumlandırıldığını görebilirsiniz. Biz de sayfamızın içeriğini ortalayalım ve okunabilirliği arttıralım. Bunun için seçicisi *body* etiketi olan bir css kodu hazırlayalım.

~~~css
body {

}
~~~

İlk olarak kullanacağımız özelliğimiz *margin* özelliği. Margin özelliği ilgili elemanın dış kısımlarından ne kadar öteleneceğini belirlemek için kullanılıyor. Biz şimdi değeri *0 auto* olan bir *margin* özelliği ekleyelim bu kodumuza.

~~~css
body {
	margin: 0 auto;
	max-width: 50em;
}
~~~

Dosyayı kaydettikten sonra tarayıcımıza geçip *index.html* dosyasını yenilersek üst-alt ve yanlardan biraz boşluk oluştuğunu ve içeriğimizin ortalandığını görebiliriz. Burada *margin* özelliğine değer olarak aslında iki farklı değer verdik. Bu değerlerden ilki olan *0* değeri elemanın üst ve alttan ne kadar öteleneceğini ifade ediyor. 2. değer olan *auto* ise sol ve sağ dıştan ne kadar öteleneceğini belirtiyor. Bunların yanında bir de *max-width* özelliğini *50em* olarak ayarladık gördüğünüz gibi. Bunun sebebi ise genişliği belli olmayan bölme/div (body etiketini de bir bölme/div olarak düşünebilirsiniz) aslında genişlik olarak ekranın alabildiği kadar geniştir. Dolayısıyla biz genişliğin tamamını kaplayan bir elemanı yanlardan öteleyemeyiz çünkü ötelenebilecek boş bir değer yok. Değer olarak verdiğimiz *50em* ise bir ölçü birimi. CSS stilleme dilinde *em* ölçü birimi aslında mevcut yazı fontunun kaç katı olacağını belirtiyor. Örneğin **2em = 2\*yazı fontu**.

Örneklendirelim bu konuyu. Ekran genişliğimizin 100em olduğunu düşünelim. Bunun 50em'lik kısımını bizim body etiketimiz kullanacak. geriye 50em kalacak. Bu etiket de sağ ve soldan otomatik olarak öteleneceği için soldan *25em* sağdan da *25em* ötelenecek ve ortalanacak demektir.

Tarayıcıda canlı olarak da görebildiğimiz gibi içeriğimiz yanlardan ortalandı ancak üst ve alttan hâlâ sınırlara dayalı. Bu sefer üst ve alttan öteleme için margin etiketini değil de *padding* etiketini kullanalım. Margin etiketinin o elemanın dıştan ötelenmesini sağladığından bahsetmiştik. *padding* etiketi ise elemanın içten ötelenmesini sağlıyor. 

![marginandpadding](../0-static/marginandpadding.gif "")

Bu görselde yeşil alan HTML elemanını temsil ediyor. Yani bizim senaryomuzda *body* etiketini. Şimdi de *body* seçicimize yazdığımız özelliklere bir de *padding* özelliğini ekleyelim ve değerini de *4em 1em* yapalım. Bunlar da sırasıyla üst-alt ve sol-sağ içe ötelemelerini temsil ediyor.


~~~css
body {
	margin: 0 auto;
	max-width: 50em;
	padding: 4em 1em;
}
~~~

Şu anda kodumuzun son hali yukarıdaki gibi. Ve tarayıcıya geçip sayfayı yenilediğimizde istediğimiz her şeyin olduğunu görebiliyoruz. Biraz da yazıları okunabilir kılalım. Çünkü sayfamızın genel yapısı artık göze daha fazla hitap ediyor ancak yazılar günümüz standartlarına pek de uymuyor. Bunun için aşağıdaki kodları da yine aynı seçicimizin özellikleri arasına ekleyelim.

~~~css
font-family: "Helvetica", "Arial", sans-serif;
line-height: 1.5;
color: #555;
~~~

Bu kodları sırasıyla açıklayalım. İlk satırda aslında yazılarımızın fontunu değiştirdik. *body* etiketi sayfamızı oluştururken kullandığımız diğer tüm HTML etiketlerini kapsadığı için bu etikette yapacağımız değişiklikler diğer tüm etiketlerde de geçerli olacak. Özetle HTML ve CSS'de bir hiyerarşiden bahsedebiliriz. Bu da demek oluyor ki fontu *Helvetica* olarak değiştirmemiz tüm sayfada fontun değişmesi anlamına geliyor.

İkinci satırda da satırların boyutunu ayarladık. *1.5* değeri vererek normal satır yüksekliğini normalinin 1.5 katı olarak ayarlamış olduk. Son satırda da yazı rengini griye yakın bir renk olan #555 rengi ile değiştirdik. Bir de arka plan rengini düzenleyerek bu kısımdaki düzenlemelerimizi sonlandıralım. *background-color* özelliğine de *#f2f2f2* değerini verelim. 

~~~css
body {
  	margin: 0 auto;
  	max-width: 50em;
  	padding: 4em 1em;

  	font-family: "Helvetica", "Arial", sans-serif;
	line-height: 1.5;
	color: #555;

  	background-color: #f2f2f2;
}
~~~

Kodumuzun son hali bu şekilde olacak. Eğer siz kodunuzu kendiniz yazdıysanız kıyaslayabilirsiniz. Tekrar tarayıcımız üzerinden kontrol edelim ve sayfamızın ilk haliyle şimdiki hali arasındaki belirgin farkı gözetleyelim.

Daha öncesinde hatırlıyorsanız sayfamıza görsel eklediğimizde görselimiz abartı boyutlardaydı. Tabii bu benim görselimin boyutlarından dolayıydı, sizin eklediğiniz fotoğrafınız daha küçük veya büyük olabilir. Ancak biz yine de resimin kaplayabileceği yüksekliği sınırlarsak standart bir görünüm elde edebiliriz. *max-width* özelliğinin elemanın genişliğini sınırlandırdığından bahsetmiştik. Elemanın yüksekliğini sınırlandırmak için de *max-height* özelliğini kullanacağız. Görselimizi *img* etiketi ile eklediğimiz için seçicisi *img* etiketi olan yeni bir css kodu hazırlayalım ve *max-height* özelliğine *150px* değerini verelim.

~~~css
img {
	max-height: 200px;
}
~~~

Bu şekilde görünüyor olmalı. Bu sefer ölçü birimi olarak **px** yani pikselleri kullandık. Bu kodlarımızı da yine *style.css* dosyası içine yazmaya devam ediyoruz. Dolayısıyla *style.css* dosyamızın son hali aşağıdaki gibi bir hal almış olmalı.

~~~css
body {
  	margin: 0 auto;
  	max-width: 50em;
  	padding: 4em 1em;

  	font-family: "Helvetica", "Arial", sans-serif;
	line-height: 1.5;
	color: #555;

  	background-color: #f2f2f2;
}

img {
	max-height: 200px;
}
~~~


Sırada ufak küçük dokunuşları yapmak kaldı. *body* etiketinin özelliklerini düzenlerken *color* özelliğine griye yakın bir ton vermiştik. Dolayısıyla sayfamızdaki tüm yazılar griye yakın bir tonda yazıyor. Ancak biz başlıkların daha koyu hatta siyah olmasını istiyoruz ki öne çıkabilsin ve genel okunabilirlik artsın. Bunun için başlıklara özel bir renk tanımlarsak genel renk tanımlamasını ezebiliriz/çiğneyebiliriz (yani genelgeçer olanı yok sayıp özel alan oluşturabiliriz) ve istediğimizi elde edebiliriz. Ancak hatırlarsanız biz HTML kodlarımızı hazırlarken başlıkları *h1* ve *h2* etiketleri ile oluşturmuştuk. Dolayısıyla bu sefer seçicimiz iki farklı etiketi seçecek. Biz bu etiketleri *, (virgül)* ile ayırarak birden fazla etiketi seçmeyi sağlayabiliyoruz. Öncelikle seçicimizi hazırlayalım.

~~~css
h1, h2{

}
~~~

Bu şekilde iki farklı etiketi seçecek ve yazdığımız özelliklerin her ikisi üzerinde de uygulanmasını sağlayacağız. Şimdi de *color* özelliğine *black* değerini verelim ve başlıklarda yazıların siyah olmasını sağlayalım.

~~~css
h1, h2{
	color: black;
}
~~~

Şimdi tüm dosyayı kayıt edelim ve tarayıcı üstünden eserimizi kontrol edelim. Kısa bir CSS yazarak sayfamızı nasıl okunabilir hale getirdiğimizi gördük. Tabii ki CSS bu kadar kısa sürede kavranabilecek bir şey değil. Biz burada sadece ne olduğu ve nasıl/ne amaçlarla kullanıldığı konularında bilgi sahibi olmayı hedefliyorduk ve olduk da. *style.css* sayfamızın son halini kıyaslama yapmak isteyenler için aşağıya bırakalım. Renk özelliklerini, boşluk değerlerini kafanıza göre düzenleyip kendi kişisel dosyanızı oluşturmak daha zevkli olacaktır. Çekinmeyin!

~~~css
body {
  	margin: 0 auto;
  	max-width: 50em;
  	padding: 4em 1em;

  	font-family: "Helvetica", "Arial", sans-serif;
	line-height: 1.5;
	color: #555;

  	background-color: #f2f2f2;
}

img {
	max-height: 200px;
}

h1, h2{
	color: black;
}
~~~