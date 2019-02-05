# CSS'e Giriş

CSS (Cascading Style Sheets) için genel tabirle HTML elemanlarını stillendirmemize olanak sağlayan bir dil diyebiliriz. Örneğin HTML'de *div* etiketini görmüştük. Bu etiketlerle oluşturduğumuz kutucukların boyutlarının ne olacağını, herhangi bir taraftan içeriye girdilenip girdilenmeyeceği gibi özellikleri CSS ile belirliyoruz.

# Sözdizimi

CSS stil dosyalarını oluştururken bilmemiz gereken bir şey var. Bu dosyalarda aslında HTML dosyamızdaki bir şeyi (şeyi diyorum çünkü tek bir eleman da olabilir bir sınıfa dahil eleman grubu da olabilir, birazdan daha detaylı göreceğiz) şekil bakımından düzenliyoruz. Dolayısıyla neyi düzenlediğimizi bildirmemiz gerekiyor. Tam bunu yaptığımız kısıma *seçici (selector)* diyoruz. Daha sonrasında ise süslü parantezler içine o seçtiğimiz şeyin sahip olmasını istediğimiz özellikleri yazıyoruz. Özellikleri yazarken **özellik: değer;** formatında yazıyoruz. Aslında en sonra noktalı virgülü koymasak da olur. Ancak bu durum sadece tek bir özellik belirteceksek geçerli. Birden fazla özellik tanımlarken noktalı virgüller ile ayırıyoruz.


Bahsettiklerimizi görsel üstünde daha kolay anlayabiliriz.

<center>
	<img src="0-static/anatomy-of-css.png">
</center>

## Seçici

Tam olarak neyin stilini düzenleyeceğimizi belirtmek için seçicilerden faydalandığımızdan bahsetmiştim. Görseldeki örnekte görebileceğiniz gibi seçici kısımına *h1* yazılmış, biz bunun aynı zamanda bir HTML etiketi olduğunu biliyoruz. Eğer CSS yazarken seçici kısımında bir HTML etiketinin adını kullanırsak orada belirttiğimiz stil özellikleri HTML dosyamızdaki o etiketlerin tamamına uygulanacak demektir. Yani biz görselde h1 seçicisi ile yazdığımız color özelliğinde rengi kırmızı yapmıştık. Bu demek oluyor ki kullandığımız tüm *h1* etiketleri kırmızı olacak.

Ancak bazı durumlarda tüm etiketleri değil de sadece bir ya da birkaç tanesinin stilini değiştirmek isteyebiliyoruz. Bu durumlarda da sınıflar (classlar) yardımımıza koşuyor. Dökümanın HTML kısımında HTML etiketlerinin nitelikler alabildiğinden bahsetmiştik. Bu niteliklerden biri de *class* niteliği. Biz CSS kodlarımızı yazarken seçici olarak *class* niteliğinin değerini kontrol edip ona göre seçim yapabiliyoruz. Ancak bu sefer seçicinin başına . (nokta) koymamız gerekiyor. Örneğin *class* niteliğinin değeri *deneme* olan etiketleri seçmek istiyorsak **.deneme** şeklinde yazmamız gerekiyor. Hadi buna bir örnek yapalım.

~~~html
<p class="deneme">Ben kırmızı bir yazı olacağım.</p>
~~~

Gördüğünüz gibi *class* niteliğinin değeri *deneme* olan bir *p* etiketi oluşturduk. Şimdi de bu etiketi şekillendireceğimiz CSS kodlarımızı yazalım.

~~~css
.deneme{
	color: red;
}
~~~

Şimdi tarayıcımızda nasıl görünüyor ona bakalım;

<p style="color: red;">Ben kırmızı bir yazı olacağım.</p>

Gördüğünüz gibi kırmızı bir yazı elde ettik. Burada dikkat edilmesi gereken bir şey var. Seçici olarak bir HTML etiketinin adını kullanırsak sayfadaki o etiketlerin tamamına etki edeceğiniz söylemiştik. Ancak seçici olarak sınıf (class) kullanırsak bu demek oluyor ki HTML içinde hangi etiket olduğu farketmeksizin o class değerine sahip tüm etiketler üzerinde çalışacak.

# HTML ile CSS

HTML ile sayfalarımızı oluşturduğumuzu ve CSS ile de sayfalarımızı biçimlendirdiğimizi/güzelleştirdiğimizi öğrendik. Peki hangi CSS dosyası hangi HTML dosyasına etki edeceğini nasıl bilebiliyoruz? Biz belirtiyoruz. HTML'e giriş kısımında HTML şablonundan bahsetmiştik. Orada `<head>` etiketi ile bazı şeyleri belirtiyorduk, örneğin *title*. Bu etiketi içine `<link>` etiketi ekliyoruz ve *rel* niteliğine *stylesheet* değerini veriyoruz. Daha sonra *a* etiketinden de hatırladığımız *href* niteliğine de CSS dosyamızın dizinini değer olarak veriyoruz.

~~~html
<head>
	<link rel="stylesheet" href="stillerim.css">
<head>
~~~

Son olarak dökümanımız bu şekilde görünüyor.
