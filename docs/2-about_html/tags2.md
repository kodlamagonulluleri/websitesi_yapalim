# HTML Etiketleri (devam)

Bir önceki kısımda gördüğümüz etiketler kullanmamız gereken, bir HTML sayfasının temeltaşlarını oluşturan etiketlerdi. Ancak bu sayfada göreceğimiz tüm etiketler bizim hayal gücümüzü tarayıcıya aktarmamızı sağlayacak etiketler. Yani bu etiketleri istediğimiz kombinasyonlarda kullanarak istediğimiz web sayfasını oluşturabiliriz. Ancak tahmin edebileceğiniz üzere HTML etiketleri buradakiler ile sınırlı değil. Biz burada sadece dökümanın ilerleyen aşamalarında işimize yarayacak olanları göreceğiz. Diğer tüm HTML etiketleri için [w3schools/tags (ingilizce)](https://www.w3schools.com/tags/) sayfasını ziyaret edebilirsiniz.

# Yazı Etiketleri

Web sayfaları oluştururken her zaman büyülü işler yapan kodlar yazmıyoruz. Bazen de düz yazılar yazmamız gerekiyor ki çoğu zaman sayfaların temellerini bu düz yazılar oluşturuyor. Ve biz yazı yazarken bazı noktaları kalınlaştırmak, başlıklar oluşturmak isteyebiliyoruz. Tam bu noktada şimdi göreceğimiz etiketlerden yardım alıyoruz. Tam bu noktada hatırlatmam gereken bir konu var. Dökümanın HTML'e Giriş kısımında HTML etiketlerinin yapısından bahsetmiştik. Bazı etiketlerin açılması ile kapanması arasına değerler girebildiğimizi ve bunlara içerik (content) dediğimizi hatırlıyorsanız okumaya devam edebilirsiniz.

## Başlıklar

Aslında başlık oluşturmak HTML'de çok basit. Başlık olmasını istediğimiz yazıyı içerik olarak `<h1>` etiketine verdiğimiz zaman o bizim için her şeyi yapıyor. Ancak bazen farklı boyutlarda başlıklar oluşturmamız gerekebiliyor. Tam bu noktada `<hX>` şeklinde kullanabiliyoruz bu etiketi. X yerine 1 ile 6 dahil olmak üzere 1 ile 6 arasında bir rakam girebiliyor ve başlığın boyutunu belirleyebiliyoruz. Bilmemiz gereken nokta ise rakam ne kadar büyür ise (en fazla 6 olabiliyor) başlığın o oranda küçüleceği. Yani ters orantı var.

~~~html
<h1>Ben h1 ile oluşturulmuş bir başlığım</h1>
<h2>Ben h2 ile oluşturulmuş bir başlığım</h2>
<h3>Ben h3 ile oluşturulmuş bir başlığım</h3>
<h4>Ben h4 ile oluşturulmuş bir başlığım</h4>
<h5>Ben h5 ile oluşturulmuş bir başlığım</h5>
<h6>Ben h6 ile oluşturulmuş bir başlığım</h6>
~~~

Bu örneğimizin tarayıcıda verdiği çıktıya hep beraber bakalım.

<h1>Ben h1 ile oluşturulmuş bir başlığım</h1>
<h2>Ben h2 ile oluşturulmuş bir başlığım</h2>
<h3>Ben h3 ile oluşturulmuş bir başlığım</h3>
<h4>Ben h4 ile oluşturulmuş bir başlığım</h4>
<h5>Ben h5 ile oluşturulmuş bir başlığım</h5>
<h6>Ben h6 ile oluşturulmuş bir başlığım</h6>

## Kalın Yazı

`<b>` etiketine içerik olarak verdiğimiz yazı tarayıcılarımız tarafından normal yazılara kıyasla daha kalın yazdırılacaktır.

## Paragraflar

Günlük hayatta bile yazılar yazarken (özellikle de uzun yazılar) okunabilirliği arttırabilmek adına paragraflar halinde yazıyoruz. HTML'de de paragraflar oluşturmak için `<p>` etiketinden yararlanıyoruz. Her paragrafı **p** etiketi içinde yazacağız. Böylelikler daha sonra CSS ile biçimlendirirken işimiz kolay olacak.

# Resim/Görsel

Sayfamız sadece yazılardan oluşmuyor. Bir çok zaman resimlerden de yardım alıyoruz. Bu noktada `<img>` etiketi bizim yardımımıza koşuyor. HTML'de etiketlerin kapatılması gerektiğinden bahsetmiştik. Ancak bazı istisna etiketlerimiz de yok değil. Örneğin **img** etiketimizi açıyoruz ancak kapatmıyoruz. Çünkü bu etiket içerik (content) olarak bir değer almıyor ve dolayısıyla kapatılmasına da gerek olmuyor. Yani bir kapsama alanı yok, kendisi bir işlemi gerçekleştiriyor sadece diyebiliriz.

*HTML'e Giriş* kısımında bazı etiketlerin nitelikler alabildiğinden bahsetmiştik. Bu etiketlerden biri `<img>` etiketi. Bu etikete **src** adında bir nitelik ile değer olarak görselim adresini veriyoruz ve o görseli sayfamıza eklemiş oluyoruz. Adres olarak görselin internet üzerindeki bir adresini verebileceğimiz gibi eğer HTML sayfamız ile erişebilecek bir konumdaysa dosya yolunu da verebiliriz. Örneğin test.html sayfamız ve test.png dosyamız aynı klasörde olsunlar. Biz HTML sayfamız içinde <img src="test.png">` kodumuzu yazarsak yine görsel sayfamıza eklenmiş olacak.


# `<a>` etiketi

`<a>` etiketi ile farklı bir etikete ya da bir yazıya bağlantı özelliği verebiliyoruz. HTML'de nitelik alabilen bir diğer etiket de **a** etiketimiz. Kendisine **href** niteliği ile birlikte değer olarak bağlantı adresini veriyoruz.

~~~html
	<a href="www.twitter.com/kodlamag"> @kodlamag </a>
~~~

Örneğimizi bir HTML dosyası olarak kaydedip herhangi bir tarayıcı ile açarsak mavi renkte **@kodlamag** yazdığını ve bu yazıya tıkladığımızda ilgili Twitter adresinin açıldığını görebilirsiniz. Ayrıca farklı etiketlere de bağlantı verebildiğimizden bahsetmiştik. **a** etiketine içerik olarak farklı bir etiket (örneğin **img** etiketi ile bir görsel) verirseniz verdiğiniz etiketin çıktısı da tıklanabilir olacaktır.

# `<br>` etiketi

Bazı durumlarda bir alt satıra geçmemiz gerekebiliyor. Bu durumda `<br>` etiketini kullanıyoruz. Bu etiket de *img* etiketi gibi kapatılmaya gerek duyulmayan etiketlerden.

# Bölümler

Web sayfalarımızı yekpare oluşturmuyoruz. Örneğin çoğu web sayfasının üst kısmında bir menü bölümü, onun altında içerik bölümü, (eğer var ise) yan kısımında ek detaylar bölümü ve en altta da bir altbilgi bölümü görüyoruz. Bunların her biri bir bölüm olarak değerlendirilebilir.

HTML'de bazı yapıları bölümlere ayırmamız gerekiyor. İleride CSS'ye giriş yaptığımızda daha iyi anlayacağız bu durumu. Tam bu noktada `<div>` etiketi yardımımıza koşuyor. **Div** etiketi bir konteyner oluşturuyor ve kendisine verdiğimiz içeriği bu konteynerın içine koyuyor diye düşünebilirsiniz. Kendisinin alabildiği niteliklere daha sonra değineceğiz.

Ancak günümüzde bu iş biraz daha karmaşık bir hâl aldı(!). **HTML5** ile birlikte gelen özelliklerden biri de isim olarak daha spesifik etiketler. Örneğin artık menü oluştururken *div* etiketi yerine *nav* etiketini kullanıyoruz. Kendisini yine bir div olarak düşünebiliriz. Ancak ismi daha özel ve sayfamızın kodlarını daha okunabilir yapıyor. Buna benzer HTML5 ile beraber eklenen diğer etiketleri de listeleyelim.

* `<article>`
* `<aside>`
* `<details>`
* `<figcaption>`
* `<figure>`
* `<footer>`
* `<header>`
* `<main>`
* `<mark>`
* `<nav>`
* `<section>`
* `<summary>`
* `<time>`

Özetle bu etiketler *div* etiketinin daha insancıl/okunabilir hali ve bir işi yapmak için özelleştirilmiş halidir diyebiliriz.

# Listeleme

HTML'de liste oluşturmanın birkaç farklı yolu var roma rakamlarıyla listeleme, harfler ile listeleme, latin rakamlarıyla listeleme ve noktalar ile listeleme. Biz şimdilik noktalar şeklinde yani madde madde listeleme ile ilgileniyoruz. Liste oluştururken bundan önce öğrendiklerimizden farklı olarak birden fazla etiket kullanacağız. `<ul>` ve `<li>` etiketleri liste oluşturmamızda bize yardımcı olacak. 

`<ul>` etiketi ile öncelikle listemizi başlatacağız ve daha sonrasında her bir liste elemanı için `<li>` etiketini kullanacağız. Bazı büyükşehirleri içeren bir liste oluşturalım ve örnek üzerinden ilerleyelim.

~~~html
<ul>
	<li>İstanbul</li>
	<li>Ankara</li>
	<li>İzmir</li>
	<li>Balıkesir</li>
	<li>Kocaeli</li>
</ul>
~~~

Gördüğünüz gibi her bir maddeyi `<li>` etiketlerine içerik olarak vererek elemanlar oluşturduk. Ve bu elemanları da `<ul>` etiketine içerik olarak verdik. Burada listeyi oluşturan etiketimiz *ul* etiketi, *li* etiketi ise liste elemanlarını belirtiyor. Şimdi bu kodun tarayıcıda vereceği çıktıya bakalım.

<ul>
	<li>İstanbul</li>
	<li>Ankara</li>
	<li>İzmir</li>
	<li>Balıkesir</li>
	<li>Kocaeli</li>
</ul>
