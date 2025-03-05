---
obsidianUIMode: preview
sumber: WPU
level: pemula
bahasa: CSS
tanggal_study: 2024-10-11T13:33:00
total_study: 1
tags:
  - CSS
id: WPUCSSD9
sr-due: 2024-10-13
sr-interval: 2
sr-ease: 150
---
# Inheritance CSS (pewarisan)
Menurut W3Schools, sebuah elemen mewarisi beberapa nilai dari peroperti yang dimiliki oleh elemen *parent*-nya.

Ilustrasinya adalah, jika orang tua memiliki rambut berwarna merah, maka sang anak akan memiliki kecenderungan untuk memiliki warna rambut juga merah.

Berikut beberapa diantarra properti yang diwariskan:
- color
- font
- letter-spacing
- line-height
- list-style
- text-align
- text-indent
- text-transform
- visibility
- white-space

Kalian juga akan menemukan beberapa kasus yang berbeda, contohnya adalah sebagai berikut:

Kode HTML:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Latihan Inheritance</title>
        <meta charset="UTF-8">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <h1>Hello World</h1>

        <a href="#">Kembali ke halaman utama</a>

        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis earum a dignissimos sed aliquam! Quia, sed perferendis corporis quidem deleniti, ex delectus quo iusto impedit animi blanditiis, quasi praesentium cumque.</p>
    </body>
</html>
```

Kode CSS:

```css
body{
    font-family: Arial, Helvetica, sans-serif;
    color: darkgrey;
}
```

Maka, hasilnya adalah seperti ini:

![[9 Inheritance-1.png|550]]

Kita memberi style pada tag `<body>`, yaitu font berupa *arial*, dan memiliki warna *darkgrey*. Karena tag `<h1>` dan tag `<p>` merupakan anak dari tag `<body>`, maka secara otomatis, sifat-sifatnya akan menurutn, yaitu membuat kedua tag ini memiliki isi tag yang memiliki font *arial* dan memiliki warna *darkgrey*.

Tapi, kenapa link nya tidak berubah, bukankan tag `<a>` merupakan anak dari tag `<body>`? 

Hal ini terjadi, karena elemen `<a>` tidak mewarisi nilai dari properti **color**. Supaya elemen `<a>` mau diwarisi sifat-sifat dari *parent*-nya, kita harus merubah kode CSS tersebut menjadi seperti ini:

```css
body{
    font-family: Arial, Helvetica, sans-serif;
    color: darkgrey;
}

a {color: inherit;}
```

Maka, hasilnya akan menjadi seperti ini:

![[9 Inheritance-2.png|550]]

Jadi, solusi sederhana yang harus kita lakukan, adalah dengan dengan memberi value *inherit* pada property *color*. Dimana kode ini memberi perintah agar semua elemen `<a>`, harus mau diwarisi property *color* oleh elemen parentnya.