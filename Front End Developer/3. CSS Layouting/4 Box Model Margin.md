---
obsidianUIMode: preview
sumber: WPU
level: medium
bahasa: CSS
tanggal_study: 2024-10-12T14:58:00
total_study: 1
tags:
  - CSS
id: WPUCSSLOT5
sr-due: 2024-10-13
sr-interval: 1
sr-ease: 130
---
# Box Model : Margin 
Disini kita akan belajar cara menggunakan margin, seperti:
- cara pakai
- overlapping margin
- negatif margin
- auto
- shorthand

## Cara pakai
Kita akan mulai mempraktekan bagaimana menggunakan margin, siapkan kode HTML sebagai berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Margin</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    
    <div class="satu">1</div>
    <div class="dua">2</div>
    <div class="tiga">3</div>

</body>
</html>
```

Lalu siapkan kode CSS berikut:

```css
.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
}
```

Maka hasilnya akan tampil seperti ini:

![[4 Box Model Margin-1.png|500]]

Mari kita gunakan properti margin untuk merubah margin. Rubah kode CSS sebelumnya menjadi seperti ini, yaitu kita menambahkan properti margin:

```css
.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
    margin-left: 100px;
    margin-top: 30px;
}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
}
```

Maka, dimensi pertama akan turun dan bergeser ke kanan, karena ada margin yang telah kita buat, hasilnya seperti ini:

![[4 Box Model Margin-2.png|500]]

Sekarang, rubah kode CSS lagi menjadi seperti ini:

```css
.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
    margin-left: 100px;
    margin-top: 30px;
    margin-bottom: 150px;
    margin-right: 50px;
}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
}
```

Sekarang kita menambahkan margin dibagian bawah, dan sebelah kanan, ketika browser kita refresh, maka tampilanya berubah menjadi seperti ini:

![[4 Box Model Margin-3.png|500]]

Bahkan, didalam browser, kita juga bisa melihat ukuran margin yang telah kita buat, cukup inspect halaman, lalu perhatikan tampilan di kanan bawah:

![[4 Box Model Margin-4.png]]

![[4 Box Model Margin-5.png]]

Tampilan itu menunjukan ukuran margin, yang jelas memiliki ukuran yang sama dengan yang telah kita buat sebelumnya.
## Overlapping margin
Hal yang terjadi ketika kita menggabungkan dua buah margin, biasanya kiri dan kanan, atau atas dan bawah. 

Dengan kode HTML yang sama, kita rubah kode CSS kita menjadi seperti ini:

```css
.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
    margin-left: 100px;
    margin-top: 30px;
    margin-bottom: 150px;
    margin-right: 50px;
}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    margin-top: 50px; 
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
}

```

Dimensi pertama memiliki properti *margin-bottom* sebesar 150px, dan dimensi kedua memiliki *margin-top* sebesar 50px. Apa yang akan terjadi setelah perubahan ini? Apakah dimensi kedua akan bergerak turun sebesar 50px?

Jawabanya:

--- start-multi-column: ExampleRegion1  
```column-settings  
number of columns: 2  
```

Sebelum:

![[4 Box Model Margin-3.png|300]]

--- end-column ---

Sesudah:

![[4 Box Model Margin-6.png|300]]

--- end-multi-column

Ternyata, tidak ada perubahan yang terjadi. Nah, inilah yang dinamakan dengan **overlapping**.

Atau lebih tepatnya, margin itu tidak saling menambahkan, khusus kasus yang vertikal seperti ini. Margin yang akan diambil adalah margin yang paling besar, yaitu margin yang berasal dari dimensi pertama yang berukuran 150px.

---
Sekarang, kita rubah kembali kode CSS menjadi seperti ini:

```css
div{
    display: inline-block;
}

.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;

}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
}
```

Maka hasilnya menjadi seperti ini:

![[4 Box Model Margin-7.png|500]]

Tunggu, kenapa ada spasi antar dimensi diatas? padahal kita tidak memberikan margin? 

Hal ini bisa diatasi jika kita tidak memberi enter pada tag `<div>` di file HTML, jadi, coba rubah kode HTML menjadi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Margin</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    
    <div class="satu">1</div><div class="dua">2</div><div class="tiga">3</div>

</body>
</html>
```

Maka, spasi yang terbentuk sebelumnya akan hilang, dan dimensi akan saling menempel:

![[4 Box Model Margin-8.png|500]]


Sekarang, mari kita buat margin dari dimensi pertama, supaya memiliki margin kanan, kode CSS:

```css
div{
    display: inline-block;
}

.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
    margin-right: 30px;

}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
}
```

Tampilanya akan menjadi seperti ini:

![[4 Box Model Margin-9.png|500]]

Lalu, mari kita beri dimensi kedua dengan margin kiri, tambahkan kode CSS menjadi seperti ini:

```css
div{
    display: inline-block;
}

.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
    margin-right: 30px;

}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    margin-left: 20px;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
}
```

Maka, ketika dijalankan, kenapa dimensi ke-2 tetap bergeser? Dimana konsep overlapping yang sebelumnya terjadi? Kenapa tidak terjadi overlapping?

--- start-multi-column: ExampleRegion1  
```column-settings  
number of columns: 2  
```

Sebelum:

![[4 Box Model Margin-9.png|500]]

--- end-column ---

Sesudah:

![[4 Box Model Margin-10.png|500]]

--- end-multi-column

Sekarang, jarak kotak satu dan kotak 2 berjarak 50px. Hal ini terjadi jika elemen memiliki nilai display *inline*, atau *inline-block*. Dimana margin akan saling menambahkan.

Tetapi jika elemen memiliki display *block*, maka margin tidak akan saling menambahkan, dan overlapping yang terjadi. Itulah kenapa ketika kotak disusun vertikal, margin tidak saling menambahkan, tapi ketika disusun horizontal, margin akan saling menambahkan.
## negative margin
Sekarang, coba rubah margin menjadi menjadi negatif. Rubah kode CSS seperti ini:

```css
.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
margin-bottom: 30px;
}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    margin-top: -50px;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
}
```

Sekarang, kotak kita susun vertikal lagi. Jika kita membuat margin pada 2 kotak, maka seperti yang kita sudah tahu sebelumnya, akan terjadi yang namanya **overlapping**. Tapi apa jadinya jika kita menambahkan margin, tapi bernilai minus atau negatif? Maka ini yang terjadi:

![[4 Box Model Margin-11.png|500]]

Ternyata, margin kedua bergerak kearah yang berlawanan, yaitu keatas, sehingga menimpa kotak diatasnya. 

Mari kita bereksperimen lebih jauh, apa jadinya jika kotak kedua kita beri *margin-left* dengan nilai negatif? Perhatikan kode CSS berikut:

```css
.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
margin-bottom: 30px;
}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    margin-top: -50px;
    margin-left: -50px;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
}
```

Maka, kotak kedua akan bergerak ke kiri browser, sehingga seakan-akan bersembunyi dari kita:

![[4 Box Model Margin-12.png|500]]
## auto
Penggunaan *auto* cukup mudah, kita hanya perlu mengisi nilai margin dengan value *auto*, sekarang kita rubah kode CSS menjadi seperti ini:

```css
.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
    margin-left: auto;
    margin-right: auto;
}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    margin-left: auto;
    margin-right: auto;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
    margin-left: auto;
    margin-right: auto;
}
```

Untuk bisa menggunakan value *auto*, kita perlu menggunakan baik *margin-left* maupun *margin-right*. Dan hasilnya akan seperti ini:

![[4 Box Model Margin-13.png|500]]

Maka, kotak akan menyesuaikan diri untuk selalu berada ditengah-tengah dari elemen *parent*-nya atau elemen containernya. Posisi kotak juga akan menjadi fleksibel, seandainya kamu membesarkan panjang atau mengecilkan panjang browser, posisi kotak akan berubah, untuk menyesuaikan posisi tengah elemen.
## shorthand
Dalam memberi margin, kita juga bisa melakukan penyingkatan, inilah yang disebut dengan **shorthand**. Berikut tricknya dengan kode CSS:

```css
.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
    margin: 50px;
}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    margin: 100px 50px;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
    margin: 50px auto;
}
```

Dalam penggunaan shorthand, kita hanya menggunakan properti *margin*, nah begini teknik pengisian valuenya:

Di kotak pertama, kita hanya menggunakan 1 value, yaitu **50px**. Ini artinya, kotak pertama akan memiliki margin disemua sisi (atas bawah kiri kanan) dengan ukuran **50px**.

Di kotak kedua, kita mengisi margin dengan 2 value. Value pertama (**100px**) akan menentukan margin bagian atas dan bawah (**top** & **bottom**), sedangkan value kedua (**50px**) akan menentukan margin bagian kanan dan kiri (**right** & **left**).

Di kotak ketiga, kita mengisi margin dengan value, tapi value kedua bernilai **auto**. Artinya, kotak ketiga akan memiliki margin atas dan bawah dengan ukuran **50px**, dan margin kanan dan kiri dengan value **auto**. Ini artinya, kotak ketiga akan mempertahankan posisi ditengah elemen *parent*-nya.

Berikut hasilnya:

![[4 Box Model Margin-14.png|500]]

Penggunaan **shorthand** tidak sampai disinit, sekarang, coba kita rubah kode CSS menjadi seperit ini:

```css
.satu {
    width: 200px;
    height: 200px;
    background-color: lightgreen;
    margin: 30px  50px 40px;
}

.dua {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    margin: 100px auto 50px;
}

.tiga {
    width: 50px;
    height: 50px;
    background-color: violet;
    margin: 10px 20px 30px 40px;
}
```

Berikut penjelasanya:

Di kotak pertama, kali ini kita menggunakan margin dengan 3 value, cara pengisianya adalah sebagai berikut:
- Value pertama (**30px**) akan menjadi margin atas (**top**)
- Value kedua (**50px**) akan menjadi margin kanan dan kiri (**right** & **left**)
- Value ketiga (**40px**) akan menjadi margin bawah (**bottom**)

Di kotak kedua, margin memiliki 3 value juga, tapi value ke-2 menggunakan value **auto**. Artinya adalah sebagai berikut:
- Value pertama (**100px**) akan menjadi margin atas(**top**)
- Value kedua (**auto**) akan menjadi margin kanan kiri, artinya kotak akan selalu berada di tengah elemen *parent*-nya
- Value ketiga (**50px**) akan menjadi margin bawah (**bottom**)

Di kotak ketiga, kita memiliki margin dengan 4 value sekaligus! Tenang, value pertama akan selalu mengisi margin atas, lalu value selanjutnya bergerak searah jaum jam, yaitu kanan, bawah, dan kiri:
- Value pertama (**10px**) akan mengisi margin atas
- Value kedua (**20px**) akan mengisi margin kanan
- Value ketiga (**30px**) akan mengisi margin bawah
- Value keempat (**40px**) akan mengisi margin kiri

Sehingga, hasillnya akan sebagai berikut:

![[4 Box Model Margin-15.png|500]]

---
Baiklah, mungkin hanya sampai situ materi margin kita kali ini, semoga mudah dipahami 👍


