---
obsidianUIMode: preview
sumber: WPU
level: medium
bahasa: CSS
tanggal_study: 2024-10-12T20:49:00
total_study: 1
tags:
  - CSS
id: WPUCSSLOT6
sr-due: 2024-10-13
sr-interval: 1
sr-ease: 130
---
# Box Model Padding, Border & Sizing
Jika sebelumnya kita sudah membahas tuntas seri Box Model Margin, maka sekarang kita akan membahas Box Model seri Padding, Border & Sizing. Sekedar pengingat saja, ini adalah gambar Box Model:

![[3 Box Model-4.png]]

CSS Box Model terdiri dari 4, yaitu:
- **margin** : Area transparan disekitar kotak (diluar border)
- **padding** : Arean transparan didalam kotak (antara content dan border)
- **border** : batas disekeliling content dan padding
- **content** : konten sebenarnya di dalam box, bisa berupa teks atau gambar

**Padding** biasa digunakan untuk memberikan jarak antara sebuah kotak dengan tulisan yang ada didalamnya. Berikut contoh penggunaanya:
## Penggunaan Padding
Tulis kode HTML berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba Padding dan Border</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Corporis est repellendus dolorum nisi ex molestiae repudiandae magnam, corrupti possimus vel laudantium, voluptate tempora nobis omnis eius voluptatem rem, reprehenderit animi.</div>
</body>
</html>
```

Lalu buat kode CSS berikut:

```css
div {
    width: 300px;
    height: 300px;
    background-color: coral;
    margin: 20px auto;
}
```

Dengan kode seperti diatas, maka hasil outputnya akan seperti ini:

![[5 Box Model Padding, Border & Sizing-1.png|500]]

Nah, sekarang, kita coba tambahkan padding pada kode CSS diatas, berikut kode CSS yang perlu kita tambahkan:

```css
div {
    width: 300px;
    height: 300px;
    background-color: coral;
    margin: 20px auto;
    padding-left: 100px;
}
```

Sekarang, kita menambahkan *padding-left* dengan value **100px**, maka akan menghasilkan output seperti berikut:

![[5 Box Model Padding, Border & Sizing-2.png|500]]

Kotak akan melebar kekiri, sebanyak **100px**, karena kita menggunakan *padding-left*. Jika kita meng *inspect* halaman, dan melihat ke *computed*, maka akan terlihat box model disitu. Kita bisa melihat ukuran padding dari elemen yang kita gunakan seperti berikut:

![[5 Box Model Padding, Border & Sizing-3.png]]

Pemberian value **padding** juga bisa dilakukan secara shorthand, yaitu seperti kita mengisi value **margin**, dimana kita mengisi value properti dengan 1, 2, 3, atau 4 value sekaligus. Tetapi, ada hal-hal yang perlu diperhatikan ketika kita ingin mengisi value **padding** dengan cara ini.

---
Ada beberapa hal yang perlu diperhatikan dalam penggunaan **padding**, yaitu:
- Padding tidak bisa diberi nilai negatif
- Padding tidak memiliki nilai **auto**
- Padding memengaruhi ukuran elemen, atau box yang kita buat. Jika kita sudah menentukan **width** & **height**, penggunaan **padding** akan membuat ukuran tersebut berubah.
## Penggunaan Border
Dengan kode HTML yang sama, kita rubah kode CSS menjaddi seperti ini:

```css
div {
    width: 300px;
    height: 300px;
    background-color: coral;
    margin: 20px auto;
    padding: 50px;
    border: 5px solid black;
}
```

Disini, kita membuat **padding** memiliki 4 sisi yang memiliki nilai **40px**. Tidak kurang juga menambahkan properti **border**. Jadi, metode pengisian dari properti ini bisa menggunakan format sebagai berikut:

```css
div { border: width style color;}
```

Sehingga, akan tampil tampilan seperti ini pada browser:

![[5 Box Model Padding, Border & Sizing-4.png|500]]

Untuk *style* dari **border** bisa menggunakan tipe **solid**, **dotted**, **dashed**, dan **double**. Untuk hasilnya mungkin akan seperti ini:

![[5 Box Model Padding, Border & Sizing-5.png|200]]

Properti ini juga tetap bisa diisi value perbaris, tidak sekaligus seperti diatas, kode CSS-nya:

```css
div {
    width: 300px;
    height: 300px;
    background-color: coral;
    margin: 20px auto;
    padding: 50px;
    border-width: 5px;
    border-style: double;
    border-color: black;
}
```

Hasilnya:

![[5 Box Model Padding, Border & Sizing-6.png|500]]


Kita juga bisa membuat hanya sisi tertentu saja dari kotak yang mendapat **border**, caranya adalah seperti berikut:

```css
div {
    width: 300px;
    height: 300px;
    background-color: coral;
    margin: 20px auto;
    padding: 50px;
    border-left: 5px solid black;
}
```

Maka hasilnya:

![[5 Box Model Padding, Border & Sizing-7.png|500]]

Jika ingin membuat yang lebih kompleks, bisa seperti ini:

```css
div {
    width: 300px;
    height: 300px;
    background-color: coral;
    margin: 20px auto;
    padding: 50px;
    border-left: 5px solid black;
    border-right: 10px dashed blue;
    border-top: 5px dotted green;
    border-bottom: 10px solid red;
}
```

Maka hasilnya:

![[5 Box Model Padding, Border & Sizing-8.png|500]]

---
Berikut materi tambahan tentang **border**:
- Border juga menambah ukuran elemen, jadi jika kita memberi style `border:5px;`, maka kita akan menambah dimensi dari semua sisi sebanyak **5px** sebagai tempat menampung **border**.

Tips: Jika ingin mengetahui luas total dari dimensi kotak yang kita buat, maka kita perlu memperhatikan penggunaan **margin**, **padding**, dan **border** yang kita gunakan. Anda bisa mengkalkulasi sendiri, atau melihat total dimensinya dengan cara *inspect* lalu melihat ke *box model*.

---
Sebenearnya, CSS juga menyediakan properti untuk membantu kita mengkalkulasi luas box model yang kita gunakan, dan, inilah yang akan kita pelajari selanjutnya.
## Box sizing
Box sizing merupakan fitur baru yang muncul di CSS 3. Fitur ini berguna agar kita tidak perlu mengkalkulasikan total dimensi yang kita buat. Contohnya seperti ini:

> Biasanya, ketika kita membuat elemen, yang biasa kita atur adalah panjang dimensinya saja. Untuk tingginya, jarang kita atur, karena biasanya, semakin banyak konten didalamnya, maka kotak tersebut akan semakin tinggi. Ketika kita mengatur tingginya, ketika konten didalamnya terlalu banyak, maka konten tersebut akan keluar dari wadahnya. Jadi, biasakan untuk mengatur lebarnya, bukan tingginya.

Buat kode HTML dengan 2 tag `<div>` seperti ini:

```HTML
<!DOCTYPE html>
<html>
<head>
    <title>Coba Padding dan Border</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="satu">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Corporis est repellendus dolorum nisi ex molestiae repudiandae magnam, corrupti possimus vel laudantium, voluptate tempora nobis omnis eius voluptatem rem, reprehenderit animi.</div>

    <div class="dua">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Rerum nulla, inventore est optio, iure eveniet magnam ab, quo voluptates aliquam mollitia explicabo aspernatur? Ipsum aperiam nobis libero porro repellendus nostrum.</div>
</body>
</html>
```

Lalu buat kode CSS:

```css
div {
    width: 600px;
    margin: 10px auto;
}

.satu {
    background-color: royalblue;
    padding: 10px;
    border: 5px solid red;
}

.dua {
    background-color: lightgreen;
    padding: 30px;
    border: 10px dashed orange;
}
```

Ini adalah kode CSS tanpa *box-sizing*, hasilnya nanti akan membuat kotak memiliki ukuran yang berbeda-beda dan tidak rapi. Karena walaupun sudah diset untuk memiliki lebar atau **width: 600px**, penggunaan properti *padding*, dan *border* akan membuat ukuranya bertambah. Solusinya adalah menggunakan *box-sizing* seperti ini:

```css
div {
    width: 600px;
    margin: 10px auto;
    box-sizing: border-box;
}

.satu {
    background-color: royalblue;
    padding: 10px;
    border: 5px solid red;
}

.dua {
    background-color: lightgreen;
    padding: 30px;
    border: 10px dashed orange;
}
```

Maka, hasilnya akan memiliki perbedaan seperti ini:
--- start-multi-column: ID_g47w
```column-settings
Number of Columns: 2
Largest Column: standard
```

Tanpa box-sizing:

![[5 Box Model Padding, Border & Sizing-9.png|400]]

--- column-break ---

Dengan box-sizing

![[5 Box Model Padding, Border & Sizing-10.png|400]]


--- end-multi-column
Hasilnya tentu lebih rapi, dan ukuran dimensi tidak berubah-ubah. Sekian, semoga bisa dipahami.
