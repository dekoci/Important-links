# dekoci Playground (Bahasa)

Repository ini memberikan informasi-informasi seperti
- Tips and trik yang biasa saya gunakan
- Link dan framework yang berguna untuk development
- Software yang biasa saya gunakan

# Konten

1. [Tips and tricks](#tips-and-tricks)
1. [Important Link](#important-link)
1. [Framework](#framework)
1. [Software](#software)

# Tips and tricks

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

1. Pertama kita harus mengaktifkan developer options di hp.
  - Kalau untuk hp Samsung ke about device > software info > build number.
  - Kalau untuk hp Xiaomi ke about phone > MIUI version.
1. Tap terus menerus hingga muncul 'You are now a developer' dan akan muncul menu baru Developer Options di halaman settings.
1. Pergilah ke **Developer** options lalu centang USB debugging.
1. Sambungkan hp-mu ke komputer dengan menggunakan kabel charger USB.
1. Buka halaman yang ingin di inspect elementnya di hp-mu dengan browser Chrome.
1. Lalu di browser Chrome desktop-mu, ketik `chrome://inspect#devices`.
1. Jika hp-mu muncul 'PC with mac address xx:xx:xx will access your smartphone' maka kamu sudah berhasil. Lalu tap Yes.
1. Otomatis di browser Chrome desktop-mu akan muncul list page beserta link yang sedang terbuka di hp-mu dengan tombol **inspect**, **focus tab**, **reload** dan **close**.

### Solusi untuk event keyup SPASI tidak terdeksi untuk keyboard mobile (Android+Chrome)

Seperti yang kita tahu, setiap kita menekan jenis huruf / kata di keyboard maka akan me-return keyCode(int).
SPASI harusnya mereturn keycode 32, tapi di mobile kita akan mendapatkan keycode 229.
Jadi saya sudah menemukan solusi dengan mencontek kode di [10fastfingers.com](https://10fastfingers.com/)

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

# Important link

- [Mengubah PNG ke SVG](http://www.online-convert.com/result/35c9d026a93397d4f529fd15f6ec3669)
- [Favicon generator](http://www.favicon-generator.org/)
- [Membuat Sprites dari beberapa gambar](http://spritegen.website-performance.org/)
- [Font converter](https://onlinefontconverter.com/)
- [Css animation generator](http://cssanimate.com/)
- [Membuat GIF dari gambar](http://gifcreator.me/)
- [Membuat background-color gradient](http://www.colorzilla.com/gradient-editor/)
- [Membuat function fullscreen browser pada button tanpa F11](http://stackoverflow.com/questions/3900701/onclick-go-full-screen)

# Software

### Local server

- [XAMPP (Windows)](https://www.apachefriends.org/index.html)
- [MAMP (Mac)](https://www.mamp.info/en/)

### Terminal 

- [Hyper terminal](https://hyper.is/)
- [Hyper plugin](https://github.com/bnb/awesome-hyper)

### Editor

- [Vscode](https://code.visualstudio.com/)
- [Sublime Text](https://www.sublimetext.com/)

### Editor plugin

- [Package Control](https://packagecontrol.io/installation)
- [Material Theme](https://github.com/equinusocio/material-theme)
- [Alignment](https://packagecontrol.io/packages/Alignment)
- [Emmet](https://emmet.io/)

### Chrome extensions

- [Quick javascript switcher](https://chrome.google.com/webstore/detail/quick-javascript-switcher/geddoclleiomckbhadiaipdggiiccfje?hl=en) Toggle javascript pada browser
- [var_masterpiece](https://chrome.google.com/webstore/detail/varmasterpiece/chfhddogiigmfpkcmgfpolalagdcamkl?hl=en) Mempercantik hasil return object dan array di browser
- [Screencastify](https://chrome.google.com/webstore/detail/screencastify-screen-vide/mmeijimgabbpbgpdklnllpncmdofkcpn?hl=en) Merekam seluruh/sebagian layar browser
- [Zenmate VPN](https://chrome.google.com/webstore/detail/zenmate-vpn-best-cyber-se/fdcgdnkidjaadafnichfpabhfomcebme?hl=en) Memanipulasi ip address ketika berkunjung ke website
- [Flash Video Downloader](https://chrome.google.com/webstore/detail/flash-video-downloader/aiimdkdngfcipjohbjenkahhlhccpdbc?hl=en) Untuk mendownload video di page yang sedang dibuka

### FTP 

[Cyberduck](https://cyberduck.io/?l=en)

### Git dengan GUI

[Source tree](https://www.sourcetreeapp.com/)

# Framework

### PHP

[Laravel](https://laravel.com/)

### Css

- [Foundation](http://foundation.zurb.com/)
- [Materializecss](http://materializecss.com/)
- [Animate.css](https://daneden.github.io/animate.css/)

### Javascript

- [jQuery](https://jquery.com/)
- [Lodash](https://lodash.com/)
- [jQuery UI](https://jqueryui.com/)
- [Anime.js](http://anime-js.com/)
- [Socket.io](https://socket.io/)
