---
layout: kılavuz
---

# Kullanma Kılavuzu

## HTML, `<input>` etiketi

HTML'deki `<input>` etiketi `type` özniteliğine verdiğiniz değere göre farklı amaçlarla kullanılabilir. Basmacayı kullanırken bu özniteliğe `checkbox` veya `radio` değerini vereceğiz. Bakalım, bunlar nasıl çalışıyormuş?

Aşağıda `<input>` etiketine farklı `type` değerleri verilince aldığımız çıktıları göreceğiz:

{%- capture html1 %}
<div>
    <input type="checkbox"> <span>Okudum ve kabul ediyorum</span> <br><br>
    <input type="radio" name="grup1"> <span>Erkek</span> <br>
    <input type="radio" name="grup1"> <span>Kadın</span>
</div>
{%- endcapture -%}

{% include kod_sonuc.html kod=html1 sayi="1" %}

`type` özniteliği `radio` olan `input` etiketlerine bir de `name` özelliği tanımlamak zorunda kaldık. Eğer ikisine de aynı `name` değeri verilmeseydi, tarayıcı, bunların aynı anda seçilemeyeceğini fark edemezdi. Bu durumda hem erkeği hem de kadını seçebilirdik. Sonuç olarak birden fazla seçenekten sadece birinin seçilebilmesini istediğimiz zaman `<input>` etiketinin `type` özelliğini `radio` yapıyoruz ve içlerinden birinin seçilebileceği bu `input` etiketlerine aynı `name` değeri vererek bunları öğürlüyoruz.

## CSS, `:checked` sözde sınıfı

CSS'te, seçilmiş olan `<input>` etiketlerinin görünüm özelliklerini düzenlemek için `:checked` şeklinde bir sözde sınıf bulunur. Aşağıdaki örnekte bu sözde sınıf kullanılarak seçilmiş olan etiketlerin sonrasında "İşaretlendi!" yazısının görüntülenmesi sağlanmıştır.

{%- capture checked %}
<style>
    style + div input:checked + span::after {
        content: "İşaretlendi!";
        margin-left: 1rem;
    }
</style>
<div>
    <input type="checkbox"> <span>Okudum ve kabul ediyorum</span> <br><br>
    <input type="radio" name="grup1"> <span>Erkek</span> <br>
    <input type="radio" name="grup1"> <span>Kadın</span>
</div>
{%- endcapture -%}

{% include kod_sonuc.html kod=checked sayi="2" %}

## HTML, `<label>` etiketi

Yukarıdaki örneklerde, `<input>` etiketlerinin sağında yazılar vardı fakat bu yazıların bir işlevleri yoktu. Şimdi bunlara işlev kazandıralım.

```html
<input type="checkbox">
<label>Okudum ve kabul ediyorum</label>
```

Yukarıdaki örnekte tarayıcının `<label>` etiketi ile `<input>` etiketinin birbirine bağlı olduğunu görmesi mümkün değil, bunu sağlamamız için `<label>` etiketinin `for` özniteliğinin değeri ile `<input>` etiketinin `id` özniteliğinin değerinin aynı olması gerekir. Şimdi bunu deneyelim:

{% capture label %}
<input id="okudum" type="checkbox">
<label for="okudum">Okudum ve kabul ediyorum</label>
<style>
    input#okudum {
        display: none;
    }
    input#okudum:checked + label {
        color: green;
    }
</style>
{% endcapture %}
{% include kod_sonuc.html kod=label sayi="3" %}

Benzer bir şeyi `<input type="radio">` ile deneyelim:

{% capture labelRadio %}
<input id="erkek" type="radio" name="cinsiyet" checked>
<label for="erkek">Erkek</label>
<input id="kadın" type="radio" name="cinsiyet">
<label for="kadın">Kadın</label>
<style>
    input[name="cinsiyet"] {
        display: none;
    }
    input[name="cinsiyet"]:checked + label {
        color: blue;
    }
</style>
{% endcapture %}
{% include kod_sonuc.html kod=labelRadio sayi="4" %}

## Basmaca'nın Kullanımı

Temel kavramları oturttuğumuza göre Basmaca'nın kullanımına geçebiliriz. Gerekli `.css` dosyalarını dahil ettikten sonra kullandığınız `.html` dosyasının `<body>` etiketi içerisine şunu yazmayı deneyebilirsiniz:

{% capture basmacaOrnek %}
<input id="örnek-basmacasını-aç" type="radio" name="örnek">
<label for="örnek-basmacasını-aç">
    <button>Aç</button>
</label>
<label for="örnek-basmacasını-yum">
    <button>Yum</button>
</label>
<input id="örnek-basmacasını-yum" type="radio" name="örnek" checked>

<div modal>
    Açıldı!
</div>
{% endcapture %}
{% include kod_sonuc.html kod=basmacaOrnek sayi="5" %}