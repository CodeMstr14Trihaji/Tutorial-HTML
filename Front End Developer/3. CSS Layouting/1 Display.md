---
obsidianUIMode: preview
sumber: WPU
level: sulit
bahasa: CSS
tanggal_study: 2024-10-11T18:10:00
total_study: 1
tags:
  - CSS
id: WPUCSSLOT2
sr-due: 2024-10-12
sr-interval: 1
sr-ease: 130
---
# CSS Display
Sebenarnya, topik paling penting dalam CSS Layouting ada 3, yaitu *box model*, *float*, dan *positioning*. Tapi ketiga topik tadi membutuhkan pemahaman dasar dari perilaku tiap-tiap elemen HTML yang akan ditampilkan didalam website. Pemahaman dasar ini akan kita bagi menjadi 3, yaitu *display*, *dimensi*, dan *overflow*.

Dan sekarang kita akan pelajari dahulu tentang **Display**.
## Pemahaman tag \<div> dan \<span> 
Tag pada HTML digunakan untuk memberikan 'maksud' atau 'arti' pada sebuah konten (**p** untuk paragraf, **h1** untuk heading utama, dll).

Tag `<div>` dan `<span>` tidak memiliki 'arti' apapun, keduanya digunakan untuk mengelompokan tag-tag HTML dan memberikan informasi terhadap tag-tag tersebut.

Sebagai contoh, perhatikan kode HTML berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Display</title>
    <meta charset="utf-8"/>
</head>
<body>
    <h1>Selamat Datang Di Website Kami</h1>

    <h2>Daftar link</h2>
    <a href="#">Link 1</a>
    <a href="#">Link 2</a>
    <a href="#">Link 3</a>
    <a href="#">Link 4</a>

    <h2>Judul Artikel</h2>
    <img src="pngegg.png" alt="Logo Real Madrid" width="230" height="230">

    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque sequi doloribus ducimus iure, id quibusdam itaque voluptatibus repellat ratione eius? Rem fuga at obcaecati possimus dolores porro doloremque molestias necessitatibus?</p>

    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum, officiis aperiam? Ratione quae, ullam alias illum qui quia dicta doloremque ipsa maiores tenetur tempora beatae, quidem accusamus quasi ea eum.</p>

    <p class="copyright">copyright 2024 | Made by Love</p>
</body>
</html>
```

Biasanya, programmer akan mengelompokan beberapa bagian dalam isi HTML dengan menggunakan bantuan tag `<div>`, atau `<span>`. Seperti mengelompokan bagian sidebar, header, footer, dll. Baik, sekarang mari kita rubah kode HTML, menjadi lebih rapi lagi, dengan mengelompokanya dengan menggunakan tag `<div>` sebagai berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Display</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="header">
        <h1>Selamat Datang Di Website Kami</h1>
    </div>
   
    <div class="navigasi">
        <h2>Daftar link</h2>
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
        <a href="#">Link 4</a>
    </div>

    <div class="main">
        <h2>Judul Artikel</h2>
        <img src="pngegg.png" alt="Logo Real Madrid" width="230" height="230">
    
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. <span>Neque sequi doloribus ducimus iure, id quibusdam itaque voluptatibus</span> repellat ratione eius? Rem fuga at obcaecati possimus dolores porro doloremque molestias necessitatibus?</p>
    
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum, officiis aperiam? Ratione quae, ullam alias illum qui quia dicta doloremque ipsa maiores tenetur tempora beatae, quidem accusamus quasi ea eum.</p>
    
    </div>

    <div class="footer">
        <p class="copyright">copyright 2024 | Made by Love</p>
    </div>

</body>
</html>
```

Diatas, kita membuat pengelompokan menggunakan tag `<di>`, yang terdiri dari *header*, *navigasi*, *main*, dan *footer*. Kita juga menggunakan tag `<span>` untuk mengapit beberapa text.

Setelah itu, mari kita beri kode CSS, dengan kode sebagai berikut:

```css
.navigasi{
    background-color: pink;
}

.main{
    background-color: lightgreen;
}

.main span{
    background-color: lightblue;
}
```

Maka, ketika dijalankan, hasilnya akan seperti berikut:

![[1 Display-1.png|500]]

Walaupun tag `<div>` dan `<span>` tidak sama secara semantik, kedua tag ini bisa digunakan untuk mengelompokan.
## Hubunganya dengan display?
Semua elemen HTMl itu memiliki properti display default. Lalu bagaimana dengan kedua tag sebelumnya yang sudah kita pelajari?

Tag `<div>`, memiliki default display berupa **block**:

```css
div {
display: block;
}
```

Sedangkan tag `<span>`, memiliki default display berupa **inline**:

```css
span {
display: inline;
}
```

Apa itu maksudnya? Baiklah, sekarang kita akan benar-benar memasuki topik display.
### Display tambahan informasi
Menurut css-tricks.com, setiap tag HTML berada didalam sebuah **kotak**. Properti **display** pada CSS mengatur perilaku dari kotak tersebut. 

Menurut developer.mozilla.org, setiap tag pada HTML memiliki nilai default untuk properti **display**. Tetapi kita juga dapat mengubah perilaku dari tag tersebut dengan mengganti value-nya.

Nah, value dari display itu sendiri ada 4, yaitu:
- **inline**
- **inline-block**
- **block**
- **none**

Mari kita bahas satu-persatu
## inline
Berikut adalah sifat-sifat dari inline:
- Elemen HTML yang secara default tidak menambahkan baris baru ketika dibuat.
- Lebar dan tinggi elemenya sebesar konten yang ada di dalamnya.
- Kita tidak dapat mengatur tinggi dan lebar dari elemen inline
- *Margin dan padding hanya memengaruhi elemen secara horizontal, tidak vertikal*.

Contoh elemen dalam HTML yang memiliki default inline:
- b
- strong
- i
- em
- a
- span
- sup
- sub
- button
- input
- label
- select
- textarea

Jika kita menggunakan tag-tag diatas, ketika dimunculkan pada browser, maka elemen tersebut akan muncul dalam satu baris jika masih ada space, itulah kenapa disebut **inline**. tag `<img>` juga memiliki nilai default **inline**, namun tag tersebut adalah satu-satunya tag dengan nilai display **inline** yang dapat diubah-ubah ukuranya.

Bukti jika tag `<a>` memiliki default display **inline**:

![[1 Display-2.png]]

Jika kita membuat kode HTML untuk memunculkan link diatas seperti ini:

```html
        <a href="#">Link 1</a>
        <a href="#">Link 2</a>
        <a href="#">Link 3</a>
        <a href="#">Link 4</a>
```

Maka, link yang tampil bukan turun kebawah, melainka ke samping jika ada space kosong. Ini sesuai seperti aturan no 1.  Selain tidak turun ke bawah, elemen yang memiliki default display inline tidak bisa diatur tinggi dan lebarnya.  Dan lebar inline akan tetap sama dengan lebar elemenya. Contohnya seperti berikut:

Rubah kode CSS:

```css
div.navigasi a{
    background-color: pink;
}

.main{
    background-color: lightgreen;
}

.main span{
    background-color: lightblue;
}
```

Maka, background yang terbentuk akan mengikuti lebar elemen, ini sesuai dengan aturan nomor 2:
![[1 Display-3.png]]

Pertanyaanya sekarang, apakah bisa kita merubah default display pada suatu tag? Tentu bisa, yaitu dengan menggunakan valur yang kedua, yaitu **inline-block**.
## inline-block
Berikut teori tentang inline-block:
- Tidak ada elemen yang secara defafult memiliki properti *display: inline-block;*
- Kita harus ubah secara manual properti tersebut
- Perilaku dasarnya sama dengan elemen inline
- Perbedaanya, elemen inline-block dapat kita atur tinggi dan lebar-nya.

Kita rubah kode CSS sebelumnya:

```css
div.navigasi a{
    background-color: pink;
    width: 100px;
    height: 100px;
}

.main{
    background-color: lightgreen;
}

.main span{
    background-color: lightblue;
}
```

Jika kita jalankan lagi kode HTML, Loh? Kenapa tidak ada perubahan? 
Hal ini terjadi karena kita masih kekurangan satu baris kode lagi, yaitu menambahkan **inline-block**:

```css
div.navigasi a{
    background-color: pink;
    width: 100px;
    height: 100px;
    display: inline-block;
}

.main{
    background-color: lightgreen;
}

.main span{
    background-color: lightblue;
}
```

Setelah kita menambahkan property **display**, dengan value **inline-block**, maka backgound link dapat kita atur ukuranya, menjadi seperti dibawah ini: 

![[1 Display-4.png]]

## block
Berikut materi tentang **block**:
- Elemen HTML yang secara default menambahkan baris baru ketika dibuat.
- Jika tidak diatur lebar-nya, maka lebar default dari elemen block akan memenuhi lebar dari browser / parent-nya.
- Kita dapat mengatu tinggi dan lebar dari elemen block.
- Didalam elemen block, kita dapat menyimpan tag dengan elemen inline, inline-block, atau bahkan elemen block lagi.

Contoh elemen HTML yang memiliki default display **block**:
- h1-h6
- p
- ol
- ul
- li
- form
- hr
- div

Dengan kode HTML yang sama, kita cukup buktikan elemen dengan display default **block** dengan menampilkanya dengan kode CSS:

```css
h1, h2, p {
    background-color: lightgreen;
}
```

Maka hasilnya adalah sebagai berikut:

![[1 Display-5.png]]

Sekarang mari kita coba rubah selector `main`, rubah kode CSS lagi menjadi seperti ini:

```css
.main {
    background-color: lightgreen;
    width: 500px;
    height: 600px;
}

h2 {
    background-color: blue;
}
```

Maka, hasilnya:
![[1 Display-6.png]]

Lihat, kita bisa mengatur ukuran block dari tag `<div>` yang memiliki *class 'main'*. Juga perhatikan lagi, bahwa ketika kita memberi style pada tag `<h2>`, tag h2 yang berada diluar class *main* akan memiliki background warna yang memenuhi sepanjang browser. Sedangkan tag h2 yang berada didalam tag dengan class *main*, hanya bisa memenuhi sampai pembungkusnya saja, atau containernya saja, tidak seluruh browser.  

Hal ini terjadi, karena saat kita menentukan batasan **width** dan **height** pada class main, kita juga menentukan batasan pada tag-tag atau *child* yang ada didalamnya.
## none
Berikut teori tentang **none**:
- Digunakan untuk menghilangkan sebuah elemen.

Coba tuliskan kode CSS berikut:

```css
.main {
    background-color: lightgreen;
    width: 500px;
    height: 600px;
}

h2 {
    background-color: blue;
}

img {
    display: none;
}
```

Perhatikan, kita menambahkan selector `img` dan membuat properti `display` dengan value `none`. Lihatt hasilnya, maka elemen akan dihilangkan:

![[1 Display-7.png]]

## Merubah display
Contoh kasus, kita membuat link didalam tag list, tapi kita ingin membuatnya tampil dalam satu baris, maka kita bisa membuatnya seperti berikut:

Kode HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Kode CSS</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="header">
        <h1>Belajar Display CSS</h1>
    </div>
    
    <div class="navigasi">
        <ul>
            <li><a href="#">Link 1</a></li>
            <li><a href="#">Link 2</a></li>
            <li><a href="#">Link 3</a></li>
            <li><a href="#">Link 4</a></li>
            <li><a href="#">Link 5</a></li>
        </ul>
    </div>
</body>
</html>
```

Tanpa kode CSS, maka tampilanya akan seperti ini:

![[1 Display-8.png]]

Tapi dengan menambahkan kode CSS sebgai berikut, kita bisa merubah urutan penampilan link, menjadi berbaris, dengan merubah default displaynya menjadi **inline**:

```css
.navigasi li{
    display: inline;
}
```

Maka, tampilanya akan menjadi seperti ini:

![[1 Display-9.png]]

---
Oke, mungkin sekia materi tentang **display** pada kesempatan kali ini, semoga mudah dipahami. Teruslah belajar!!