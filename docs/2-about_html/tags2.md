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

![hx-tags](../0-static/h-tags.jpg "hX tags")


# `<a>` etiketi

`<a>` etiketi ile farklı bir etikete ya da bir yazıya bağlantı özelliği verebiliyoruz. 