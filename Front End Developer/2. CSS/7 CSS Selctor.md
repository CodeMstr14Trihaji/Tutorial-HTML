---
obsidianUIMode: preview
sumber: WPU
level: medium
bahasa: CSS
tanggal_study: 2024-10-10T18:18:00
total_study: 1
tags:
  - CSS
id: WPUCSSD7
sr-due: 2024-10-11
sr-interval: 1
sr-ease: 130
---
# CSS Selctor
Pada pembelajaran pertama, kita sudah belajar bagaimana cara menggunakan selector. Namun pembelajaran kali ini, kita akan mempelajari selector lebih dalam.

Menurut W3schools, Selector digunakan pada CSS untuk mengenali sebuah elemen HTML yang akan diberi style. 

Ada beberapa seletor yang bisa digunakan, yaitu:
- elemen HTML (yang sudah kita pelajari sebelumnya)
- id (selector yang kita buat sendiri)
- class (selector yang kita buat sendiri)
- complex selector

Baiklah, saatnya belajar!
## Penggunaan Selector mengunakan Elemen HTML
Buat kode HTML seperti berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Belajar Selector CSS</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Belajar Selector CSS</h1>
    <p>Lihatlah dan pahami link-link berikut:</p>
    <p>
        <ul>
            <li><a href="#">Link 1</a></li>
            <li><a href="#">Link 2</a></li>
            <li><a href="#">Link 3</a></li>
            <li><a href="#">Link 4</a></li>
            <li><a href="#">Link 5</a></li>
        </ul>
    </p>
    <p>
        <ol>
            <li><a href="#">Link 6</a></li>
            <li><a href="#">Link 7</a></li>
            <li><a href="#">Link 8</a></li>
            <li><a href="#">Link 9</a></li>
            <li><a href="#">Link 10</a></li>
        </ol>
    </p>
    <p>
        <a href="https://www.youtube.com">Youtube Play</a>
    </p>

<h2>Judul artikel Subheading</h2>

    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat et eum at exercitationem ullam laboriosam perferendis sed quisquam aliquam. Incidunt, hic amet inventore sit maxime illo ducimus excepturi. Eligendi, dolor!</p>

    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis sed voluptate odio suscipit eaque. Cumque hic adipisci tenetur sequi distinctio facere at dolor incidunt. Maiores est porro repellendus perferendis magni.
    </p>
</body>
</html>
```

Disini, kita bisa membuat style CSS dengan nama file *style.css*, dan menambahkan kode ini didalamnya:

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}

h1{
    color: green;
}

h2{
    color: green;
}

```

Baiklah, diatas, kita mencoba memberi style pada tag body, h1, dan h2. Sebenarnya, jika kita memberikan style yang sama, kita bisa menggabungkan selector dengan cara berikut:

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}

h1, h2 {
    color: green;
}

```

Sekarang, jalankan file HTML tersebut, maka hasilnya akan seperti ini:

![[7 CSS Selctor-1.png]]

Oke, kita berhasil merubah style pada tag h1, dan h2, serta merubah font yang digunakan pada tag body.

### Keterbatasan penggunaan selector dengan nama Tag 
Bayangkan jika kamu ingin merubah  style hanya pada **link 1**, kita tidak bisa menggunakan selector dengan nama tagnya yaitu `<a>`, karena itu akan merubah keseluruhan style link pada semua halaman.

Jika kita menuliskan kode CSS seperti ini:

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}

h1, h2 {
    color: green;
}

a {
    color: orange;
}
```

Maka, akan membuat semua link berubah menjadi satu style seperti ini:

![[7 CSS Selctor-2.png]]

Kita mungkin masih bisa merubah 5 link pertama untuk memiliki satu style, dengan cara mengetahui tag-tag penyusunya, dan merubah kode CSS menjadi seperti ini:

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}

h1, h2 {
    color: green;
}

ul li a {
    color: orange;
}
```

Perhatikan! **ul li a**, maksudnya adalah: "Masuk ke tag `<ul>`, lalu masuk ke tag `<li>`, lalu rubah style pada semua tag `<a>` didalamnya". 

Maka hasilnya adalah seperti ini:

![[7 CSS Selctor-3.png]]

Jika kita menggunakan tag `<ol>` maka link nomor 6-10 lah yang akan menerima style.

Kode CSS:
```css
body {
    font-family: Arial, Helvetica, sans-serif;
}

h1, h2 {
    color: green;
}

ul li a {
    color: orange;
}

ol li a {
    color: red;
}
```

Maka hasilnya:
![[7 CSS Selctor-4.png]]

---
Baiklah, tidak ada cara untuk memberi **link 1**, style tersendiri, karena tag memberi style pada semua tag yang sama. Maka, kita harus beralih menggunakan selector sebagai id.
## Penggunaan selector dengan id dan class
Penggunaan selector yang menargetkan elemen tertentu pada HTML, jauh lebih mudah jika kita menggunakan **id** atau **class**. Selain itu, penggunaan id dan class pada HTML akan membuat pemberian style oleh CSS akan jauh lebih mudah, lebih rapi, dan metode ini jugalah yang biasanya digunakan pada proyek yang sebenarnya.

Jadi, pemberian id dan class dilakukan pada file HTML, mari kita modifikasi file HTML kita, dimana kita menambahkan id pada tag **paragraf pertama** dan class untuk tag **paragraf kedua**:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Belajar Selector CSS</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Belajar Selector CSS</h1>
    <p>Lihatlah dan pahami link-link berikut:</p>
    <p>
        <ul>
            <li><a href="#">Link 1</a></li>
            <li><a href="#">Link 2</a></li>
            <li><a href="#">Link 3</a></li>
            <li><a href="#">Link 4</a></li>
            <li><a href="#">Link 5</a></li>
        </ul>
    </p>
    <p>
        <ol>
            <li><a href="#">Link 6</a></li>
            <li><a href="#">Link 7</a></li>
            <li><a href="#">Link 8</a></li>
            <li><a href="#">Link 9</a></li>
            <li><a href="#">Link 10</a></li>
        </ol>
    </p>
    <p>
        <a href="https://www.youtube.com">Youtube Play</a>
    </p>

<h2>Judul artikel Subheading</h2>

    <p id="p1">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat et eum at exercitationem ullam laboriosam perferendis sed quisquam aliquam. Incidunt, hic amet inventore sit maxime illo ducimus excepturi. Eligendi, dolor!</p>

    <p class="p2">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis sed voluptate odio suscipit eaque. Cumque hic adipisci tenetur sequi distinctio facere at dolor incidunt. Maiores est porro repellendus perferendis magni.
    </p>
</body>
</html>
```

Pemberian style CSS bisa dilakukan dengan cara seperti ini:

```css
#p1{
    color: orange;
}

.p2{
    color: red;
}
```

Untuk **id** maka selectornya harus menggunakan tambahan tanda pagar atau hashtag (#).
Untuk **class**, maka selectornya harus menggunakan tambahan tanda titik (.).

Sehingga, ketika HTML kita jalankan lagi, maka paragraf yang ditampilkan akan memiliki style yang berbeda:

![[7 CSS Selctor-5.png]]

### Ekstra teori
Lantas, apa perbedaan **id** dan **class** dalam CSS ini? Perhatikan teori berikut:
#### Teori id
- Sebuah elemen HTML hanya boleh memiliki 1 id
- Setiap halaman hanya boleh memiliki 1 elemen dengan id tersebut
- Dapat digunakan sebagai penanda halaman untuk link
- Digunakan juga untuk javascript
- Sebaiknya tidak digunakan untuk CSS (lebih baik gunakan class)
	- Jika diilustrasikan, menggunakan tag sebagai selector, memiliki beban 1. Menggunakan class sebagai selector, memiliki beban 10 kali lipat. Sedangkan menggunakan id sebagai selector, memiliki beban 100 kali lipat. Tidak dianjurkan menggunakan id sebagai selector.
#### Teori class
Berikut adalah alasan mengapa sebaiknya menggunakan **class** pada CSS:

1. **Penggunaan Ulang**: Kelas (class) memungkinkan styling diterapkan pada banyak elemen tanpa menduplikasi kode.
2. **Spesifik tetapi Fleksibel**: Class memberikan gaya yang spesifik, tapi masih fleksibel diterapkan pada elemen yang berbeda.
3. **Kemudahan Pemeliharaan**: Mempermudah perubahan gaya secara global untuk semua elemen yang menggunakan class tersebut.
4. **Penamaan Semantik**: Class memungkinkan penggunaan nama yang semantik, sehingga kode lebih mudah dipahami.
5. **Menghindari Ketergantungan Struktur HTML**: Tidak terikat pada struktur HTML tertentu seperti ID atau tag selector, sehingga lebih fleksibel saat elemen diubah.
### Penggunan class
Class lebih unik, dan lebih baik digunakan untuk CSS, setelah penjelasan sebelumnya, seharusnya kamu sudah tahu apa keistimewaan class pada CSS.

Sekarang, kita coba rubah kembali kode HTML kita, menjadi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Belajar Selector CSS</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Belajar Selector CSS</h1>
    <p>Lihatlah dan pahami link-link berikut:</p>
    <p>
        <ul>
            <li><a href="#">Link 1</a></li>
            <li><a href="#">Link 2</a></li>
            <li><a href="#">Link 3</a></li>
            <li><a href="#">Link 4</a></li>
            <li><a href="#">Link 5</a></li>
        </ul>
    </p>
    <p>
        <ol>
            <li><a href="#">Link 6</a></li>
            <li><a href="#">Link 7</a></li>
            <li><a href="#">Link 8</a></li>
            <li><a href="#">Link 9</a></li>
            <li><a href="#">Link 10</a></li>
        </ol>
    </p>
    <p>
        <a href="https://www.youtube.com" class="cetak-tebal">Youtube Play</a>
    </p>

<h2>Judul artikel Subheading</h2>

    <p id="p1">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quaerat et eum at exercitationem ullam laboriosam perferendis sed quisquam aliquam. Incidunt, hic amet inventore sit maxime illo ducimus excepturi. Eligendi, dolor!</p>

    <p class="p2 cetak-tebal">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis sed voluptate odio suscipit eaque. Cumque hic adipisci tenetur sequi distinctio facere at dolor incidunt. Maiores est porro repellendus perferendis magni.
    </p>
</body>
</html>
```

Di kode HTML diatas, kita menambahkan class **cetak-tebal** pada tag `a` yang menyebut youtube, dan tag `<p>` yang menyebut paragraf, tepatnya pada paragraf kedua.

Tunggu, kenapa ada 2 class pada paragraf kedua? Inilah kelebihan class, dimana class bisa diisi oleh class lain, cara menambahkanya pun cukup mudah, yaitu dengan memberi tanda spasi diatara classnya.

Perhatikan kode CSS berikut:

```css
#p1{
    color: orange;
}

.p2{
    color: red;
}

.cetak-tebal{
    font-weight: bold;
    font-family: Arial, Helvetica, sans-serif;
}
```

Jika sekarang kita jalankan file HTML, maka hasilnya adalah sebagai berikut:

![[7 CSS Selctor-6.png]]

Sekarang, link dan paragraf kedua akan mendapatkan style berupa font yang tebal, yang berasal dari class `cetak-tebal`. Keunikan disini adalah bahwa paragraf kedua juga mendapat style dari class lain berupa `p2` yang memberi style warna merah.

Eits...

Tidak sampai disitu penggunaan class, ada cara lain lagi untuk menggunakan class, coba rubah kode CSS kita menjadi seperti ini:

```css
#p1{
    color: orange;
}

.p2{
    color: red;
}

p.cetak-tebal{
    font-weight: bold;
    font-family: Arial, Helvetica, sans-serif;
}
```

Maka, akan terjadi perubahan pada tampilan halaman HTML kita:

![[7 CSS Selctor-7.png]]

Ternyata, link youtube tidak menjadi tebal lagi! Kenapa ini bisa terjadi?

Ini karena kita merubah selector menjadi `p.cetak-tebal{}`. Maksud dari kode ini, adalah: "CSS, rubah style elemen HTML yang memiliki tag `<p>` (paragraf), yang memiliki class berupa `cetak-tebal`". 

Karena tag `<a>` tidak termasuk, maka otomatis tag yang memiliki isi link youtube tersebut tidak menerima perubahan style oleh CSS.