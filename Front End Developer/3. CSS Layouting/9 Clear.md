---
obsidianUIMode: preview
sumber: WPU
level: medium
bahasa: CSS
tanggal_study: 2024-10-14T10:45:00
total_study: 1
tags:
  - CSS
id: WPUCSSLOT10
sr-due: 2024-10-15
sr-interval: 1
sr-ease: 130
---
# CSS Clear
Setelah sebelumnya kita belajar materi **float**, sekarang kita akan mempelajari materi lanjutan tentang **float**, yaitu **clear**. Karena menggunakan **float** memang tidak semudah itu, sehingga kita perlu belajar materi lain untuk menyempurnakan penggunaan **float** kita.

Kita lihat saja contoh ini, kita buat kode HTML seperti ini:

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
        <img src="pngegg.png" width="300" height="300" alt="real madrid">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus maiores rem nulla temporibus, dicta praesentium consequatur error quae totam quis eveniet vero cumque nesciunt fuga quod quos aliquam molestiae modi consequuntur? Non nemo necessitatibus qui eius, iusto est nulla excepturi itaque libero magnam, quas saepe ea sapiente quaerat iure provident dolorum cumque perspiciatis numquam quia id ad? Rerum facere, magnam a quae laudantium consectetur id obcaecati reprehenderit blanditiis labore eos magni repellendus tempora dolorem commodi quaerat. Eum debitis nobis eos harum quod facilis inventore, tempore ullam sint vero, natus iure veritatis perferendis porro expedita assumenda quaerat repudiandae dolorem suscipit dolorum.</p>
    </div>
    
</body>
</html>
```

Lalu, kita buat kode CSS seperti ini:

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

Maka hasilnya akan menjadi seperti ini:

![[9 Clear-1.png]]

Baiklah, mungkin terlihat tidakk ada masalah. Namun, masalah akan terlihat jika kita mengurangi jumlah teks yang kita tampilkan. Perbaiki kode HTML kita agar menampilkan lebih sedikit teks sebagai berikut:

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
        <img src="pngegg.png" width="300" height="300" alt="real madrid">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    </div>
    
</body>
</html>
```

Maka hasilnya adalah elemen **container** mengalami keruntuhan, karena elemen ini tidak manganggap didalam dirinya ada gambar. Seperti ini:

![[9 Clear-2.png]]

---
Nah, cara mengatasi maasalah ini, adalah dengan **menghentikan / membersihkan float**:
- Menggunakan property **overflow**
- Menggunakan `<div>` kosong
- Menggunakan teknik **micro clearfix**

## overflow
Solusi pertama adalah dengan menggunakan properti **overflow** sebagai berikut:

```css
 .container {
    width: 600px;
    border: 1px solid black;
    margin: auto;
    padding: 5px;
    overflow: auto;
 }

 img {
    float: left;
    margin: 5px;
 }
```

Ini artinya, **container**-nya akan menyesuaikan tinggi dari isi kontenya,  sehingga overflow akan mengikuti tinggi. Ini artinya, gambar akan dianggap ada kembali. Hasilnya adalah:

![[9 Clear-3.png]]

Walaupun cara ini berhasil, ini bukan cara yang paling tepat. Karena cara yang paoing tepat, adalah kita menggunakan properti CSS yang bernama **clear**. 

**Clear** berfungsi untuk menghentikan / membersihkan **float**. Dimana properti ini memiliki value *left*, *right*, dan *both*.

Lalu bagaimana cara menggunakanya? Caranya adalah kita menggunakan `<div>`  kosong.
## \<div\> kosong
Untuk menggunakan **clear**, kita perlu mengetahui bahwa terdapat beberapa value yang bisa digunakan, diataranya adalah:
- **left**
- **right**
- **both**

Jadi, kita akan menghentikan nilai **float**-nya dengan menggunakan div kosong, yang nantinya akan kita buat class dengan nama **clear**.

Tag `img` atau elemen gambar yang kita gunakan, kita pasangi properti **float**, terserah kita untuk menentukan bagaimana cara menghentikan **float**-nya.

Sekarang, kita buat kode HTML menjadi seperit ini:

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
        <img src="pngegg.png" width="300" height="300" alt="real madrid">
        <div class="clear"></div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    </div>
    
</body>
</html>
```

Kita menambahkan elemen div dengan class **clear**. Lalu buat kode CSS sebagai berikut:

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

 .clear {
   clear: left;
 }
```

Untuk properti **overflow** pada selector **.container** kita hapus saja. Sekarang kita buat properti **clear** pada selector **clear**. Kita buat properti tersebut memiliki nilai value *left*. Maka hasilnya adalah sebagai berikut:

![[9 Clear-4.png]]

Tunggu, terget kita adalah tulisanya mengelilingi gambar, bukan berada dibawah gambar, melainkan berada di samping kanan gambar. Oleh karena itu kita perbaiki kode HTML kita dengan meletakan penggunaan **clear** dibawah paragraf, bukan sebelumnya. Kita perbaiki menjadi seperti ini:

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
        <img src="pngegg.png" width="300" height="300" alt="real madrid">
        
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>

        <div class="clear"></div>
    </div>
    
</body>
</html>
```

Maka, kini tulisanya sudah berada di posisi yang tepat:

![[9 Clear-5.png]]

Sekarang, tulisanya tetap ada dikanan, tapi kotaknya tidak collapse.

Kesimpulanya, kita bisa menggunakan properti **overflow**, tapi ini adalah cara meng akali. Sedangkan **float** harus dibersihkan, sehingga cara yang paling tepat adalah menggunakan **clear**.
### Kasus pertama
Tulis kode HTML berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba Float 2</title>
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

Lau, tulis kode CSS berikut:

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

Maka, akan menghasilkan keluaran seperti ini:
![[9 Clear-14.png]]

Nah, seandainya kita ingin menambahkan teks pada keluaran diatas, kita mungkin merbah kode HTML kita menjadi seperit ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba Float 2</title>
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

        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vitae fuga, reiciendis praesentium, incidunt necessitatibus omnis sequi vero voluptatum quia dicta est aliquam accusamus eaque in a aut. Minima, quo cumque.</p>
    </div>
</body>
</html>
```

Maka, outputnya sekarang menjadi seperit ini:

![[9 Clear-15.png]]

Nah, kita ingin membuat teks yang dimunculkan tidak berada disebelah kanan kotak, melainkan berada dibawah sebelah kiri. Berikut hal yang harus kita lakukan.

Rubah kode HTML menjadi seperti ini:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba Float 2</title>
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

        <div class="clear"></div>
        
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vitae fuga, reiciendis praesentium, incidunt necessitatibus omnis sequi vero voluptatum quia dicta est aliquam accusamus eaque in a aut. Minima, quo cumque.</p>
    </div>
</body>
</html>
```

Pada kode HTML diatas, kita menambahkan elemen baru berupa tag `<div>` yang memiliki class **clear**. Lalu buat kode CSS menjadi seperti ini:

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

.clear {
   clear: left;
}
```

Disini, kita memberi style lagi kepada selector **clear**, untuk merubah elemen **clear** agar membersihkan sisa **float** dengan menggunakan properti **float** yang kita isi dengan valur *left*.

Sehingga hasilnya akan menjadi seperti ini:

![[9 Clear-8.png]]

Jika elemen **kotak** memiliki nilai **float** berupa **right**, maka kita hanya perlu menyesuaikan saja, yaitu dengan merubah nilai dari properti **clear** menjadi *right*, contohnya seperti ini:

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
   float: right;
}

.clear {
   clear: right;
}
```

Maka, hasilnya adalah seperti ini:

![[9 Clear-9.png]]

### Kasus kedua
Sekarang, kiata gunakan kode HTML yang dulu pernah kita pakai, tulis kode HTML lagi seperti ini:

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

Kode CSS:

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

Maka keluaranya pada browser adalah seperti ini:

![[9 Clear-11.png]]

Bisa dilihat dengan jelas, bahwa koten didalamnya keluar dari *parent*-nya. Tapi dengan menggunakan **clear**, masalah ini bisa diperbaiki, dengan merubah kode HTML dan CSS sebagai berikut:

Kode HTML:

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

        <div class="clear"></div>

    </div>
</body>
</html>
```

Dan kode CSS menjadi seperti ini:

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

.clear {
    clear: left;
}
```

Maka, sekarang, element yang berada didalamnya akan tetap terbungkus oleh *parent*-nya, seperti ini:

![[9 Clear-12.png]]

Sebelumnya kita menggunakan ketiga kotak tersebut properti **float** dengan value *left*, apa jadinya jika salah satu dari ketika kotak tersebut menggunakan value *rigth*? Sehingga terdapat kotak yang memiliki properti **float** dengan value *rigth* dan *left*? Mudah saja, kita hanya perlu merubah kode CSS menjadi seperti ini:

Sebelum:
```css
.clear {
    clear: left;
}
```

Sesudah:
```css
.clear {
    clear: both;
}
```

---
Tapi ada yang bilang, bahwa menggunakan div kosong seperti cara diatas,  membuat kode kita menjadi tidak rapi, karena kita hanya membuat tag div tersebut hanya untuk menghilangkan nilai **float**, sehingga tag div tersebut tidak memiliki makna sama sekali. Sehingga teknik ini tidak bagus untuk dilakukan.

Ada cara ketiga, yang bisa dibilang lebih efektif lagi, yaitu teknik **micro clearfix**.
## micro clearfix
Teknik **micro clearfix** adalah teknik yang ditemukan oleh seseorang, yang bernama **Nicolas Gallagher**. Kalian bisa mencari di search bar browser kalian, dengan kata kunci **micro clearfix**, yang mana kalian akan langsung diarahkan ke situsnya. 

> site : https://nicolasgallagher.com/micro-clearfix-hack/

Didalam situs tersebut, terdapat script yang dapat kita copy paste, bentuknya seperti ini:

```css
/**
 * For modern browsers
 * 1. The space content is one way to avoid an Opera bug when the
 *    contenteditable attribute is included anywhere else in the document.
 *    Otherwise it causes space to appear at the top and bottom of elements
 *    that are clearfixed.
 * 2. The use of `table` rather than `block` is only necessary if using
 *    `:before` to contain the top-margins of child elements.
 */
.cf:before,
.cf:after {
    content: " "; /* 1 */
    display: table; /* 2 */
}

.cf:after {
    clear: both;
}

/**
 * For IE 6/7 only
 * Include this rule to trigger hasLayout and contain floats.
 */
.cf {
    *zoom: 1;
}
```

> Penulis atau pencipta teknik ini, kadang membuat update pada syntaxnya, jadi, kunjungi situsnya jika ingin melihat informasi terbaru!

> Jika kamu meng copy-paste kode `*zoom:1;`, maka kamu akan mendapati sebuah pesan error. Walaupun kode CSS tetap bisa dijalankan walau terdapat pesan error ini, ada beberapa yang harus kamu tahu.
> 
> Masalah yang kamu alami dengan properti `*zoom: 1;` di CSS adalah karena properti ini sudah dianggap usang dan merupakan _hack_ khusus untuk mengatasi masalah dalam browser Internet Explorer lama (IE 6-7). Modern browser tidak membutuhkan _hack_ ini lagi, dan bahkan mungkin VS Code memberikan peringatan karena dianggap tidak perlu atau berpotensi tidak kompatibel dengan standar CSS yang baru.
> 
> Jika kamu tidak perlu mendukung browser yang sangat lama seperti IE 6-7, kamu bisa dengan aman menghapus baris tersebut.
> 
> Namun, jika kamu tetap perlu mendukung browser lama tersebut, kamu bisa tetap membiarkannya, tapi dengan pemahaman bahwa properti tersebut tidak direkomendasikan untuk browser modern.
> 
> Apakah kamu memerlukan dukungan untuk browser yang lebih lama, atau apakah lebih fokus pada kompatibilitas dengan browser modern? Tergantung pada tujuan kamu membuat website tertentu.

Teknik diatas sebenarnya memiliki konsep yang sama dengaan kita, yaitu menggunakan properti **clear** dengan value *both*. Tapi bedanya adalah, cara diatas memungkinkan kita untuk tidak membuat elemen div kosong pada HTML.

Karena teknik ini menggunakan **pseudo element**:

```css
.cf:before,
.cf:after {
    content: " "; /* 1 */
    display: table; /* 2 */
}
```

### Cara menggunakan
Cara menggunakan teknik ini mudah saja, kita perbaiki kode CSS kita menjadi seperti ini, kita menambahkan teknik **micro clearfix** dibagian bawah kode CSS, dan menggantikan selector **clear**:

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

/**
 * For modern browsers
 * 1. The space content is one way to avoid an Opera bug when the
 *    contenteditable attribute is included anywhere else in the document.
 *    Otherwise it causes space to appear at the top and bottom of elements
 *    that are clearfixed.
 * 2. The use of `table` rather than `block` is only necessary if using
 *    `:before` to contain the top-margins of child elements.
 */
 .cf:before,
 .cf:after {
     content: " "; /* 1 */
     display: table; /* 2 */
 }
 
 .cf:after {
     clear: both;
 }
 
 /**
  * For IE 6/7 only
  * Include this rule to trigger hasLayout and contain floats.
  */
 .cf {
     *zoom: 1;
 }
```

Nah, setelah kita mengedit kode CSS, tidak lupa juga kita harus edit kode HTML kita, ada class baru yang perlu kita tambahkan, yaitu class **cf**. Karena dari bawaan kode **micro clearfix**, selector yang digunakan adalah **cf**. 

Tapi tenang saja, karena kode ini bisa kita ganti sesuai selera kita saja. 

Baik, rubah kode HTML menjadi seperti inii kira-kira:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba Float</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container cf">

        <div class="kiri"></div>
        <div class="tengah"></div>
        <div class="kanan"></div>

        <div class="clear"></div>

    </div>
</body>
</html>
```

Maka, ketika kita run lagi kode HTML kita, hasilnya menjadi seperti ini:

![[9 Clear-13.png]]

Memang tidak ada perubahan dalam tampilan, tapi perubahan ini akan membuat kode jauh lebih rapi, dan lebih efisien jika seadainya kita membuat project web yang nyata.

---
Oke sekian, terima kasih 👍

