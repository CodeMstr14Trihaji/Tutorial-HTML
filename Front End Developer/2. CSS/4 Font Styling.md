---
obsidianUIMode: preview
sumber: WPU
level: pemula
bahasa: CSS
tanggal_study: 2024-10-10T04:17:00
total_study: 1
tags:
  - CSS
id: WPUCSSD4
sr-due: 2024-10-12
sr-interval: 2
sr-ease: 150
---
# Font Styling pada CSS
Font merupakan elemen pada halaman web yang berhubungan dengan typeface (jenis tulisan / huruf), bisa mengenai family-nya, ukuran, bold atau tidaknya dan lain-lain.

Font pada CSS berguna untuk mengatur style pada teks yang digunakan pada web. Ada beberapa jenis penggunaan font, beberapa maksud penggunaan font pada CSS adalah sebagai berikut.
## font-family
Memiliki value yang terdiri dari **nama font** dan **generic family**. Contohnya adalah sebagai berikut:

```css
body {
	font-family: arial, verdana, sans-serif;
}

p {
	font-family: "Times New Roman", serif;
}
```

Pada CSS dengan selector body,  *arial* dan *verdana* merupakan **nama font**. Dan *sans-serif* merupakan **generic family**.

Sedangkan CSS dengan selector p, *'"Times New Roman"* merupakan **nama font**. Dan *serif* merupakan **generic family**.

Berikut adalah contoh penggunaanya:

Kode HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba font</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1>Hello World</h1>

    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ullam deleniti, dicta tempore numquam harum aliquid? Nulla, earum quas minima iste soluta atque. Ipsam voluptate rerum eos aliquid explicabo in qui?</p>

    <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Accusamus, vero laudantium? Corrupti amet culpa hic consequuntur laudantium eligendi minus, pariatur nulla, natus neque sed voluptate in nesciunt dolores ut ex?
    </p>
    
</body>
</html>
```

Kode CSS:

```css
h1{
    font-family: Arial, verdana, sans-serif;
} 
```

Kenapa value yang diberikan bisa lebih dari satu? Artinya font yang pertama dicari adalah font *arial*, jadi ketika user membuka website, maka akan dicek sistem operasi penggunaanya, apakah ada font *arial*. Jika tidak, maka jalankan font disampingnya, yaitu font *verdana*. Tapi jika tidak ada lagi, maka akan menjalankan font *sans-serif*.

Kita bisa tambahkan lagi style CSS diatas, menjadi:

```css
h1{
    font-family: Arial, verdana, sans-serif;
} 

p {
    font-family: Georgia, 'Times New Roman', Times, serif;
}
```

Disini, kita menambahkan style font pada tag paragraf pada HTML.

> Untuk bisa melihat perubahan yang dilakukan di CSS, kita tidak perlu menutup browser yang menampilkan hasil kode HTML. Cukup rubah kode program pada VS Code, save, lalu Refresh Browser, maka perubahan akan terlihat.

## font-size
Memiliki value seperti **px**, **%**, dan **em**. Style CSS ini berguna untuk memberi ukuran pada teks. Berikut contohnya:

Kode HTML

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Coba Font</title>
        <meta charset="utf-8">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <h1>Hello World</h1>

        <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dicta laborum natus illum vel ab iure dolorum, totam laboriosam possimus neque quod! Numquam molestias earum consequuntur, soluta repudiandae vel quisquam velit.
        </p>
        <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Commodi magnam laudantium praesentium corrupti vel aliquid tenetur ea consectetur quas id beatae, sunt veniam earum explicabo, vitae nisi harum voluptatibus voluptas?
        </p>
    </body>
</html>
```

Kode CSS:

```css
h1{
    font-family: arial, Verdana, Geneva, Tahoma, sans-serif;
    font-size: 100px; 
}

p {
    font-family: Georgia, 'Times New Roman', Times, serif;
}
```

*font-size* berguna untuk mengatur besar teks, jalankan dan lihat dibrowser, bahwa tulisan didalam tag h1 yaitu Hello World akan berukuran besar, karena sudah kita atur agar berukuan 100px. Nilai **px** atau **pixel** ini bisa digantikan dengan **%** dan juga **em**. 

Untuk ukuran 100, jika kita menggunakan value **%**, maka ukuranya masih biasa. Jika menggunakan value **px**, maka ukuranya akan menjadi lumayan besar. Tapi ketika menggunakan value **em**, maka ukuran font akan sangat-sangat besar. Kita tentukan saja kapan harus menggunakan value-value tersebut.
## font-weight
Memiliki value seperti **lighter**, **normal**, **100-900**, **bold**, dan **bolder**. Style CSS ini berguna untuk membuat font menjadi bold, atau menjadi tebal. Berikut contoh penggunaanya.

Kode HTML:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Coba Font</title>
        <meta charset="UTF-8">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <h1>Hello World</h1>

        <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Repudiandae eum pariatur delectus, voluptas impedit numquam asperiores cupiditate, consectetur quia illum, adipisci quae sint architecto suscipit? Ullam iure praesentium laborum itaque.
        </p>
        
    </body>
</html>
```

Kode CSS:

```css
h1{
    font-family: arial, Verdana, Geneva, Tahoma, sans-serif;
    font-size: 100px; 
    font-weight: 1000;
}

p {
    font-family: Georgia, 'Times New Roman', Times, serif;
}
```

Kode CSS diatas meminta h1 memiliki ketebalan 1000px, hasilnya akan menjadi seperti ini:

![[4 Font Styling.png]]

## font-variant
Memiliki value seperti **normal**, dan **small-caps**. Penggunaan style CSS ini cukup unik, lebih baik lihat contoh berikut agar lebih paham.

Ini adalah hasil kode HTML dengan CSS sebelumnya:

![[4 Font Styling.png]]

Jika kita menambahkan kode CSS, yaitu menambahkan *font-variant: small-caps;*, maka akan terjadi perubahan. Pertama-tama rubah kode CSS menjadi seperti berikut:

```css
h1{
    font-family: arial, Verdana, Geneva, Tahoma, sans-serif;
    font-size: 100px; 
    font-weight: 1000;
    font-variant: small-caps;
}

p {
    font-family: Georgia, 'Times New Roman', Times, serif;
}
```

Maka, semua huruf pada tag h1, atau kata Hello World, semuanya akan menjadi huruf kapital. Namun hanya huruf pertama dari setiap kata yang memiliki ukuran lebih besar daripada huruf sesudahnya, hasil atau perbedaanya adalah seperti ini:

![[4 Font Styling-1.png]]

## font-style
Memiliki value seperti **normal**, **italic**, dan **oblique**. Berguna untuk memberikan style pada font, seperti menjadikan font menjadi italic. Sebagai catatan, tidak semua font memiliki tipe italic, maksudnya adalah, beberapa font tidak memiliki type italic, sehingga yang terjadi adalah pemiringan beberapa derajat oleh sistem, yaitu **oblique**, ketika kita meminta font tersebut menjadi miring atau italic. Ilustrasinya adalah sebagai berikut:

![[4 Font Styling-2.png|500]]

Dengan kode HTML yang sama, berikut tambahan kode CSS yang kita lakukan:

Kode CSS:
```css
h1{
    font-family: arial, Verdana, Geneva, Tahoma, sans-serif;
    font-size: 100px; 
    font-weight: 1000;
    font-variant: small-caps;
    font-style: italic;
}

p {
    font-family: Georgia, 'Times New Roman', Times, serif;
}
```

Dengan penambahan CSS diatas, maka hasil nya berubah menjadi seperti ini:

![[4 Font Styling-3.png]]

## line-height
Memiliki value yang diantaranya adalah **normal**, **px**, dan **em**. Berguna untuk memberi jarak antar baris, berikut contoh penggunaanya.

Dengan kode HTML yang sama, cukup kita rubah kode CSS-nya:

```css
h1{
    font-family: arial, Verdana, Geneva, Tahoma, sans-serif;
    font-size: 100px; 
    font-weight: 1000;
    font-variant: small-caps;
    font-style: italic;
}

p {
    font-family: Georgia, 'Times New Roman', Times, serif;
    line-height: 50px;
}
```

Maka, hasilnya akan menjadi seperti ini:

![[4 Font Styling-4.png]]

# Shorthand CSS

Penulisan kode CSS juga bisa disingkat menjadi lebih padat, dari yang sebelumnya seperti ini:

![[4 Font Styling-5.png]]

Bisa dibuat lebih singkat, dengan urutan yang harus sesuai tentunya:

![[4 Font Styling-6.png]]

Untuk bagian *font-size* dan *font-family*, sifatnya wajib, sedangkan yang lainya opsional.

Tapi, jika tidak hafal dengan urutanya, atau terkesan ribet, boleh saja tetap menggunakan cara penulisan biasa.