---
obsidianUIMode: preview
sumber: WPU
level: sulit
bahasa: CSS
tanggal_study: 2024-10-10T21:29:00
total_study: 1
tags:
  - CSS
id: WPUCSSD8
sr-due: 2024-10-11
sr-interval: 1
sr-ease: 130
---
# CSS Pseudo Class
Menurut W3schools, CSS Pseudo Class adalah kelas semu yang dimiliki oleh sebuah elemen HTML, yang membuat kita dapat mendefinisikan style pada "*keadaan tertentu*" dari elemen tersebut.

Kenapa disebut kelas semu, karena kelas atau class ini hanya akan aktif pada keadaan tertentu saja. 

## pseudo class berdasarkan link
pseudo-class yang berhubungan dengan link:
- **:link** : style default pada sebuah link (a yang memiliki href)
- **:hover** : style ketika kursor mouse berada diatas sebuah link / elemen
- **:active** : style ketika sebuah link di-klik (keadaan aktif)
- **:visited** : style ketika sebuah link sudah pernah dikunjungi sebelumnya (menggunakan browser yang sama)

Baiklah, mari kita coba. Kita siapkan kode HTML, seperti berikut:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Pseudo Class</title>
        <meta charset="UTF-8">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <p><a href="#" class="hello">Hello World</a></p>
        <p>
            <ul>
                <li><a href="#">Link 1</a></li>
                <li><a href="#">Link 2</a></li>
                <li><a href="#">Link 3</a></li>
                <li><a href="#">Link 4</a></li>
                <li><a href="#">Link 5</a></li>
                <li><a href="#">Link 6</a></li>
                <li><a href="#">Link 7</a></li>
                <li><a href="#">Link 8</a></li>
                <li><a href="#">Link 9</a></li>
                <li><a href="#">Link 10</a></li>
            </ul>
        </p>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid, blanditiis. Quam unde itaque voluptatem possimus excepturi ea totam. Laborum ab soluta voluptatem iste voluptatibus quae nesciunt labore similique cumque atque.
        </p>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea nesciunt praesentium iure atque magni obcaecati deserunt, sequi autem, similique iste, vero dolor animi perferendis? Eveniet inventore officiis neque nisi reiciendis!
        </p>
    </body>
</html>
```

Kita buat class **hello** pada tag `<a>` atau link yang memiliki isi berupa *Hello World*. 

Lalu kita siapkan kode CSS, dan kita langsung praktekan kode CSS diatas:

```css
.hello:link{
    color: orange;
} 

.hello:hover{
    color: green;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 20px;
}

.hello:active{
    font-style: italic;
    font-size: 100px;
}

.hello:visited{
    color: red;
}
```

Berikut penjelasanya:
- Style pada selector pertama berguna untuk merubah warna link menjadi **orange**
- Style pada selector kedua berguna untuk memberi style ketika mouse berada diatas link, yaitu memberi style merubah warna menjadi hija**u**, merubah font menjadi **arial**, dan merubah ukuran menjadi **20px**
- Style pada selector ketiga berguna untuk memberi style ketika mouse berada dikondisi menekan (ditahan) link, yaitu mengaktifkan style font menjadi **italic**, dan ukuran font menjadi **100px**. 
- Style pada selector keempat berguna untuk memberi style ketika link sudah pernah dikunjungi, yaitu memberi style warna menjadi **merah**.

Berikut live demonya:
![[20241010-1221-44.2355067.mp4]]
## Pseudo class yang berhubungan dengan posisi elemen (1)
Ada psedo-class yang berhubungan dengan posisi elemen, kali ini kita membahas bagian pertama dari pseudo-class ini:
- **:first-child** : Memilih elemen pertama dari sebuah parent (elemen pembungkusnya)
- **:last-child** : Memilih elemen terakhir dari sebuah parent (elemen pembungkusnya)
- **:nth-child(n)** : Memilih elemen ke-n dari sebuah parent (elemen pembungkusnya). n bisa berarti urutan (1), (2), ... atau pola (2n), (3n+2), (4n-1), atau ganjil dan genap (even) & (odd)

Baiklah, langsung saja kita praktek:

Dengan kode HTML yang sama:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Pseudo Class</title>
        <meta charset="UTF-8">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <p><a href="#" class="hello">Hello World</a></p>
        <p>
            <ul>
                <li><a href="#">Link 1</a></li>
                <li><a href="#">Link 2</a></li>
                <li><a href="#">Link 3</a></li>
                <li><a href="#">Link 4</a></li>
                <li><a href="#">Link 5</a></li>
                <li><a href="#">Link 6</a></li>
                <li><a href="#">Link 7</a></li>
                <li><a href="#">Link 8</a></li>
                <li><a href="#">Link 9</a></li>
                <li><a href="#">Link 10</a></li>
            </ul>
        </p>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid, blanditiis. Quam unde itaque voluptatem possimus excepturi ea totam. Laborum ab soluta voluptatem iste voluptatibus quae nesciunt labore similique cumque atque.
        </p>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea nesciunt praesentium iure atque magni obcaecati deserunt, sequi autem, similique iste, vero dolor animi perferendis? Eveniet inventore officiis neque nisi reiciendis!
        </p>
    </body>
</html>
```

> [!NOTE] Penting!
> ### child - parent
> Sebelum mulai mengedit kode CSS, kita perlu tahu dulu *child - parent* dalam CSS. Perhatikan kode HTML dibawah ini, ini adalah potongan kode diatas:
> 
> ```html
> <ul>
> 	<li><a href="#">Link 1</a></li>
> 	<li><a href="#">Link 2</a></li>
> 	<li><a href="#">Link 3</a></li>
> 	<li><a href="#">Link 4</a></li>
> 	<li><a href="#">Link 5</a></li>
> 	<li><a href="#">Link 6</a></li>
> 	<li><a href="#">Link 7</a></li>
> 	<li><a href="#">Link 8</a></li>
> 	<li><a href="#">Link 9</a></li>
> 	<li><a href="#">Link 10</a></li>
> </ul>
> ```
> 
> tag `<ul>` adalah *parent* dari tag `<li>`. Dan tag `<li>` adalah *parent* dari tag `<a>`. 
> Didalam tag `<ul>` terdapat 10 *child* yaitu 10 tag `<li>`. Sedangkan disetiap tag `<li>` terdapat satu *child* yaitu tag `<a>`.
> 
> Paham sampai sini? Harusnya sudah paham lah ya.

Kita masukan kode CSS sebagai berikut:

```css
li:first-child a{
    color: green;
}

li:last-child a{
    color: red;
}
```

Berikut penjelasanya:
- Selector pertama memberi style, kepada tag `<li>`, dan mencari *first-child* (anak pertama), yang berupa tag `<a>`. Atau jika dibuat kalimat, mungkiin akan berbunyi seperti ini: "CSS, tolong carikan saya `<a>`, yang ada didalam `<li>`, yang merupakan anak pertama. Lalu beri dia warna hijau".
- Selector kedua memberi style, kepada tag `<li>`, dan mencari *last-child* (anak terakhir), yang berupa tag `<a>`. Atau jika dibuat kalimat, mungkiin akan berbunyi seperti ini: "CSS, tolong carikan saya `<a>`, yang ada didalam `<li>`, yang merupakan anak terakhir. Lalu beri dia warna merah".

Maka, output yang keluar, adalah sebagai berikut:

![[8 CSS Pseudo Class-1.png]]

### Penggunaan nth-child
Untuk penggunaan *nth-child*, sedikit tricky, karena membutuhkan pemahaman yang lebih baik. Tapi jika dipelajari dengan baik, maka anda akan cepat paham.

Pertama, mari kita rubah kode HTML kita menjadi seperti ini:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Pseudo Class</title>
        <meta charset="UTF-8">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <p><a href="#1" class="hello">Hello World</a></p>
        <p>
            <ul class="ulsatu">
                <li><a href="#">Link 1</a></li>
                <li><a href="#">Link 2</a></li>
                <li><a href="#">Link 3</a></li>
                <li><a href="#">Link 4</a></li>
                <li><a href="#">Link 5</a></li>
                <li><a href="#">Link 6</a></li>
                <li><a href="#">Link 7</a></li>
                <li><a href="#">Link 8</a></li>
                <li><a href="#">Link 9</a></li>
                <li><a href="#">Link 10</a></li>
            </ul>
            <ul class="uldua">
                <li><a href="#">Link 1</a></li>
                <li><a href="#">Link 2</a></li>
                <li><a href="#">Link 3</a></li>
                <li><a href="#">Link 4</a></li>
                <li><a href="#">Link 5</a></li>
                <li><a href="#">Link 6</a></li>
                <li><a href="#">Link 7</a></li>
                <li><a href="#">Link 8</a></li>
                <li><a href="#">Link 9</a></li>
                <li><a href="#">Link 10</a></li>
            </ul>
            <ul class="ultiga">
                <li><a href="#">Link 1</a></li>
                <li><a href="#">Link 2</a></li>
                <li><a href="#">Link 3</a></li>
                <li><a href="#">Link 4</a></li>
                <li><a href="#">Link 5</a></li>
                <li><a href="#">Link 6</a></li>
                <li><a href="#">Link 7</a></li>
                <li><a href="#">Link 8</a></li>
                <li><a href="#">Link 9</a></li>
                <li><a href="#">Link 10</a></li>
            </ul>
        </p>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid, blanditiis. Quam unde itaque voluptatem possimus excepturi ea totam. Laborum ab soluta voluptatem iste voluptatibus quae nesciunt labore similique cumque atque.
        </p>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea nesciunt praesentium iure atque magni obcaecati deserunt, sequi autem, similique iste, vero dolor animi perferendis? Eveniet inventore officiis neque nisi reiciendis!
        </p>
    </body>
</html>
```

Oke, kita melakukan banyak perubahan pada kode HTML, yaitu menambah jumlah link, dan yang paling penting, adalah membuat **class** pada setiap list (unordered list) yang kita buat.

Lalu, kita siapkan kode CSS dengan kode seperti berikut:

```css
.ulsatu li:nth-child(3) a {
    color: green;
}

.uldua li:nth-child(2n) a {
    color: red;
}

.ultiga li:nth-child(3n-2) a {
    color: orange;
}

```

Berikut penjelasanya:
- Selector pertama **.ulsatu li:nth-child(3) a {}**, memiliki arti: "CSS, carikan aku tag `<a>`, yang berada didalam tag `<li>` dengan nomor urut 3, dan berada di elemen dengan class *ulsatu*. Lalu berikan warna hijau".
- Selector kedua **.uldua li:nth-child(2n) a {}**, memiliki arti : "CSS, carikan aku tag `<a>`, yang berada didalam tag `<li>` dengan nomor urut kelipatan 2, dan berada di elemen dengan class *uldua*. Lalu berikan warna merah".
- Selector ketiga **.uldua li:nth-child(3n-2) a {}**, memiliki arti : "CSS, carikan aku tag `<a>`, yang berada didalam tag `<li>` dengan nomor urut kelipatan 3, lalu dikurangi 2, dan berada di elemen dengan class *ultiga*. Lalu berikan warna orange".

Kode CSS diatas, akan menghasilkan tampilan seperti dibawah ini:

![[8 CSS Pseudo Class-2.png]]

Penggunaan *nth-child* juga bisa menggunakan parameter ganjil (odd) dan genap (even), berikut contoh modifikasi kode CSS untuk menampilkanya:

```css
.ulsatu li:nth-child(even) a {
    color: green;
}

.uldua li:nth-child(odd) a {
    color: red;
}
```

Maka, output HTML yang keluar adalah sebagai berikut:

![[8 CSS Pseudo Class-3.png]]
### Latihan menggunakan dua pseudo class bersamaan
Pseudo-class juga tentu bisa digunakan bersamaan dalam kondisi tertentu, misal kita menggunakan pemberian warna pada link dalam urutan genap, dan ketika kursor mouse berada diatas link tersebut, ukuran, dan warnanya berubah.

Berikut kode CSS-nya:

```css
.ulsatu li:nth-child(even) a {
    color: green;
}

.ulsatu li:nth-child(even) a:hover{
    color: red;
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
    font-style: italic;
}
```

Berikut penjelasanya:
- Selector pertama **.ulsatu li:nth-child(even) a {}**, memiliki arti: "CSS, carikan aku tag `<a>`, yang berada didalam tag `<li>` dengan nomor genap, dan berada di elemen dengan class *ulsatu*. Lalu berikan warna hijau".
- Selector kedua melakukan pencarian yang sama seperti selector pertama, namun kita menambahkan *pseudo-class* lain, yaitu **:hover**. Dimana ketika mouse berada diatas link yang berada di urutan genap, maka akan memberi style yang telah ditentukan.

Berikut hasil live demonya:

![[20241010-1409-41.5462122.mp4]]
## pseudo-class yang berhubungan dengan posisi elemen(2)
Pseudo-class yang berhubungan dengan posisi elemen jenis kedua, adalah sebagai berikut:
- **:first-of-type** : Memilih elemen pertama dari sebuah jenis / tipe tag
- **:last-of-type** : Memilih elemen terakhir dari sebuah jenis / tipe tag

Sekarang mari kita coba rubah kode HTML, menjadi memiliki 3 paragraf seperti berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Contoh Penggunaan Pseudo Class</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1>Penggunaan pseudo class</h1>
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa aut a sunt quaerat, voluptatibus ipsa debitis dolores, beatae quibusdam praesentium animi mollitia quas, sequi officiis eum sint fuga voluptatem veritatis.
    </p>
    <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Cumque quaerat distinctio libero expedita esse perspiciatis quod necessitatibus ullam ut laudantium iure qui provident cupiditate eum soluta, sapiente hic debitis maiores.
    </p>
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima quae soluta, autem quibusdam delectus fugiat obcaecati minus provident adipisci rerum. Aperiam, quam necessitatibus accusamus maxime nemo quod beatae cupiditate hic!
    </p>
    
</body>
</html>
```

Baiklah, sekarang kita langsung saja membuat kode CSS, dengan kode seperti berikut:

```css
p:first-of-type{
    color: red;
}

p:last-of-type{
    color: purple;
}
```

Penjelasan: 
- Selector pertama, akan memberikan style pada tag `<p>` pertama, dengan warna merah.
- Selector pertama, akan memberikan style pada tag `<p>` terakhir, dengan warna ungu.

Maka hasilnya akan tampil seperti ini:

![[8 CSS Pseudo Class-4.png]]

---
Oke mungkin itu beberapa pseudo-class yang telah kita pelajari, sebenarnya masih banyak pseudo-class yang lain, namun akan kita pelajari secara bertahap di pembelajaran selanjutnya. Sekian, dan stay strong!!