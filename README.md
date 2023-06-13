# BASMACA
<details>
    <summary>Türkçe Oku</summary>

Basmaca, arı html-css ile oluşturulmuş açma kapama işini yapan bir düğmedir. 

Basmacaya basınca kapalı olan yeri açacaksınız, açık olan yeri kapayacaksınız. Bu işi ise javascript olmadan yapabileceksiniz. Böylece javascriptin yavaşlatıcı etkisinden sıyrılabileceksiniz. Tasarladığınız ağ sayfasına bakan kişinin bilgisayarını yormayacaksınız.

- Javascript yok
- Ağ tarayıcılarının hepsinde işler.

[Örneği görmek için tıklayınız.](https://data-deveb.github.io/basmaca/)

## Kullanma Kılavuzu

- Aşağıdaki basmacanın html kaynak kodlarını kapın.

```html
<input id="????-basmacayı-aç" type="radio" name="????-tr">
<label for="????-basmacayı-aç"><button type="button">AÇ</button></label>
<label for="????-basmacayı-kapa"><button type="button">KAPA</button></label>

<input id="????-basmacayı-kapa" type="radio" name="????-tr" checked="">
<div>
  <!-- Başucu -->
  Bu alana dilediğini yazabilirsin, koyabilirsin, katabilirsin.
  <!-- Ayakucu -->
</div>
```

- Basmacanın css kodlarını kapın.

```css
/************************************************************************
╔═══════════════════════════════════════════════════════════════════════╗
║ BASMACA 1.0                                                           ║
║ https://data-deveb.github.io/basmaca                                  ║
║ https://github.com/data-deveb/basmaca                                 ║
╚═══════════════════════════════════════════════════════════════════════╝
************************************************************************/

input[id*="-basmacayı-"],
input[id*="-basmacayı-"]:checked+*,
input[id*="-basmacayı-"]:not(:checked)+label+label[for$="-basmacayı-kapa"]{
  /* <input> hep görünmez tutulur. */
  display: none;
}

input[id$="-basmacayı-aç"]+label,
input[id$="-basmacayı-aç"]+*+label {
  /* Tıklar iken yazılar seçilmemeli */
  cursor: pointer;
  user-select: none;
  -moz-user-select: none;
  -webkit-user-select: none;
  -ms-user-select: none;
}

input[id$="-basmacayı-aç"]+label>button,
input[id$="-basmacayı-aç"]+*+label>button{
  /* Kolanlar bir düğme barındırır iken işlemesi için tanımlandı. */
  pointer-events: none;
}
```

- Tasarım belgelerinizde kullanacağınız yerlere katın.

- ???? yazılı yerlere eşsiz bir değer yazın. Örnek: A0A1 > id="A0A1-basmacayı-aç", id="A0A1-basmacayı-kapa" gibi.

- Bitti. Deneyebilirsiniz.

- [Bir sızı durumunda buradan bir başlık oluşturabilirsiniz.](https://github.com/data-deveb/basmaca/issues)
</details>
<details>
    <summary>Read English</summary>

Basmaca is a button that does the job of turning it on and off, created with pure html-css.

By pressing the pressure, you will open the closed place, you will close the open place. You can do this job without javascript. Thus, you will be able to avoid the slowing effect of javascript. You will not tire the computer of the person looking at the web page you have designed.

- No javascript
- It works in all web browsers.

[Click to see the example.](https://data-deveb.github.io/basmaca/)

</details>
