---
obsidianUIMode: preview
sumber: WPU
level: medium
bahasa: CSS
tanggal_study: 2024-10-14T13:59:00
total_study: 1
tags:
  - CSS
id: WPUCSSLOT10
---
# Website Sederhana part 2

Kali ini, kita akan membuat desain website sederhana yang kita kembangkan lagi dari desain kita website sebelumnya. Kira-kira desain website yang kita buat akan seperti ini:

![[10 Website sederhana (Part 2)-1.png]]

Dengan ukuran sebagai berikut:

![[10 Website sederhana (Part 2)-2.png]]

## Pendahuluan
Karena kita akan menggunakan source code website sebelumnya, maka sebagai pengingat, berikut kode HTML dan CSSnya. 

Kode HTML:

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

Berikut kode CSS:

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

## 1. Rubah lebar website
Baiklah, langkah pertama dalam pembuatan website kali ini adalah melebarkan **container**-nya, menjadi seperti ini:


--- start-multi-column: ID_s5mx
```column-settings
Number of Columns: 2
Largest Column: standard
```

Sebelum:

```css
.container {
    width: 800px;
    margin: auto;
    background-color: white;
}
```

--- column-break ---

Sesudah:

```css
.container {
    width: 960px;
    margin: auto;
    background-color: white;
}
```

--- end-multi-column
Maka, lebar containernya menjadi bertambah menjadi seperti ini:

![[10 Website sederhana (Part 2)-3.png]]

Karena kita menggunakan **background-size** berupa **cover**, maka sekarang tinggi hero image nya terlalu kecil. Maka kita perlu ubah tingginya, agar gambarnya muat. 

Selain itu, kita juga harus mengatur posisi gambar supaya menjadi lebih ditengah, ketika kita melebarkan dimensinya menjadi lebih tinggi.

Kita ubah CSS nya menjadi seperti ini:
--- start-multi-column: ID_l7js
```column-settings
Number of Columns: 2
Largest Column: standard
```

Sebelum:

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

--- column-break ---

Sesudah:

```css
.hero {
    height: 320px;
    background-image: url(heroimage.jpg);
    background-size: cover;
    background-position: 0 -130px;
    border-top: 5px solid salmon;
    border-bottom: 5px solid lightskyblue;
}
```

--- end-multi-column
Maka, hasilnya akan menjadi seperti ini:

![[10 Website sederhana (Part 2)-4.png]]

## 2. membuat 2 dimensi
Kita perlu mengubah kode HTML kita, agar terdapat 2 elemen, yaitu elemen untuk menampung artikel atau elemen **main**, dan juga elemen yang akan berada di pinggir atau elemen **sidebar**.

Rubah kode HTML menjadi seperti ini:

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

            <div class="main">
                <h2>Judul Artikel</h2>
                <p class="penulis">ditulis oleh<a href="#">Trihaji Khoerur Rohman</a> pada 12 Oktober 2024</p>
            
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores cum ea nemo ipsam quidem perspiciatis? Rerum, provident. Minima hic modi, labore iste possimus quidem sit, vel molestias itaque, et corporis?</p>

                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo magnam ipsum facilis perferendis. Tenetur ex consectetur repellendus maiores recusandae, saepe hic itaque soluta, ipsum quaerat laboriosam architecto. Distinctio, natus molestias! Laboriosam animi consequuntur quaerat vitae error debitis obcaecati veritatis nam unde. Quisquam non atque suscipit tempore tenetur minus natus voluptas quam beatae adipisci molestiae quo dignissimos corrupti, placeat error nihil doloremque eos ea autem minima quos! Sequi dignissimos molestias rerum pariatur laudantium unde? Eum deserunt labore, voluptate obcaecati nostrum ea odit molestiae, consequatur numquam velit magnam officia assumenda vel beatae. Maiores facilis totam numquam dolorem sapiente et aliquid qui temporibus?</p>

                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, voluptatum cum illo doloremque totam fugiat eius inventore enim excepturi nemo animi eum a iure odit quos recusandae hic nostrum earum aliquid laborum quasi. Cupiditate, optio at sit ex eius reprehenderit exercitationem illo nulla! Obcaecati saepe impedit nemo eos voluptate illo repellendus sapiente praesentium quae, explicabo id voluptas et. Consectetur, aliquid dicta. Explicabo dolore quia qui eveniet animi tempore molestiae officia, veniam a esse amet, totam corporis, veritatis iste voluptate alias!</p>
            </div>

            <div class="sidebar">
                
            </div>

            
        </div>
        <div class="footer">
            <p class="copy">Copyright 2024 | By Trihaji Khoereur Rohman | Made by Love</p>
        </div>
    </div>

</body>
</html>
```

Diatas, kita menambahkan dua elemen utama, yaitu elemen **main**, untuk menampung artikel kita, dan elemen **sidebar**, yaitu elemen disebelah kanan elemen **main**.

Perhatikan juga bahwa artikel utama kita, tidak lagi dibungkus oleh elemen **content**, tetapi oleh elemen yang baru saja kita buat, yaitu elemen **main**, sehinggakita perlu mengedit kode CSS kita, supaya sesuai selectornya. Berikut perubahan kode CSS yang perlu dilakukan:

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
    width: 960px;
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
    height: 320px;
    background-image: url(heroimage.jpg);
    background-size: cover;
    background-position: 0 -130px;
    border-top: 5px solid salmon;
    border-bottom: 5px solid lightskyblue;
}

.main {
    padding: 20px;
}

.main h2 {
    font-size: 28px;
    font-weight: bold;
}

.main .penulis {
    font-size: 11px;
    margin-top: 5px;
}

.main .penulis a {
    color: salmon;
    text-decoration: none;
}

.main p {
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

> Shorthan : Dengan VS Code, blok tulisan **.content**, lalu tekan **ctrl + d**. Maka secara otomatis, kata serupa akan terblok, dan kita bisa mengganti semua kata tersebut secara bersamaan menjadi **.main**.

Setelah dirubah, ketika dijalankan lagi, maka tidak terjadi perubahan apapun dalam tampilan, kita hanya merubah susunan CSS saja agar kedepanya lebih rapi dan efisien.

## 3. membuat main
Kita perlu membuat space disebalah kanan, sehingga kita perlu mengedit kode CSS kita menjadi seperti ini pada selector **main**. Tujuanya adalah membuat elemen **main** tidak memiliki ukuran yang sama dengan elemen *parent*-nya:
--- start-multi-column: ID_3rob
```column-settings
Number of Columns: 2
Largest Column: standard
```

Sebelum:

```css
.main {
    padding: 20px;
}
```

--- column-break ---

Sesudah:

```css
.main {
    width: 600px;
    padding: 20px;
    box-sizing: border-box;
}
```

--- end-multi-column
Jangan lupa, beri properti **box-sizing** agar ukuranya tidak berubah, karena kita juga menambahkan properti **padding** didalamnya.

Maka, sekarang tampilan elemen **main** akan berubah menjadi seperti ini:

![[10 Website sederhana (Part 2)-6.png]]

Sekarang, kita juga perlu menambahkan properti **float** kedalam elemen **main**. Ingat, ketika kita menambahkan properti **float** kepada suatu elemen, maka elemen pembungkusnya akan menganggap bahwa elemen itu tidak ada, atau tidak berada dalam satu **flow** yang sama, sehingga terjadi *collapse*.


--- start-multi-column: ID_ik77
```column-settings
Number of Columns: 2
Largest Column: standard
```

Sebelum:

```css
.main {
    width: 600px;
    padding: 20px;
    box-sizing: border-box;
}
```

--- column-break ---

Sesudah:

```css
.main {
    width: 600px;
    padding: 20px;
    box-sizing: border-box;
    float: left;
}
```

--- end-multi-column
Maka hasilnya akan terjadi colllapse:

![[10 Website sederhana (Part 2)-7.png]]

Bisa terlihat jelas disitu, bahwa elemen **footer** bahkan sampai naik keatas, karena kita menggunakan properti **float** tadi.

Solusinya adalah kita menggunakan **micro clearfix**, untuk menghentikan **float**-nya. Kita berikan teknik ini ke elemen **content**, sebagai pembungkus dari elemen **main** dan **sidebar**. Sekarang kita copy paste syntaxnya, kita taruh dibagian paling akhir CSS atau dimanapun itu, sehingga menjadi seperti ini:

```css
/* micro clearfix */
.cf:before,
.cf:after {
    content: " "; /* 1 */
    display: table; /* 2 */
}

.cf:after {
    clear: both;
}

.cf {
    *zoom: 1;
}
```

Tidak lupa juga, kita edit halaman HTML agar bisa terhubung dengan selector **cf** yang kita buat:


--- start-multi-column: ID_siuq
```column-settings
Number of Columns: 2
Largest Column: standard
```

Sebelum:

```html
<div class="content">
```

--- column-break ---

Sesudah:

```html
<div class="content cf">
```

--- end-multi-column
Sehingga, outputnya adalah **footer** akan kembali ke bawah seperti ini:

![[10 Website sederhana (Part 2)-8.png]]

## 4. Membuat sidebar
Sekarang, kita akan fokus untuk membuat elemen **sidebar**. Berikut adalah apa yang harus kita lakukan.

Pertama, kita perlu menentukan tujuan dari elemen **sidebar**. Jadi kita akan menentukan bahwa elemen sidebar akan kita gunakan untuk menaruh profil dan keterangan dari penulis. Dimana kita meletakan gambar dan juga beberapa patah kata didalmnya.

Sekarang kita edit file HTML kita, kita fokuskan saja perubahan kode HTML pada elemen **sidebar**:

Sebelum: 

```html
<div class="sidebar"></div> 
```

Sesudah:
> Jangan lupa, edit ukuran gambar agar sesuai, bisa diedit di potoshop supaya tidak perlu mengatur **width** dan **height**-nya, atau edit langsung di HTML

```html
<div class="sidebar">
	<h3>Tentang penulis</h3>
	<img src="img/editanprofil.png" width="100px" height="100px" alt="Trihaji Khoerur Rohman">
</div>
```

Hasilnya:

![[10 Website sederhana (Part 2)-9.png]]

Sekarang, kita buat ukuran **sidebar** dengan kode CSS berikut:

```css
/* sidebar */
.sidebar {
    width: 300px;
}
```

Maka hasilnya:

![[10 Website sederhana (Part 2)-10.png]]

Tunggu, kenapa gambarnya malah jadi dibawah? Ini karena kita belum menambahkan properti **float** pada sidebar. Rubah lagi kode CSS menjadi seperti ini:

```css
/* sidebar */
.sidebar {
    width: 300px;
    float: right;
    padding: 20px;
}
```

Sehingga hasilnya menjadi seperti ini:

![[10 Website sederhana (Part 2)-11.png]]

Sekarang, kita edit judul "tentang penulis" atau tag h3 menjadi seperti ini dengan kode CSS:

```css
.sidebar h3 {
    font-weight: bold;
    color: #666;
}

.sidebar img {
    width: 70px;
    height: 70px;
}
```

Maka, hasilnya menjadi seperti ini:
--- start-multi-column: ID_nn6o
```column-settings
Number of Columns: 2
Largest Column: standard
```

Sebelum:

![[10 Website sederhana (Part 2)-12.png]]

--- column-break ---

Sesudah: 

![[10 Website sederhana (Part 2)-13.png]]

--- end-multi-column

Sekarang, kita akan membuat teks yang mengelilingi gambar, kita edit kode HTML menjadi seperti ini, tambahkan 1 paragraf atau keterangan tentang penulis dibawah tag img:

```html
 <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo beatae similique, fugit enim perferendis pariatur repudiandae blanditiis. Nihil, provident debitis eaque, ex pariatur, vitae tempore saepe eum assumenda perspiciatis placeat!</p>
```

Lalu kita perbaiki kode CSS **sidebar** kita menjadi seperti ini.
Menjadi seperti ini:

```css
/* sidebar */
.sidebar {
    width: 300px;
    float: right;
    padding: 20px;
}

.sidebar h3 {
    font-weight: bold;
    color: #666;
    margin-bottom: 10px;
}

.sidebar img {
    width: 70px;
    height: 70px;
    float: left;
    padding-right: 10px;
}

.sidebar p {
    font: 12px/18px arial;
}
```

Perubahan diatas menyertakan:
- Membuat font "tentang penulis" lebih menarik dengan memiliki format **bold**, dan warna abu-abu gelap
- Membuat gambar memiliki ukuran **70x70px**, memiliki properti **float** dengan value *left*, dan padding disebelah kanan dengan ukurang **10px**.
- Membuat paragraf yang digunakan untuk memberi keterangan penulis, berukuran **12px**, dengan **line-height** berupa **18px**, dan memiliki font berupa **arial**.

Maka, hasilnya finalnya seperti ini:

![[10 Website sederhana (Part 2)-15.png]]

---
## Hasil akhir kode program
Kode HTML: 

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
        <div class="content cf">

            <div class="main">
                <h2>Judul Artikel</h2>
                <p class="penulis">ditulis oleh<a href="#">Trihaji Khoerur Rohman</a> pada 12 Oktober 2024</p>
            
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores cum ea nemo ipsam quidem perspiciatis? Rerum, provident. Minima hic modi, labore iste possimus quidem sit, vel molestias itaque, et corporis?</p>

                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo magnam ipsum facilis perferendis. Tenetur ex consectetur repellendus maiores recusandae, saepe hic itaque soluta, ipsum quaerat laboriosam architecto. Distinctio, natus molestias! Laboriosam animi consequuntur quaerat vitae error debitis obcaecati veritatis nam unde. Quisquam non atque suscipit tempore tenetur minus natus voluptas quam beatae adipisci molestiae quo dignissimos corrupti, placeat error nihil doloremque eos ea autem minima quos! Sequi dignissimos molestias rerum pariatur laudantium unde? Eum deserunt labore, voluptate obcaecati nostrum ea odit molestiae, consequatur numquam velit magnam officia assumenda vel beatae. Maiores facilis totam numquam dolorem sapiente et aliquid qui temporibus?</p>

                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, voluptatum cum illo doloremque totam fugiat eius inventore enim excepturi nemo animi eum a iure odit quos recusandae hic nostrum earum aliquid laborum quasi. Cupiditate, optio at sit ex eius reprehenderit exercitationem illo nulla! Obcaecati saepe impedit nemo eos voluptate illo repellendus sapiente praesentium quae, explicabo id voluptas et. Consectetur, aliquid dicta. Explicabo dolore quia qui eveniet animi tempore molestiae officia, veniam a esse amet, totam corporis, veritatis iste voluptate alias!</p>
            </div>

            <div class="sidebar">
                <h3>Tentang penulis</h3>
                <img src="img/editanprofil.png" width="100px" height="100px" alt="Trihaji Khoerur Rohman">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo beatae similique, fugit enim perferendis pariatur repudiandae blanditiis. Nihil, provident debitis eaque, ex pariatur, vitae tempore saepe eum assumenda perspiciatis placeat!</p>
            </div>

            
        </div>
        <div class="footer">
            <p class="copy">Copyright 2024 | By Trihaji Khoereur Rohman | Made by Love</p>
        </div>
    </div>

</body>
</html>
```

Kode CSS:

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
    width: 960px;
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
    height: 320px;
    background-image: url(heroimage.jpg);
    background-size: cover;
    background-position: 0 -130px;
    border-top: 5px solid salmon;
    border-bottom: 5px solid lightskyblue;
}

.main {
    width: 600px;
    padding: 20px;
    box-sizing: border-box;
    float: left;
}

.main h2 {
    font-size: 28px;
    font-weight: bold;
}

.main .penulis {
    font-size: 11px;
    margin-top: 5px;
}

.main .penulis a {
    color: salmon;
    text-decoration: none;
}

.main p {
    margin-bottom: 20px;
    font-size: 14px;
}

/* sidebar */
.sidebar {
    width: 300px;
    float: right;
    padding: 20px;
}

.sidebar h3 {
    font-weight: bold;
    color: #666;
    margin-bottom: 10px;
}

.sidebar img {
    width: 70px;
    height: 70px;
    float: left;
    padding-right: 10px;
}

.sidebar p {
    font: 12px/18px arial;
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

/* micro clearfix */
.cf:before,
.cf:after {
    content: " "; /* 1 */
    display: table; /* 2 */
}

.cf:after {
    clear: both;
}


```

Mungkin sekian pelajaran kali ini, semoga mudah dipahami, dan selamat berkreasi untuk membuat website sendiri! 👍



