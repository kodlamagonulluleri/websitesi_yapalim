# Son Dokunuşlar

HTML kodlarımızı yazarken bir menü oluşturduğumuzu hatırlıyorsunuz. Bu menüyü artık işlevsel yapma zamanı geldi. *a* etiketinin sadece web sitelerine bağlantı vermediğinden bahsetmiştik. Bu etiketin bir özelliği de sayfa içinde bağlantı verebiliyor olması. Peki bu bağlantıyı nereye veriyor? Diğer HTML etiketlerine. Peki hangi etikete bağlantı vereceğimizi nasıl seçiyoruz? Etiketlerin **id** niteliğine eşsiz kimlik atayarak. Şimdi oluşturduğumuz *özet, deneyim, eğitim, yetenekler, iletişim* bölmelerine eşsiz id yani kimlikler atayalım. Sırasıyla bu bölümlere atayacağımız id değerlerini listeliyorum.

* bölme      ->  alacağı değer
* özet       ->  ozet
* deneyim    ->  deneyim
* eğitim     ->  egitim
* yetenekler ->  yetenekler
* iletişim   ->  iletisim

Özetle o bölüme belirlediğimiz başlıktan Türkçe karakterleri düzenleyerek idyi tanımlayacağız. İlk bölümümüz olan *özet* kısımının section etiketinin id'sini tanımlayalım.

~~~html
	<section>
		<h2>Özet</h2>
		<p>Yazılıma meraklı bir sağlıkçıyım. Aynı zamanda gezmeyi/organizasyonlarda görev almayı seviyorum.</p>
	</section>
~~~

HTML kodlarımızı yazarken oluşturduğumuz *özet* bölümü böyle görünüyor olmalıydı (içeriğin sizin bilgilerinize göre farklılık gösterebileceğini unutmayalım). Şimdi *section* etiketinin *id* niteliğine *ozet* değerini tanımlayalım.

Sonuç olarak kodlarımız artık şu şekilde görünüyor olmalı.

~~~html
	<section id="ozet">
		<h2>Özet</h2>
		<p>Yazılıma meraklı bir sağlıkçıyım. Aynı zamanda gezmeyi/organizasyonlarda görev almayı seviyorum.</p>
	</section>
~~~

Bu işlemi diğer tüm *section* etikletleri için tekrarlayalım. Ancak her birine içeriğine göre farklı bir id tanımlamaya dikkat edelim. Bu yaptığımız işlemler her bir *section* etiketine bir kimlik vermiş olduk. Şimdi menümüzdeki elemanlara birer bağlantı ekleyerek bu kimliğin olduğu bölgeye yönlendirmesini saylayacağız. Böylece aynı sayfa içinde bağlantılar oluşturmuş olacağiz.

Menü kısımımızın HTML kodları nasıldı bir hatırlayalım.

~~~html
	<ul>
		<li>Özet</li>
		<li>Deneyim</li>
		<li>Eğitim</li>
		<li>Yetenekler</li>
		<li>İletişim</li>
	</ul>
~~~

Şimdi buradaki her elemana ilgili alanına bağlantı ekleyeceğiz. Örneğin *Özet* elemanına id'si *ozet* olan bölgeye yönlendiren bir bağlantı ekleyeceğiz. Hepsini eklediğimizde şuna benzer görünüyor olmalı.

~~~html
	<ul>
		<li>
			<a href="#ozet">Özet</a>
		</li>
		<li>
			<a href="#deneyim">Deneyim</a>
		</li>
		<li>
			<a href="#egitim">Eğitim</a>
		</li>
		<li>
			<a href="#yetenekler">Yetenekler</a>
		</li>
		<li>
			<a href="#iletisim">İletişim</a>
		</li>
	</ul>
~~~

Kayıt edip sayfamızı tarayıcı ile açarsak artık menümüzün de çalıştığını görebiliriz. Ve kişisel sayfamızı başarıyla hazırladık! Sıra sayfamızı internette yayınlamaya geldi, bir sonraki bölüm de bunun hakkında.
