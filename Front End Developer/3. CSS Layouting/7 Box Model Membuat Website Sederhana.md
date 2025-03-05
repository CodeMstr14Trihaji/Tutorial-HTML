---
obsidianUIMode: preview
sumber: WPU
level: sulit
bahasa: CSS
tanggal_study: 2024-10-13T01:10:00
total_study: 1
tags:
  - CSS
id: WPUCSSLOT8
sr-due: 2024-10-14
sr-interval: 1
sr-ease: 130
---
# Box Model Membuat Website Sederhana
Jadi, pada kesempatan kali ini, kita akan mencoba untuk membuat website sederhana, dengan desain rancangan sebagai berikut:

![[7 Box Model Membuat Website Sederhana-1.png]]

Baiklah, ada beberapa hal yang perlu diperhatikan disini:
- Website akan memiliki gambar utama, yang kita sebut hero image. Supaya website kita lebih menarik dan seperti artikel pada umumnya.
- Memiliki h1 dan h2.
- Memiliki link navigasi pada bagian atas atau header, yang terdiri dari 5 link.
- Terdapat area footer dibagian bawah.
- Terdapat beberapa paragraf sebagai isi artikel.

Baiklah, mari kita mulai!
## 1. Membuat container
Jika kamu perhatikan, website ini akan berbentuk kotak yang tidak memenuhi browser. Jika kita membuat beberapa kotak sendiri-sendiri, dimana footer, header, dan kotak artikel terpisah elemenya, lalu menggunakan **margin: auto;**, memang kotak-kotak tersebut akan berposisi ditengah. 

Namun cara ini tidak efektif. Kita perlu membuat pembungkus atau **container** yang mewadahi semua isi website kita, sehingga kita hanya perlu mengatur satu elemen agar, untuk membawa semua elemen didalamnya agar berposisi ditengah menggunakan properti **margin**. Mungkin kode HTML yang kita buat akan menjadi seperti ini (index.html):

```html
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Box Model</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <div class="header">

        </div>
    </div>
    
</body>
</html>
```

Lalu kode CSS yang kita buat akan seperti ini, jangan lupa, kita tambahkan **CSS reset** untuk mereset semua nilai defautl **margin** yang dimiliki oleh beberapa elemen HTML (style.css):

```css
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}
```

Tapi nantinya, dalam pembelajaran kali ini, sytax diatas tidak perlu ditunjukan lagi supaya menghemat tempat dalam memberi penjelasan. Jadi, intinya, syntax diatas tidak perlu diutak-atik lagi, dan hiraukan saja dalam perubahan kode CSS mendatang.

Sekarang, buat kode CSS ini:

```css
.container {
    width: 800px;
    margin: auto;
}
```

Hal ini untuk membuat website kita berada di tengah, dengan panjang **800px**, sehingga hasilnya adalah sebagai berikut:

![[7 Box Model Membuat Website Sederhana-2.png]]

Sekarang, kotak sudah berada ditengah, ditandai dengan tulisan "My Website" yang berada ditengah, karena mengikuti *parent*-nya, yaitu elemen dengan class **container**.
## 2. CSS body
Tambahkan kode CSS berikut untuk memberi style pada elemen **body**:

```css
body {
    font: 16px/28px arial, sans-serif;
    background-color: #eaeaea;
    color: #333;
}
```

Penjelasan:
- **font** : *16px/28px* artinya kita menggunakan ukuran font *16px*, dengan jarak antarbarisnya adalah *28px*. Lalu jenis font yang kita gunakan adalah *arial*, dan *sans-serif*. Sebenarnya kita bisa menggunakan properti yang berbeda-beda untuk setiap value yang berbeda, kita hanya melakukan **shorthand** atau penyingkatan.
- **background-color** : *\#eaeaea* berguna untuk memberi background yang berwarna sedikit putih keabu-abuan.
- **color** : berguna untuk memberi warna pada tulisan yang ada di elemen **body**. Warna yang kita berikan adalah abu-abu tua, yaitu *\#333333*. Karena nilai hexadesimalnya sama semua, bisa kita singkat menjadi hanya *\#333* saja.
## 3. CSS container
Sekarang, kita beri warna elemen **container** dengan warna putih. Rubah kode CSS **container** menjadi seperti ini:

```css
.container {
    width: 800px;
    margin: auto;
    background-color: white;
}
```

## 4. padding Header
Karena kontek utama kita terlalu dekat dengan langit-langit browser, maka kita buat style untuk **header** dengan kode CSS sebagai berikut:

```css
.header {
    padding: 20px;
}
```

Sejauh ini, ini dia hasiilnya:

![[7 Box Model Membuat Website Sederhana-3.png]]

## 5. CSS h1
Kenapa ukuran teks pada elemen **h1** berukuran kecil, bukanhkah sebelumnya kita sudah belajar, bahwa tag h1 akan memberikan judul dengan text berukuran paling besar?

Hal ini terjadi karena kita sudah melakukan **CSS Reset** sebelumnya, sehingga nilai default yang dimiliki oleh elemen **h1** pun juga akan hilang. Rubah kode HTML kita menjadi seperti ini: 

```html
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Box Model</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <div class="header">
            <h1 class="judul">My Website</h1>
        </div>
    </div>

</body>
</html>
```

Sekarang, kita beri kode CSS berikut untuk memperindah elemen **h1**:

```css
.header .judul {
    font-size: 40px;
    font-weight: bold;
}
```

Maka hasiilnya menjadi seperti ini:

![[7 Box Model Membuat Website Sederhana-4.png]]

## 6. Membuat navigasi
Sekarang, kita akan membuat link navigasi, rubah kode HTML menjadi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Box Model</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <div class="header">
            <h1 class="judul">My Website</h1>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Product</a></li>
                <li><a href="#">Service</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>
    </div>

</body>
</html>
```

Diatas, kita menambahkan tag `<ul>`, lalu kita isi dengan tag `<li>` yang didalamnya terdapat link. Setelah itu kita tambahkan kode CSS sebagai berikut:

```css
.header ul li {
    display: inline-block;
    margin-top: 20px;
    margin-right: 10px;
}
```

Penjelasan kode diatas:
- **.header ul li { }** : Selector yang kita gunakan untuk menarget elemen dengan class bernama **header**, lalu menarget tag `<ul>` yang didalamnya terdapat tag `<li>`. Kita buat lebih spesifik, ingat bukan materi tentang bobot selector? Bagus kalau kamu ingat, kita gunakan konsep itu disini.
- **display: inline-block;** : Properti ini kita gunakan agar list yang dimunculkan memiliki **display** dengan value **inline-block**. Ini membuat link kita muncul dalam satu baris, secara horizontal, bukan turun kebawah.
- **margin-top:20px;** : Agar navigasi yang kita buat tidak terlalu menempel dengan judul website kita. Berguna agar navigasi turun kebawah sebanyak **20px**.
- **margin-right: 10px;** : Berguna agar setiap link yang kita buat, memiliki jarak yang cukup, agar tidak terlalu menempel satu sama lain.

Nah, berikut hasil dari kodingan kita:

![[7 Box Model Membuat Website Sederhana-5.png]]

## 7. CSS navigasi
Navigasi yang kita buat sudah lumayan bagus, namun itu tidak menjadi alasan untuk tidak menambahkan beberapa CSS didalamnya. Ada beberapa hal yang bisa kita lakukan untuk meningkatkan tampilan navigasi agar lebih menarik. Yang akan kita lakukan adalah merubah warna, dan menambahkan *pseudo-class*.

Berikut kode CSS yang kita tambahkan:

```css
.header a {
    text-decoration: none;
    color: salmon;
    padding: 3px;
}

.header a:hover {
    background-color: lightskyblue;
    color: white;
}
```

Penjelasan untuk selector pertama:
- **.header  a { }** : Selector yang memfokuskan padad elemen dengan class **header**, lalu memilih tag `<a>` yang ada didalamnya.
- **text-decoration: none;** : Berguna untuk menghilangkan dekorasi teks bawaan link, seperti garis bawah atau *underline*.
- **color: salmon;** : Memberi warna pada link dengan warna *salmon*.
- **padding: 3px;** : Memberi **padding** pada setiap link dengan value *3px*. Perubahan ini akan membuat tampilan lebih menarik ketika kita menambahkan *pseudo-class* berupa **:hover**, yang nanti akan dijelaskan.

Penjelasan untuk selector kedua:
- **.header a:hover { }** : Selector memfokuskan pada elemen dengan class **header** yang didalamnya terdapat tag `<a>`, lalu buat *pseudo-class* bertipe **:hover** (memberi style ketika kursor mouse berada diatas elemen).
- **background-color: lightskyblue;** : Memberi efek berupa background yang berwarna *lightskyblue*.
- **color: white;** : Memberi warna pada teks berupa warna *putih*.


> [!NOTE] Bantuan!
> Untuk bisa mendapatkan sample warna yang lengkap, bisa mengunjungi situs:
> - https://imagecolorpicker.com/ Untuk sampel warna dengan format hexadesimal, RGB, dll.
> - https://www.w3schools.com/cssref/css_colors.php Untuk bantuan dari situs W3Schools


Sehingga hasilnya akan menjadi seperti ini:

![[Screen Recording 2024-10-12 231245.mp4]]

## 8. Hero image
Untuk memasukan gambar, kita bisa menggunakan gambar kita sendiri, yang mana ukuranya terserah. Namun kita harus hati-hati dalam menggunakan gambar yang kita ambil secara sembarangan di Internet, karena bisa jadi gambar tersebut memiliki **Copyright**. 

Kita bisa mengunjungi situs penyedia gambar gratis, seperti https://unsplash.com/, yang menyediakan banyak gambar secara gratis untuk digunakan. pilih salah satu gambar yang sesuai, lalu download.

Berikut adalah gambar yang kita pilih:

![[heroimage.jpg]]

Sebelum kita menggunakanya, kita perlu cek ukuran atau **size** gambar, karena jika terlalu besar, maka perlu kita **resize** atau perkecil ukuranya. Hal ini bisa dilakukan dengan menggunakan aplikasi seperti **Potoshop**, dan sejenisnya, atau website yang menyediakan jasa resize ukuran gambar.

Setelah itu, kita pindahkan file gambar tadi, ke dalam file yang sama, atau mengetikan alamat pathfile gambar tersebut.

Baiklah, kita buat kode HTML menjadi seperti ini, kita siapkan elemen untuk menampung gambar ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Box Model</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <div class="header">
            <h1 class="judul">My Website</h1>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Product</a></li>
                <li><a href="#">Service</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>

        <div class="hero"></div>

    </div>

</body>
</html>
```

Lalu buat kode CSS sebagai berikut:

```css
.hero {
    height: 250px;
    background-image: url(heroimage.jpg);
}
```

Penjelasan kode diatas adalah sebagai berikut:
- **.hero** : Memfokuskan pemberian style pada elemen dengan class **hero**.
- **height:  250px;** : Menentukan tinggi elemen (gambar) yaitu **250px**. Untuk **width** atau panjang tidak kita tentukan, biarkan mengikuti lebar **container**-nya.
- **background-image: url(heroimage.jpg);** : Menampilkan background untuk elemen berupa gambar dengan nama file gambar adalah *heroimage.jpg*.

Maka, hasilnya akan menjadi seperti ini:

![[7 Box Model Membuat Website Sederhana-6.png]]

Jika diperhatikan, gambar tidak muncul dengan ukuran yang seharusnya. Supaya gambar bisa muncul dengan ukuran yang pas, rubah kode CSS menjadi seperti ini:

```css
.hero {
    height: 280px;
    background-image: url(heroimage.jpg);
    background-size: cover;
    background-position: 0 -70px;
    border-top: 5px solid salmon;
    border-bottom: 5px solid lightskyblue;
}
```

Penjelasan kode diatas:
- **.hero { }** : Selector yang akan memfokuskan pada elemen dengan class bernama **hero**.
- **height: 280px;** : Menentukan tinggi elemen yang akan menjadi wadah gambar, berupa **280px**.
- **background-image: url(heroimage.jpg);** : Menampilkan background untuk elemen berupa gambar dengan nama file gambar adalah *heroimage.jpg*.
- **background-size: cover;** : Agar gambarnya muat kedalam elemen yang dibuat.
- **background-position: 0 -70px;** : Mengatur posisi gambar. Value pertama menentukan pergeseran horizontal, sedangkan value kedua menetukan pergeseran secara vertikal. Untuk horizontal sudah tepat, sehingga kita beri nilai **0**. Untuk vertikal masih kurang tinggi, sehingga kita tambahkan value **-70px**.
- **border-top: 5px solid salmon;** : Memberi border bagian atas dengan ketebalan **5px** dengan type **solid**, dan berwarna *salmon*.
- **border-bottom: 5px solid lightskyblue;** : Memberi border pada bagian bawah dengan ketebalan **5px** dengan type **solid**, dan berwarna *lightskyblue*.

Maka, hasilnya akan menjadi seperti ini:

![[7 Box Model Membuat Website Sederhana-7.png]]

## 9. Isi konten
Sekarang, kita masuk ke pembuatan isi konten. Langsung saja, kita rubah kode HTML kita menjadi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Box Model</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <div class="header">
            <h1 class="judul">My Website</h1>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Product</a></li>
                <li><a href="#">Service</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>

        <div class="hero"></div>
        <div class="content">
            <h2>Judul Artikel</h2>
            <p class="penulis">ditulis oleh<a href="#">Trihaji Khoerur Rohman</a> pada 12 Oktober 2024</p>
        </div>
    </div>

</body>
</html>
```

Bisa dilihat, bahwa kita menambahkan beberapa elemen, seperti:
- Elemen dengan class **content**
- tag `<div>`, `h2`, `<p>`, dan `<a>`.
- Elemen paragraf dengan class **penulis**

Baiklah, lalu buat kode CSS sebagai berikut:

```css
.content {
    padding: 20px;
}

.content h2 {
    font-size: 28px;
    font-weight: bold;
}

.content .penulis {
    font-size: 11px;
    margin-top: 5px;
}
```

Berikut penjelasan mengenai kode CSS diatas, dimulai dari selector pertama:
- **.content { }** : Memfokuskan elemen yang memiliki class **content**.
- **padding: 20px;** : Memberikan elemen target **padding** dengan value **20px**.

Penjelasan selector kedua:
- **.content h2 { }** : Memfokuskan elemen yang memiliki class **content**, yang mana didalamnya terdapat tag `<h2>`. 
- **font-size: 28px;** : Memberikan ukuran font berupa **28px**.
- **font-weight: bold;** : Memberikan format berupa **bold**, sehingga font menjadi tebal.

Penjelasan selector ketiga:
- **.content .penulis { }** : Menargetkan elemen dengan class **content**, lalu fokuskan lagi ke elemen yang memiliki class **penulis**.
- **font-size: 11px;** : Memberikan ukuran font berupa **11px**.
- **margin-top: 5px;** : Memberikan jarak dari bagian atas dengan **margin-top** senilai **5px**.

Maka, ketika kode HTML kita jalankan, hasilnya adalah sebagai berikut:

![[7 Box Model Membuat Website Sederhana-8.png]]

## 10. Isi paragraf
Setelah bagian atas selesai, kita buat paragraf dengan merubah kode HTML menjadi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Box Model</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <div class="header">
            <h1 class="judul">My Website</h1>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Product</a></li>
                <li><a href="#">Service</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>

        <div class="hero"></div>
        <div class="content">
            <h2>Judul Artikel</h2>
            <p class="penulis">ditulis oleh<a href="#">Trihaji Khoerur Rohman</a> pada 12 Oktober 2024</p>
        
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores cum ea nemo ipsam quidem perspiciatis? Rerum, provident. Minima hic modi, labore iste possimus quidem sit, vel molestias itaque, et corporis?</p>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo magnam ipsum facilis perferendis. Tenetur ex consectetur repellendus maiores recusandae, saepe hic itaque soluta, ipsum quaerat laboriosam architecto. Distinctio, natus molestias! Laboriosam animi consequuntur quaerat vitae error debitis obcaecati veritatis nam unde. Quisquam non atque suscipit tempore tenetur minus natus voluptas quam beatae adipisci molestiae quo dignissimos corrupti, placeat error nihil doloremque eos ea autem minima quos! Sequi dignissimos molestias rerum pariatur laudantium unde? Eum deserunt labore, voluptate obcaecati nostrum ea odit molestiae, consequatur numquam velit magnam officia assumenda vel beatae. Maiores facilis totam numquam dolorem sapiente et aliquid qui temporibus?</p>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, voluptatum cum illo doloremque totam fugiat eius inventore enim excepturi nemo animi eum a iure odit quos recusandae hic nostrum earum aliquid laborum quasi. Cupiditate, optio at sit ex eius reprehenderit exercitationem illo nulla! Obcaecati saepe impedit nemo eos voluptate illo repellendus sapiente praesentium quae, explicabo id voluptas et. Consectetur, aliquid dicta. Explicabo dolore quia qui eveniet animi tempore molestiae officia, veniam a esse amet, totam corporis, veritatis iste voluptate alias!</p>
        
        </div>
    </div>

</body>
</html>
```

Disini, kita cukup menambahkan 3 paragraf dengan jumlah kata yang berbeda-beda.


> [!NOTE] Tips trick!
> Untuk bisa menambahkan paragraf secara sepintas, mudah saja. Pertama, karena kita menggunakan Visual Studi Code, kita hanya perlu instal plugin CSS terlebih dahulu. Setelah itu, ketika ingin mengetikan paragraf, ketik saja dengan **lorem**, lalu enter. Maka secara otomatis akan terbuat satu paragraf.
> 
> Jika ingin membuat paragraf dengan jumlah kata tertentu, kita bisa mengetikanya seperti ini: **lorem100**. Maka akan tercetak paragraf dengan 100 kata. Tinggal ketik saja jumlah kata yang kita inginkan dibelakang kata **lorem**.

Lalu, tambahkan kode CSS berikut:

```css
.content .penulis a {
    color: salmon;
    text-decoration: none;
}

.content p {
    margin-bottom: 20px;
    font-size: 14px;
}
```

Keterangan selector pertama:
- **.content .penulis a { }** : Menarget elemen yang memiliki class **content**, yang didalamnya terdapat elemen dengan class **penulis**, yang menggunakan tag `<a>`.
- **color: salmon;** : Memberikan warna link menjadi warna *salmon*.
- **text-decoration: none;** : Menghilangkan dekorasi pada link, sehingga tidak lagi memiliki *underline*.

Keterangan selector kedua:
- **.content p { }** : Menargetkan elemen yang memiliki class **content**, yang memiliki tag `<p>`.
- **margin-bottom: 20px;** : Buat setiap tag `<p>` memiliki **margin** bagian bawah sebesar **20px**. Ini digunakan supaya setiap paragraf memiliki jarak yang cukup.
- **font-size: 14px;** : Merubah teks yang ada didalamnya (teks paragraf)  agar memiliki ukuran sebesar **14px**.

Maka, hasilnya sudah sampai disini:

![[7 Box Model Membuat Website Sederhana-9.png]]

## 11. Footer copyright
Sekarang, kita tambahkan bagian terakhir, yaitu bagian **footer**. Sekarang rubah kode HTML kita menjadi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Box Model</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <div class="header">
            <h1 class="judul">My Website</h1>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Product</a></li>
                <li><a href="#">Service</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>

        <div class="hero"></div>
        <div class="content">
            <h2>Judul Artikel</h2>
            <p class="penulis">ditulis oleh<a href="#">Trihaji Khoerur Rohman</a> pada 12 Oktober 2024</p>
        
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores cum ea nemo ipsam quidem perspiciatis? Rerum, provident. Minima hic modi, labore iste possimus quidem sit, vel molestias itaque, et corporis?</p>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo magnam ipsum facilis perferendis. Tenetur ex consectetur repellendus maiores recusandae, saepe hic itaque soluta, ipsum quaerat laboriosam architecto. Distinctio, natus molestias! Laboriosam animi consequuntur quaerat vitae error debitis obcaecati veritatis nam unde. Quisquam non atque suscipit tempore tenetur minus natus voluptas quam beatae adipisci molestiae quo dignissimos corrupti, placeat error nihil doloremque eos ea autem minima quos! Sequi dignissimos molestias rerum pariatur laudantium unde? Eum deserunt labore, voluptate obcaecati nostrum ea odit molestiae, consequatur numquam velit magnam officia assumenda vel beatae. Maiores facilis totam numquam dolorem sapiente et aliquid qui temporibus?</p>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, voluptatum cum illo doloremque totam fugiat eius inventore enim excepturi nemo animi eum a iure odit quos recusandae hic nostrum earum aliquid laborum quasi. Cupiditate, optio at sit ex eius reprehenderit exercitationem illo nulla! Obcaecati saepe impedit nemo eos voluptate illo repellendus sapiente praesentium quae, explicabo id voluptas et. Consectetur, aliquid dicta. Explicabo dolore quia qui eveniet animi tempore molestiae officia, veniam a esse amet, totam corporis, veritatis iste voluptate alias!</p>
        </div>
        <div class="footer">
            <p class="copy">Copyright 2024 | By Trihaji Khoereur Rohman | Made by Love</p>
        </div>
    </div>

</body>
</html>
```

Kode HTML diatas adalah menambahkan elemen baru untuk **footer**. Lalu kita buat kode CSS berikut:

```css
.footer {
    background-color: #333;
    padding: 10px;
}

.footer .copy {
    color: #eaeaea;
    text-align: center;
    font-size: 12px;
}
```

Keterangan selector pertama:
- **.footer { }** : Menargetkan elemen dengan class **footer**.
- **background-color: #333;** : Memberi warna background untuk elemen footer, berupa warna abu-abu tua, yang dituliskan dengan *\#333*.
- **padding: 10px;** : Memberi padding pada elemen **footer** sebesar **10px**, artinya semua elemenya akan melebar **10px**.

Keterangan selector kedua:
- **.footer .copy { }**: Menargetkan elemen dengan class **footer**, lalu cari yang didalamnya terdapat elemen dengan class **copy**.
- **color: \#eaeaea;** : Memberi warna kepada teks berupa putih keabu-abuan.
- **text-align: center;** : Mengatur posisi teks / elemen terkait, agar berada di posisi tengah.
- **font-size: 12px;** : Mengatur ukuran font menjadi **12px**.

Maka, hasilnya akan menjadi seperti ini:

![[7 Box Model Membuat Website Sederhana-10.png]]

## 12. Background artikel
Sepertinya akan jauh lebih menarik jika kita membuat perbaikan, dengan menambahkan background pada keseluruhan artikel. Disini, kita akan menggunakan background berupa gambar yang disediakan oleh situs [subtlepaterns](https://www.toptal.com/designers/subtlepatterns/). Lalu kita unduh salah satu, pindahkan ke folder yang sama dengan HTML.

Kira-kira inilah yang akan kita gunakan sebagai pola:

![[marocan.png]]

Lalu, kita ubah kode CSS bagian `<body>` menjadi seperti ini:

```css
body {
    font: 16px/18px arial, sans-serif;
    background-color: #eaeaea;
    color: #333;
	
	/* penambahan */
    background-image:url(marocan.png);
}
```

Keterangan:
- **background-image:url(marocan.png);** : Untuk menambahkan background berupa file gambar dengan nama file **marocan.png** ke dalam elemen **body**. 

Maka hasilnya akan menjadi seperti ini:

![[7 Box Model Membuat Website Sederhana-11.png]]

---
Oke, kita sudah selesai pada pelajaran kali ini. Kalian bisa rubah kode-kode diatas agar bisa menghasilkan output sesuai selera kalian. Setidaknya tampilan web ini sudah cukup bagus untuk pemula. 

Terima kasih sudah mengikuti pelajaran dengan sangat baik, sampai jumpa di pembelajarran selanjutnya 👍

# Kode yang dipakai keseluruhan
## Kode HTML
Berikut kode HTML yang digunakan:

```HTML
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Box Model</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <div class="header">
            <h1 class="judul">My Website</h1>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Product</a></li>
                <li><a href="#">Service</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>

        <div class="hero"></div>
        <div class="content">
            <h2>Judul Artikel</h2>
            <p class="penulis">ditulis oleh<a href="#">Trihaji Khoerur Rohman</a> pada 12 Oktober 2024</p>
        
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores cum ea nemo ipsam quidem perspiciatis? Rerum, provident. Minima hic modi, labore iste possimus quidem sit, vel molestias itaque, et corporis?</p>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo magnam ipsum facilis perferendis. Tenetur ex consectetur repellendus maiores recusandae, saepe hic itaque soluta, ipsum quaerat laboriosam architecto. Distinctio, natus molestias! Laboriosam animi consequuntur quaerat vitae error debitis obcaecati veritatis nam unde. Quisquam non atque suscipit tempore tenetur minus natus voluptas quam beatae adipisci molestiae quo dignissimos corrupti, placeat error nihil doloremque eos ea autem minima quos! Sequi dignissimos molestias rerum pariatur laudantium unde? Eum deserunt labore, voluptate obcaecati nostrum ea odit molestiae, consequatur numquam velit magnam officia assumenda vel beatae. Maiores facilis totam numquam dolorem sapiente et aliquid qui temporibus?</p>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, voluptatum cum illo doloremque totam fugiat eius inventore enim excepturi nemo animi eum a iure odit quos recusandae hic nostrum earum aliquid laborum quasi. Cupiditate, optio at sit ex eius reprehenderit exercitationem illo nulla! Obcaecati saepe impedit nemo eos voluptate illo repellendus sapiente praesentium quae, explicabo id voluptas et. Consectetur, aliquid dicta. Explicabo dolore quia qui eveniet animi tempore molestiae officia, veniam a esse amet, totam corporis, veritatis iste voluptate alias!</p>
        </div>
        <div class="footer">
            <p class="copy">Copyright 2024 | By Trihaji Khoereur Rohman | Made by Love</p>
        </div>
    </div>

</body>
</html>
```

## Kode CSS
Berikut kode CSS yang digunakan:

```css
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}

/* pemberian style */

.container {
    width: 800px;
    margin: auto;
    background-color: white;
}

body {
    font: 16px/18px arial, sans-serif;
    background-color: #eaeaea;
    color: #333;

    background-image:url(marocan.png);
}

.header {
    padding: 20px;
}

.header .judul {
    font-size: 40px;
    font-weight: bold;
}

.header ul li {
    display: inline-block;
    margin-top: 20px;
    margin-right: 10px;
}

.header a {
    text-decoration: none;
    color: salmon;
    padding: 3px;
}

.header a:hover {
    background-color: lightskyblue;
    color: white;
}

.hero {
    height: 280px;
    background-image: url(heroimage.jpg);
    background-size: cover;
    background-position: 0 -70px;
    border-top: 5px solid salmon;
    border-bottom: 5px solid lightskyblue;
}

.content {
    padding: 20px;
}

.content h2 {
    font-size: 28px;
    font-weight: bold;
}

.content .penulis {
    font-size: 11px;
    margin-top: 5px;
}

.content .penulis a {
    color: salmon;
    text-decoration: none;
}

.content p {
    margin-bottom: 20px;
    font-size: 14px;
}

.footer {
    background-color: #333;
    padding: 10px;
}

.footer .copy {
    color: #eaeaea;
    text-align: center;
    font-size: 12px;
}
```