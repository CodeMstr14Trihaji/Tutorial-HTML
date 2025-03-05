---
obsidianUIMode: preview
sumber: WPU
level: medium
bahasa: CSS
tanggal_study: 2024-10-11T20:44:00
total_study: 1
tags:
  - CSS
id: WPUCSSLOT3
sr-due: 2024-10-12
sr-interval: 1
sr-ease: 130
---
# Dimensi dan Overflow CSS
 Langsung ke kode HTML saja supaya lebih jelas:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Dimensi & Overflow</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div>Hello World</div>
</body>
</html>
```

Disini kita akan praktekan saja tentang penggunaan dimensi, lalu sekarang perhatikan kode CSS berikut:

```css
div {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
}
```

Dimensi memang hanya terdiri dari **width** dan **height** saja. Untuk melihat dengan jelas dimensi yang telah terbentuk, kita juga menambahkan background, yaitu background warna hijau muda, hasilnya seperti ini:

![[2 Dimensi & Overflow-1.png]]

## Nilai satuan yang bisa digunakan pada width & height
Satuan yang bisa digunakan untuk value dari properti **width** dan **height** adalah sebagai berikut:
- px (absolut/pasti)
- % (relatif terhadap elemen parent / pembungkusnya)
- in, cm, mm, pt, pc (satuan yang diambil dari dunia nyata)

Khusus untuk nilai %, kita bis mengganti kode CSS yang telah kita buat sebelumnya, menjadi seperti ini:

```css
div {
    width: 50%;
    height: 200px;
    background-color: lightgreen;
}
```

Setelah itu, kamu jalankan kode HTML. Lalu cobalah untuk memperbesar dan memperkecil ukuran browser, maka otomatis dimensi yang telah kita buat akan berusaha untuk tetap berada di posisi 50% dari elemen parentnya.

Live demo:

![[20241011-1301-36.3836041.mp4]]

## Penggunaan dimensi
Sekarang, cobalah kode HTML berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Dimensi & Overflow</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="satu">
        <div class="dua">Hello World</div>
    </div>
</body>
</html>
```

Lalu ketikan kode CSS berikut:

```css
.satu {
    width: 500px;
    height: 200px;
    background-color: pink;
}

.dua {
    width: 80%;
    background-color: aqua;
}
```

Kode CSS diatas memiliki penjelasan seperti ini:
- Selector pertama berguna untuk memberi dimensi pada elemen dengan class *satu*. Ukuran dimensi adalah 500x200px, dengan background berwarna pink. Elemen ini juga menjadi elemen *parent* dari elemen didalamnya.
- Selector kedua berguna untuk memberi dimensi pada elemen kedua, yang memiliki class *dua*. Ukuran dimensi yang kita buat hanya panjang, yang berukuran **80%**. Karena menggunakan satuan **%**, maka dimensi yang dibuat akan relatif terhadap elemen *parent*-nya. Dimensi dari elemen ini juga ditampilkan dengan memiliki background berwarna biru muda atau aqua.

Ketika kita menampilkan kode HTML, maka akan tampil sebagar berikut:
\
![[2 Dimensi & Overflow-2.png]]

## Ketika child lebih besar dari dimensi parent
Apa jadinya jika kitta mengetikan kode CSS berikut:

```css
.satu {
    width: 500px;
    height: 200px;
    background-color: pink;
}

.dua {
    width: 150%;
    background-color: aqua;
}
```

Perhatikan value dari properti **width**, diatas, valuenya memiliki nilai lebih besar dari 100%. Apakah yang akan terjadi?

Yang akan terjadi adalah elemen *child* akan memanjang, melebihi panjang element *parent*-nya. Hasilnya akan menjadi seperti ini:

![[2 Dimensi & Overflow-3.png]]

## Jika hanya menuliskan width saja
Kode HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Dimensi & Overflow</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="main">    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis id enim, reprehenderit animi in facere eos illo molestiae modi saepe eligendi corrupti recusandae magni adipisci esse eum cumque maxime numquam.</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed dolore consectetur dicta, eos porro animi modi praesentium nobis fuga odit et maiores, nihil ipsam officiis, accusamus nostrum repellendus ullam quae.</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Modi aspernatur incidunt itaque libero aliquid eos magnam? Minima nulla, id itaque corrupti iusto veritatis tenetur, harum ullam, doloremque quisquam dolores veniam.</p>
    </div>

</body>
</html>
```

Lalu tulis kode CSS sebagai berikut:

```css
.main {
    width: 300px;
    background-color: pink;
}
```

Pada CSS diatas, kita mengatur supaya dimensi dari elemen ber class *main* memiliki batasan panjang yaitu 300px. Namun kita tidak membatasi **height** nya. Hal ini membuat teks yang ada didalamnya akan turun kebawah ketika sudah mencapai batas dari panjang yang ditentukan.

Hasil:

![[2 Dimensi & Overflow-4.png]]

Jika kita mengatur heigtnya juga, dimana kita merubah kode CSS menjadi seperti ini:

```css
.main {
    width: 300px;
    height: 250px;
    background-color: pink;
}
```

Maka, isi elemen akan keluar dari dimensi yang telah ditentukan, karena dimensi telah disetel untuk memiliki panjang dan tinggi yang telah dibuat:

![[2 Dimensi & Overflow-5.png]]

## Penggunaan CSS Overflow
Ketika kasus diatas terjadi, disinilah kegunaan Overflow. Overflow pada CSS, berguna untuk menangani kondisi ketika elemen *child* keluar dari *parent*-nya.

Untuk value dari overflow, adalah sebagai berikut:
- **visible** (jika ada konten yang keluar dari *parent*-nya, maka konten akan diperlihatkan)
- **auto** (CSS akan membuatkan scroll, ketika kontenya tidak cukup lagi)
- **hidde** (menyembunyikan konten yang keluar dari *parent*-nya)

Sekarang, kita buat kode HTML kita menjaddi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Penggunaan Overflow</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquid repellendus iure deserunt maiores ducimus quasi eligendi voluptatum! Quo animi repellendus aliquid sint enim, tempore, ut molestiae adipisci dolores, reprehenderit non!</div>
</body>
</html>
```

Lalu, kita buat kode CSS kita menjadi seperti ini:

```css
div {
    width: 200px;
    height: 200px;
    background-color: pink;
    overflow:visible ;
}
```

Jika menggunakan property **overflow** dengan **value** *visible*, maka konten yang keluar dari *child* akan tetap ditampilkan:

![[2 Dimensi & Overflow-6.png]]

Ganti kode CSS menjadi seperti ini:

```css
div {
    width: 200px;
    height: 200px;
    background-color: pink;
    overflow:auto;
}
```

Jika value yang kita isi adalah *auto*, maka jika ada konten yang keluar dari element *parent*-nya, akan dibuat scroll bar pada bagian samping elemen *parent*-nya. Seperti berikut:

![[2 Dimensi & Overflow-7.png]]

Ganti kode CSS menjadi seperti ini:

```css
div {
    width: 200px;
    height: 200px;
    background-color: pink;
    overflow: hidden;
}
```

Jika kita mengisi nilai value dengan *hidden*, maka konten yang keluar dari dimensi *parent*-nya akan disembunyikan, sehingga tidak terlihat:

![[2 Dimensi & Overflow-8.png]]

Terakhir, ganti kode HTML menjadi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Penggunaan Overflow</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div>Lorem ipsum dolor, sit amet consectetur</div>
</body>
</html>
```

Dan kode CSS menjadi seperti ini:

```css
div {
    width: 200px;
    height: 200px;
    background-color: pink;
    overflow: scroll;
}
```

Maka, akan muncul scroll pada dimensi *parent*. Sekalipun konten yang ada didalamnya tidak melebihi dimensi *parent*-nya.

Hasilnya adalah sebagai berikut:

![[2 Dimensi & Overflow-9.png]]
