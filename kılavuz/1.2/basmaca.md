---
layout: kılavuz
---

# Basmaca

<div class="bilgilik (1/1)">
    Şu an Basmaca'nın 1.2 sürümü için yazılmış kılavuzu okuyorsunuz!
</div>

## Basmaca Nedir?

Basmaca, deveb.css ekibi tarafından geliştirilen bir yapıdır. Bu yapı, sadece HTML ve CSS kullanılarak oluşturulan bir modal / aç-kapa yapısıdır. İsmi, anadolu'da kapı mandalına verilen bir isim olan "basmaca"dan gelmektedir.

Bir web sitesinde kullanılan modaller, kullanıcılara belirli bir bilgi veya içeriği daha detaylı bir şekilde sunmak için kullanılır. Genellikle bir düğmeye veya bağlantıya tıklandığında açılan ve kapatılan bu modaller, kullanıcı deneyimini iyileştirir ve siteye etkileşim katmaya yardımcı olur. Basmaca da bu tür bir aç-kapa yapısıdır. Bir aç-kapa / modal yapısı örneği:

<div class="örnek">
<input id="0002-basmacasını-aç" type="radio" name="0002-tr">
<label for="0002-basmacasını-aç">
    <button type="button">AÇ</button> 
</label>
<label for="0002-basmacasını-yum">
    <button type="button">YUM</button>
</label>


<input id="0002-basmacasını-yum" type="radio" name="0002-tr" checked>
<ul>
    <li>1. seçenek</li>
    <li>2. seçenek</li>
</ul>
</div>  

## Niye Basmaca?

Web geliştirme sürecinde, kullanıcı arayüzünü etkileşimli hale getirmek için JavaScript (JS) sıklıkla kullanılan bir programlama dilidir. Ancak, bazı durumlarda JS'nin tarayıcıyı şişirmesi ve daha fazla yer kaplaması sorunları ortaya çıkabilir. İşte bu noktada, Basmaca'nın no-js (JavaScript olmadan) yapısı önemli bir avantaj sunar. Peki, neden Basmaca'yı tercih etmelisiniz?

1. Hafif ve Verimli: 
    Basmaca, sadece HTML ve CSS kullanılarak oluşturulduğu için son derece hafif ve verimlidir. JS kullanmadığından dolayı, tarayıcıda daha az kaynak tüketir ve daha hızlı yüklenir. Bu da kullanıcı deneyimini iyileştirir ve web sayfasının daha akıcı çalışmasını sağlar.

2. Daha Hızlı Yükleme Süreleri:
    JS dosyaları genellikle büyük boyutlara sahip olabilir ve bu da web sayfasının yükleme süresini etkileyebilir. Basmaca, sadece HTML ve CSS kullanıldığı için JS dosyasının yüklenme sürecini tamamen ortadan kaldırır. Bu da sayfanın daha hızlı yüklenmesini sağlar ve kullanıcıların içeriğe daha hızlı erişmesini sağlar.

3. Daha Az Bağımlılık:
    JS kullanılarak geliştirilen modallar, projenin karmaşıklığına bağlı olarak çeşitli kütüphaneleri veya eklentileri gerektirebilir. Bu durum, ek bağımlılıkların yönetilmesini zorlaştırabilir ve projenin sürdürülebilirliğini etkileyebilir. Basmaca ise sadece HTML ve CSS'ye dayandığından, ek bağımlılıklarla uğraşma ihtiyacını ortadan kaldırır ve daha basit bir yapı sunar.

4. Daha Fazla Özelleştirme Seçeneği:
    Basmaca, CSS kullanılarak tasarlandığından, modalın görünümü ve davranışı tamamen geliştiricinin kontrolü altındadır. CSS'in sunduğu zengin özelleştirme seçenekleri sayesinde, farklı stillerde ve tasarımlarda modaller oluşturmanız mümkündür. Bu, projenize özgü bir görünüm elde etmenizi sağlar.

5. JavaScript Bilgisi Gerektirmez:
    Basmaca'yı kullanarak modaller oluşturmak için JavaScript bilgisine ihtiyaç duymazsınız. Sadece HTML ve CSS bilgisiyle modalleri düzenleyebilir ve özelleştirebilirsiniz. Bu, yeni başlayan geliştiriciler veya sadece HTML ve CSS bilgisine sahip olanlar için ideal bir çözüm sunar.

Sonuç olarak, Basmaca'yı tercih etmenizin nedenleri, JS'nin tarayıcıyı şişirmesi ve daha fazla yer kullanması sorunlarını ortadan kaldırmasıdır. Hafif, verimli, hızlı yüklenen ve daha az bağımlılığa sahip olması, Basmaca'yı web geliştirme projelerinde cazip kılar. Ayrıca, CSS ile sağladığı özelleştirme seçenekleri ve JavaScript bilgisi gerektirmemesi de avantajları arasında yer alır. Basmaca, modern ve etkileşimli web siteleri oluştururken JS'ye olan bağımlılığı azaltarak daha sade ve kullanıcı dostu bir deneyim sunar.