# Important-links (Bahasa)

Repository ini hanya memberikan informasi-informasi seperti
- Tips and trick yang biasa saya gunakan
- Link yang berguna untuk development
- Software yang biasa saya gunakan

# Konten

- [Tips and tricks](#tipsandtricks)
- [Important Links](#importantlinks)
- [Framework](#framework)
- [Softwares](#softwares)

# Tipsandtricks

### Mencegah Sass membuat file .map (Ini menggunakan Sass command line)

  ```shell
  --sourcemap=none
  ```

### Mencegah Sass membuat cache (Ini menggunakan Sass command line)

  ```shell
  --no-cache
  ```

### Sass dapat sekaligus meminify css (Ini menggunakan Sass command line)

  ```shell
  --style compressed
  ```
  
### Cara melakukan inspect element Chrome di handphone (Android saja)

- Pertama kita harus mengaktifkan developer options di hp.
  - Kalau untuk hp Samsung ke about device > software info > build number.
  - Kalau untuk hp Xiaomi ke about phone > MIUI version.
- Tap terus menerus hingga muncul 'You are now a developer' dan akan muncul menu baru Developer Options di halaman settings.
- Pergilah ke Developer options lalu centang USB debugging.
- Sambungkan hp-mu ke komputer dengan menggunakan kabel charger USB.
- Buka halaman yang ingin di inspect elementnya di hp-mu dengan browser Chrome.
- Lalu di browser Chrome desktop-mu, ketik `chrome://inspect#devices`.
- Jika hp-mu muncul 'PC with mac address xx:xx:xx will access your smartphone' maka kamu sudah berhasil. Lalu tap Yes.
- Otomatis di browser Chrome desktop-mu akan muncul list page beserta link yang sedang terbuka di hp-mu dengan tombol **inspect**, **focus tab**, **reload** dan **close**.

### Solusi untuk event keyup SPASI tidak terdeksi untuk keyboard mobile (Android+Chrome)

Seperti yang kita tahu, setiap kita menekan jenis huruf / kata di keyboard maka akan me-return keyCode(int).
SPASI harusnya mereturn keycode 32, tapi di mobile kita akan mendapatkan keycode 229.
Jadi saya sudah menemukan solusi dengan mencontek kode di https://10fastfingers.com/

```javascript
var android_spacebar = 0;
$(window).on("touchstart", function(event) {
  $input.on("input", function( event ) {
    var value = $input.val();	

    if (value.indexOf(" ") != -1) {
      android_spacebar = 1;
    } else {
      android_spacebar = 0;
    }
  });
});
```

Penjelasan code di atas, untungnya kita bisa mendapatkan event touchstart bahkan ketika kita menekan tombol keyboard di mobile. 
Maka kita cek kotak input yang ingin kita awasi, lalu cek setiap string yang masuk apakah terdapat spasi atau tidak dengan menggunakan function [jQuery indexOf](https://www.w3schools.com/jsref/jsref_indexof.asp).

### Cara menghilangkan a link highlight color di Mobile ketika di tap

```css
-webkit-tap-highlight-color: rgba(0, 0, 0, 0);
```

# Importantlinks

### Mengubah PNG ke SVG

http://www.online-convert.com/result/35c9d026a93397d4f529fd15f6ec3669

### Favicon generator

http://www.favicon-generator.org/

### Membuat Sprites dari beberapa gambar

http://spritegen.website-performance.org/

### Font converter

https://onlinefontconverter.com/

### Css animation generator

http://cssanimate.com/

### Membuat GIF dari gambar

http://gifcreator.me/

### Membuat background-color gradient

http://www.colorzilla.com/gradient-editor/

### Membuat function fullscreen browser pada button tanpa F11

http://stackoverflow.com/questions/3900701/onclick-go-full-screen

# Softwares

### Terminal 

https://hyper.is/
[plugin](https://github.com/bnb/awesome-hyper)

### Editor

https://code.visualstudio.com/

https://www.sublimetext.com/

### Editor plugin

[Package Control](https://packagecontrol.io/installation)

[Material Theme](https://github.com/equinusocio/material-theme)

[Alignment](https://packagecontrol.io/packages/Alignment)

[Emmet](https://emmet.io/)

### Chrome extensions

[Quick javascript switcher](https://chrome.google.com/webstore/detail/quick-javascript-switcher/geddoclleiomckbhadiaipdggiiccfje?hl=en) Extension ini berguna untuk mematikan javascript website yang sedang kita buka.

[var_masterpiece](https://chrome.google.com/webstore/detail/varmasterpiece/chfhddogiigmfpkcmgfpolalagdcamkl?hl=en) Extension ini berguna untuk developer yang kesulitan melihat hasil return object dan array yang ditampilkan browser, extension ini merapihkan sehingga mudah dilihat mata.

[Screencastify](https://chrome.google.com/webstore/detail/screencastify-screen-vide/mmeijimgabbpbgpdklnllpncmdofkcpn?hl=en) Extension ini berguna untuk mereka video browser, biasa digunakan untuk membuat dokumentasi atau tutorial.

[Zenmate VPN](https://chrome.google.com/webstore/detail/zenmate-vpn-best-cyber-se/fdcgdnkidjaadafnichfpabhfomcebme?hl=en) Extension ini berguna untuk memanipulasi ip address kita ketika berkunjung ke website.

[Flash Video Downloader](https://chrome.google.com/webstore/detail/flash-video-downloader/aiimdkdngfcipjohbjenkahhlhccpdbc?hl=en) Extension ini berguna untuk mendownload video, list video akan ditampilkan sesuai dengan page yang kita buka

### FTP 

https://cyberduck.io/?l=en

### Git dengan GUI

https://www.sourcetreeapp.com/

# Framework

### PHP

[Laravel](https://laravel.com/)

### Css

[Foundation](http://foundation.zurb.com/)

[Materializecss](http://materializecss.com/)

### Javascript

[jQuery](https://jquery.com/)

[Lodash](https://lodash.com/)

[jQuery UI](https://jqueryui.com/)



