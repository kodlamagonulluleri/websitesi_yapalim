# İnternet Nasıl Çalışır?

Bir websitesi yapacaksak öncelikle internetin nasıl çalıştığı konusunda en azından fikir sahibi olmamız gerekiyor. Öncelikle internetin bir çok bilgisayarı (kişisel bilgisayar, sunucu, süper bilgisayarlar) birbirine bağladığını söyleyebiliriz. Bu bilgisayarlar internet üzerinden sürekli birbirlerine anlamlı/anlamsız (bizim için anlamsız, uygulamalar için anlamlı) veriler gönderiyorlar. Örneğin Twitter'i açtığınızda gördüğünüz sayfa sizin için anlamlı ancak o sayfa ile birlikte tarayıcınıza iletilen diğer veriler (çerezler, headerler, kurabiyeler) sizin için bir anlam ifade etmese de tarayıcınız ve Twitter için çok anlam ifade edebiliyor. Bu dökümanda sadece HTML ve CSS dilleri hakkında giriş seviyesinde bilgi aktaracağımız için internetin çalışma prensibine çok derinden inmeyeceğiz. 

![howinternetworks](https://img.labnol.org/di/how-internet-works1.jpg "How Internet Works")

Bu görselde internetin nasıl çalıştığı ve ana karakterlerin neler olduğu basitçe karikatürize edilmiş. Bu aşamada dikkat etmemiz gereken karakterler *User (Kullanıcı)*, *Browser (Tarayıcı)* ve *Hosting Server (Sunucu)*. Bunların ne olduğunu biraz detaylı inceleyelim.

## User (Kullanıcı)

User, arama çubuğuna twitter.com yazıp siteye giren bizler oluyoruz.

## Browser (Tarayıcı)

Browser ise Chrome, Firefox, Opera, Vivaldi, Safari gibi tarayıcılar oluyor. Browser, user(kullanıcı) arama çubuğuna twitter.com yazıp gönderdiği zaman *Hosting Server*'e User'in twitter.com'a girmek istediğini bildiriyor. Hosting server gerekli kontrolleri yaptıktan sonra (eğer kontrol katmanları varsa) twitter.com sitesinin HTML ve CSS dosyalarını tekrar Tarayıcıya gönderiyor. Tarayıcımız da kendisine sunucudan ulaşan bilgileri kullanıcının anlayabileceği formata çevirip, biçimlendirip ekrana yansıtıyor.

## Hosting Server (Sunucu)

Aslında web sitelerinin kalbi sunucular diyebiliriz. Web sitelerinin temelde HTML/CSS dosyalarından oluştuğunu biliyoruz. Ve bu HTML/CSS dosyalarının kullanıcının anlayabileceği görsel formata *tarayıcılar* tarafından çevirildiğini de az önce öğrenmiştik. Dolayısıyla bu HTML/CSS dosyalarının bir yerde durması ve gerektiği/istendiği zaman tarayıcıya gönderilmesi gerekiyor. İşte bu işlemleri sunucular gerçekleştiriyor.

Sunucuları şu an bu dökümanı okuduğunuz bilgisayarınızın/telefonunuzun daha gelişmiş ve sadece dosya tutmat/göndermek için özelleşmiş çeşidi olarak düşünebilirsiniz. Biz bu dökümanın son aşamasında web sitemizi yayına alırken sunucu olarak Github'u kullanacağız.