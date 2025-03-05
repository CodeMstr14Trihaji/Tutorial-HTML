---
obsidianUIMode: preview
sumber: WPU
level: sulit
bahasa: CSS
tanggal_study: 2024-10-13T20:13:00
total_study: 1
tags:
  - CSS
id: WPUCSSLOT9
sr-due: 2024-10-14
sr-interval: 1
sr-ease: 130
---
# Float pada CSS
Apa itu float? **Float** merupakan properti pada CSS untuk mengatur posisi sebuah elemen. Sebuah elemen dapat dipaksa untuk berada di sebelah kiri atau kanan dari parent / pembungkusnya dengan menggunakan properti ini.

Jadi properti ini memiliki beberapa value, diantaranya adalah:
- **none** (default value)
- **left** (elemen akan ada di kiri)
- **right** (elemen akan ada di kanan)

---
Sebelum kita belajar lebih dalam tentang materi ini, ada yang perlu kita bahas yaitu tentang 
**normal flow** dan **out-of low**. Jadi, kedua value ini adalah nilai-nilai yang dimiliki oleh sebuah elemen ketika kita memberi kode CSS.

Sepanjang tutorial sebelumnya, sebagian besar project yang kita buat adalah **normal flow**. Seperti ketika kita menggunakan **box model** dan semacamnya. 

Kali ini, kita akan mulai menggunakan konsep **out-of low** dalam pembelajaran **float** kali ini.
## Penggunaan float
Tulis kode HTML berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Penggunaan Float</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    
    <div class="satu"></div>
    <div class="dua"></div>
    <div class="tiga"></div>

</body>
</html>
```

Lalu, kita tulis kode CSS sebagai berikut:

```css
div {
    width: 100px;
    height: 100px;
}

.satu {
    background-color: salmon;
}

.dua {
    background-color: limegreen;
}

.tiga {
    background-color: lightskyblue;
}
```

Kita membuat tiga elemen `<div>`, lalu membuatnya memiliki warna background. Sekilas akan tampis hasil seperti ini:

![[8 Float-1.png|500]]

Inilah yang disebut dengan **normal flow**, karena kita menggunakan elemen yang memiliki tag `<div>`, yang juga memiliki display default berupa **block**. Bisa dilihat bahwa kotak yang muncul akan turun kebawah, sesuai seperti sifat dari display **block**.

Sekarang, kita coba untuk memberi kotak warna hijau properti **float**. Perhatikan kode CSS berikut:

```css
div {
    width: 100px;
    height: 100px;
}

.satu {
    background-color: salmon;
}

.dua {
    background-color: limegreen;
    float: left;
}

.tiga {
    background-color: lightskyblue;
}
```

Maka hasilnya: 

![[8 Float-2.png]]

What the ff...! Kenapa kotak biru yang hilang?

Ini terjadi, karena ketika kita memberi kotak hijau properti **float**, maka kotak biru yang ada dibawahnya akan menganggap kotak hijau itu *tidak ada*. Karena kotak hijau sudah keluar dari **flow normal**-nya.

Baiklah, sekarang kita coba geser kotak hijau ini, supaya menampilkan kotak biru yang ditimpanya dengan kode CSS:

```css
div {
    width: 100px;
    height: 100px;
}

.satu {
    background-color: salmon;
}

.dua {
    background-color: limegreen;
    float: left;
    margin-left: 10px;
}

.tiga {
    background-color: lightskyblue;
}
```

Maka hasilnya, akan terlihat seperti ini:

![[8 Float-3.png|500]]

Nah inilah yang disebut dengan **out-of flow**. Karena kita memberi kotak hijau properti **float** dengan value *left*, maka kotak hijau akan bergerak kekiri dari element *parent*-nya. Element *parent* dari elemen dengan class **dua** adalah elemen **body**. 

Tapi, karena secara default elemen kotak akan dimunculkan disebelah kiri, maka perubahan ini tidak terlihat, kita bisa merubah value property **float** dengan *right*. Hasilnya akan seperti ini:

```css
div {
    width: 100px;
    height: 100px;
}

.satu {
    background-color: salmon;
}

.dua {
    background-color: limegreen;
    float: right;
    margin-left: 10px;
}

.tiga {
    background-color: lightskyblue;
}

```

Maka, outputnya akan seperti ini:

![[8 Float-4.png|500]]

Sekarang, elemen kotak hijau akan bergerak kekanan dari elemen *parent*-nya, yaitu elemen **body**.

Sekarang, kita akan mencoba untuk membungkus elemen div yang sebelumnya kita buat, dengan elemen **container**. Rubah kode HTML menjadi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Penggunaan Float</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    
    <div class="container">
        <div class="satu"></div>
        <div class="dua"></div>
        <div class="tiga"></div>
    </div>

</body>
</html>
```

Sekarang, elemen yang membentuk kotak (tiga kotak) telah kita bungkus dengan elemen **container**. Lalu rubah juga kode CSS sebelumnya menjadi seperti ini:

```css
.container {
    width: 600px;
    border: 1px solid black;
    margin: auto;
    padding: 5px;
}

.satu, .dua, .tiga {
    width: 100px;
    height: 100px;
}

.satu {
    background-color: salmon;
}

.dua {
    background-color: limegreen;
}

.tiga {
    background-color: lightskyblue;
}
```

Kode CSS diatass berfokus merubah elemen **container**.  Sekarang, tampilan browser akan menjadi seperti ini:

![[8 Float-5.png|500]]

Maka, akan menjadi seperti ini. Sekarang kita rubah lagi kode CSS kita menjadi seperti ini:

```css
.container {
    width: 600px;
    border: 1px solid black;
    margin: auto;
    padding: 5px;
}

.satu, .dua, .tiga {
    width: 100px;
    height: 100px;
}

.satu {
    background-color: salmon;
}

.dua {
    background-color: limegreen;
    float: right;
}

.tiga {
    background-color: lightskyblue;
}
```

Maka, sekarang, kotak hijau akan menjadi berada disebelah kanan dari **container**, karena sekarang, **container** adalah elemen *parent*-nya. 

![[8 Float-6.png|500]]

## Penggunaan float
Yang bisa dilakukan menggunakan peroperti float, adalah sebagai berikut:
- **text wrapping** : membuat teks mengelilingi gambar / elemen lain
- **image gallery** : membuat serangkaian gambar menjadi galeri
- **multi-column layout** : membuat halaman memiliki beberapa kolom
- **dll** : dan masih banyak lagi

Baiklah, kita coba satu-persatu.
### text wrapping
Sekarang, kita coba buat kode HTML seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba Float</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <img src="pngegg.png" width="300" height="300" alt="Read Madrid">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur molestiae eaque ipsum laudantium deleniti ducimus repellendus dolorum voluptate vitae? Doloribus rerum consectetur dolorem nam suscipit hic tempore amet ea ex, consequatur optio repellendus, voluptas quis facere voluptatibus tenetur aut fugiat quisquam! Repellat enim quae repellendus ipsam, maxime eum! Dolores voluptatum natus placeat aspernatur minima aut, excepturi fugiat corporis optio debitis molestias voluptas reprehenderit quasi consectetur quam nam maxime corrupti amet explicabo! Perspiciatis vero rerum assumenda minus cumque fuga at quaerat ea saepe. Vero placeat cum reprehenderit impedit possimus dolore asperiores? Doloribus tempore quasi accusantium fugit necessitatibus saepe sunt eveniet veniam!</p>
    </div>
</body>
</html>
```

Kita siapkan satu gambar sembarang untuk kita gunakan sebagai pembelajaran. Tambahkan gambar pada HTML.

Lalu setelah itu, kita tambahkan kode CSS sebagai berikut:

```css
.container {
    width: 600px;
    border: 1px solid black;
    margin: auto;
    padding: 5px;
}
```

Maka, hasilnya akan menjadi seperti ini:

![[8 Float-8.png|500]]

Akan terbuat logo dengan teks yang terbungkus oleh **container** seperti ini. Sekarang coba kita rubah kembali kode CSS menjadi seperti ini:

```css
.container {
    width: 600px;
    border: 1px solid black;
    margin: auto;
    padding: 5px;
}

img {
    float: left;
    margin: 5px;
}
```

Kita merubah agar gambar memiliki value **float** berupa *left*, sehingga gambar akan berada disebelah kiri dari *parent*-nya. Berikut adalah hasil perubahanya:

![[8 Float-9.png|500]]
### image gallery
Sekarang, kita tulis kode HTML seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba Float</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">

        <div class="kotak">1</div>

    </div>
</body>
</html>
```

Disini kita membuat satu elemen div, lalu buat lagi kode CSS sebagai berikut:

```css
.container {
    width: 600px;
    border: 1px solid black;
    margin: auto;
    padding: 5px;
}

.kotak {
    width: 80px;
    height: 80px;
    background-color: salmon;
    color: white;
    text-align: center;
    line-height: 80px;
    font-size: 30px;
}
```

Penjelasan selector pertama:
- **container** diatas berguna untuk membuat elemen *parent* untuk elemen yang kita buat didalamnya. Sehingga akan ada elemen pembungkus, yang dapat terlihat dengan garis kotak tipis, karena kita menambahkan **border**.

Penjelasan selector kedua:
- Membuat kotak kecil berukuran **80x80px**. Memiliki warna *salmon*, dengan isi elemen berwarna *putih* (text). Lalu elemen **kotak** akan memiliki teks yang didalamnya berada diposisi tengah secara horizontal, tapi karena dibantu **line-heigth**, maka text akan turun kebawah, sehingga berada tepat diposisi tenah kotak baik horizontal maupun vertikal. Ukuran teks didalamnya nantinya berukuran **30px**.

Berikut hasilnya:

![[8 Float-10.png|500]]

Sekarang, kita tambahkan kode HTML lagi menjadi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba Float</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">

       <div class="kotak">1</div>
       <div class="kotak">2</div>
       <div class="kotak">3</div>
       <div class="kotak">4</div>
       <div class="kotak">5</div>
       <div class="kotak">6</div>
       <div class="kotak">7</div>
       <div class="kotak">8</div>
       <div class="kotak">9</div>
       <div class="kotak">10</div>

    </div>
</body>
</html>
```

> Dengan menggunakan VS Code yang sudah terinstal exstension HTML, kita bisa menggunakan shorthand dengan mengetikan : **.kotak{$}\*10**
> 
> Setelah selesai, tekan enter dan Voila! Terbuat 10 baris elemen div, dengan nomor urut 1-10 yang ada didalmnya!

Lalu, tambahkan kode CSS menjadi seperti ini:

> Jika kamu bingung dengan beberapa kode CSS, kamu bisa coba mengatur valuenya sendiri, atau menghilangkan style tertentu pada CSS untuk melihat, efek apa yang diberikan oleh syntax tertentu pada CSS

```css
.container {
    width: 600px;
    border: 1px solid black;
    margin: auto;
    padding: 5px;
}

.kotak {
    width: 80px;
    height: 80px;
    background-color: salmon;
    color: white;
    text-align: center;
    line-height: 80px;
    font-size: 30px;
    margin: 2px;
}
```

Maka, hasiilnya akan menjadi seperti ini:

![[8 Float-11.png]]

Nah, sekarang kita buat agar kotak-kotak tersebut saling berbaris menyamping, tidak menumpuk seperti ini. Kita perlu menambahkan properti **float**:

```css
.container {
    width: 600px;
    border: 1px solid black;
    margin: auto;
    padding: 5px;
}

.kotak {
    width: 80px;
    height: 80px;
    background-color: salmon;
    color: white;
    text-align: center;
    line-height: 80px;
    font-size: 30px;
    margin: 2px;
    float: left;
}
```

Maka, hasilnya akan menjadi seperti ini:

![[8 Float-12.png]]

Karena kita membuat semua elemen kotak diatas memiliki class **kotak**, lalu membuat elemen kotak bertipe **float**, otomatis 10 elemen kotak tersebut akan memiliki nilai yang sama, sehinngga wadah, atau **container**-nya akan menyusut. Ini dikarenakan karena elemen **container** menganggap bahwa didalam dirinya tidak ada isi atau elemen.

Ingat! properti **float** akan membuat elemen tersebut keluar dari element *parent*-nya!

Oh ya, ini jadinya jika kita mengisikan nilai **float** dengan *right* :

![[8 Float-13.png]]

Otomatis, kotak pertama, dan urutanya akan dimulai dari kanan.
### multi-column layout
Multi column berguna untuk memberi beberapa column pada tampilan. Berikut yang perlu kalian buat pada kode HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba Float</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">

        <div class="kiri"></div>
        <div class="tengah"></div>
        <div class="kanan"></div>
        
    </div>
</body>
</html>
```

Kita membuat 3 elemen. Setelah itu kita buat kode CSS berikut:

```css
.container {
    width: 800px;
    border: 1px solid black;
    margin: auto;
    padding: 5px;
}

.kiri {
    width: 150px;
    height: 500px;
    background-color: salmon;
}

.tengah {
    width: 500px;
    height: 500px;
    background-color: lightskyblue;
}

.kanan {
    width: 150px;
    height: 500px;
    background-color: limegreen;
}
```

Sekarang, hasilnya akan menjadi seperti ini:

![[8 Float-14.png]]
Note : ukuran browser dikecilkan hingga 33%.

Sekarang, tahap selanjutnya adalah membuat kotak tersebut sejajar, sehingga lebih rapi. Sekarang edit kode CSS menjadi seperti ini:

```css
.container {
    width: 800px;
    border: 1px solid black;
    margin: auto;
    padding: 5px;
}

.kiri {
    width: 150px;
    height: 500px;
    background-color: salmon;
    float: left;
}

.tengah {
    width: 500px;
    height: 500px;
    background-color: lightskyblue;
    float: left;
}

.kanan {
    width: 150px;
    height: 500px;
    background-color: limegreen;
    float: left;
}
```

Kita memberikan semua kotak properti **float**, sehingga hasilnya akan menjadi:

![[8 Float-15.png]]

Catatan: Ketika bermain dengan **float**, selalu perhatikan lebar yang digunakan. Karena sebelumnya kita menggunakan **container** dengan ukuran *800px*, artinya ketika elemen kotak tersebut harus memiliki lebar yang sama ketika dijumlahkan yaitu *800px*. Seadainya ada salah satu elemen saja, yang lebarnya lebih *1px* sekalipun, sehingga membuat total lebar menjadi *801px*, maka tampilan tidak akan sama lagi, yaitu salah satu elemen akan turun:

![[8 Float-16.png]]

Semoga mudah dipahami Guys!


