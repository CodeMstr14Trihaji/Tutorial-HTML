# Pengenalan CSS
CSS adalah bahasa yang kita gunakan untuk menata halaman Web.

---
## Apa itu CSS?

- CSS adalah singkatan dari Cascading Style Sheets
- CSS menjelaskan bagaimana elemen HTML ditampilkan di layar, kertas, atau media lainnya
- CSS menghemat banyak pekerjaan. Ia dapat mengontrol tata letak beberapa halaman web sekaligus
- Stylesheet eksternal disimpan dalam file CSS

## Mengapa Menggunakan CSS?

CSS digunakan untuk menentukan gaya untuk halaman web Anda, termasuk desain, tata letak, dan variasi tampilan untuk berbagai perangkat dan ukuran layar.
### Contoh CSS

```css
body {  background-color: lightblue;}  
  
h1 {  color: white;  
  text-align: center;}  
  
p {  font-family: verdana;  
  font-size: 20px;}
```

HTML TIDAK PERNAH dimaksudkan untuk memuat tag untuk memformat halaman web!

HTML diciptakan untuk mendeskripsikan konten halaman web, seperti: 

```html
<h1>Ini adalah judul</h1> 
```

```html
<p>Ini adalah sebuah paragraf.</p>
``` 

Ketika tag seperti `<font>` dan atribut warna ditambahkan ke spesifikasi HTML 3.2, hal itu memicu mimpi buruk bagi pengembang web. Pengembangan situs web besar, tempat font dan informasi warna ditambahkan ke setiap halaman, menjadi proses yang panjang dan mahal. Untuk mengatasi masalah ini, World Wide Web Consortium (W3C) menciptakan CSS. CSS menghapus format gaya dari halaman HTML!
## CSS Menghemat Banyak Pekerjaan!

Definisi gaya biasanya disimpan dalam file .css eksternal.

Dengan file stylesheet eksternal, Anda dapat mengubah tampilan seluruh situs web hanya dengan mengubah satu file!