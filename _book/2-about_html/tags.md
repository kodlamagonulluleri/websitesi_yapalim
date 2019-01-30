# HTML Etiketleri

HTML'in ne olduğu ve yapısı hakkında biraz bilgi sahibi olduk. Şimdi bazı HTML etiketlerini öğreneceğiz. Bu etiketleri dökümanın devamında bolca kullancağımız için anlamanız önem taşıyor. Daha sonrasında buraya geri dönüp tekrar bakmaktan çekinmeyin.

## HTML İskeleti

HTML sayfalarının değişmez bir iskeleti var, bu iskelette belli başlı değişmez kısımlar bulunuyor. Öncelikle bu etiketi oluşturalım daha sonrasında üstünde konuşalım.

~~~html
<html>
<head>
	<title></title>
</head>
<body>

</body>
</html>
~~~

Bu iskeleti açıklamaya başlamadan önce lütfen etiketlere bir göz atın. Her etiket açıldığı sırayla kapatılıyor gördüğünüz gibi. Bu HTML'in temel prensiplerinden biri. En başta *html* etiketi açılmış ve daha sonrasında *head* etiketi takip etmiş. Dolayısıyla bu aşamada önce *head* etiketi kapatılmalıdır. Eğer *head* etiketinden önce *html* etiketini kapatırsanız istenmeyen sonuçlarla karşılaşmanız kaçınılmaz olacaktır.

Şimdi iskelette kullanılan etiketlere göz atalım.

### `<html>` etiketi

Bu etiketimiz tarayıcımıza bu dökümanın bir HTML dökümanı olduğunu ve ona göre yorumlaması gerektiğini bildirir. Ayrıca diğer tüm etiketler bu etiketin içine yazılır. Genel kapsayıcıdır diyebiliriz.

### `<head>` etiketi

Adından da anlaşılacağı üzere baş kısımı ilgilendiren kodların yazıldığı bölümdür. İleride stil (CSS) dosyalarımızı bu kısımda içe aktaracağız.

### `<title>` etiketi

Bu etiketimiz sayfamızın (sitemizin) başlığını barındırıyor. Bu etikete içerik olarak verdiğimiz değer tarayıcımızın başlık kısmında görünecek. Modern tarayıcılarda sekme adı olarak da düşünebilirsiniz. Bir örnek yapalım ve herhangi bir sayfamızın `<title>` etiketinin 