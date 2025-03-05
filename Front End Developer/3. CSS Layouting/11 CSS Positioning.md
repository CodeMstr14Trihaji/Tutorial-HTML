
# Position : Static & Relative
Baiklah, untuk bisa mempelajari materi ini, kita langsung saja menuju contoh. Kita buat kode HTML seperti ini:

Kode HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba Positioning</title>
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

Lalu kode CSS (style.css) dengan kode seperti ini:

```css
div {
    width: 200px;
    height: 200px;
}

.satu{
    background-color: lightgreen;
}

.dua {
    background-color: violet;
}

.tiga {
    background-color: gold;
}
```

Maka, hasilnya, atau outputnya akan seperti ini:

![[11 CSS Positioning-1.png]]

Sekarang, kita akan menccoba untuk menggeser kotak pink atau kotak tersebut ke arah kanan, katakanlah sebanyak **20px**, mungkin kode CSS yang kita buat, akan kita ganti menjadi seperti ini:

```css
.dua {
    background-color: violet;
    margin-left: 20px;
}
```

Maka, kotak kedua mungkin akan bergeser seperti ini;

![[11 CSS Positioning-2.png]]

Lalu, jika kita ingin menggeser kotak pink tersebu ke bawah sebanyak **30px**, mungkin kita perlu memberikanya margin, dan merubah kode CSS lagi menjadi seperti ini:

Tampilan keseluruhan CSS:

```css
div {
    width: 200px;
    height: 200px;
}

.satu{
    background-color: lightgreen;
}

.dua {
    background-color: violet;
    margin-left: 30px;
    margin-top: 30px;
}

.tiga {
    background-color: gold;
}
```

Maka, hasilnya menjaddi seperti ini:

![[11 CSS Positioning-3.png]]

Baiklah, apa masalahnya sekarang? Masalahnya adalah ketika kita menggunakan properti **margin**, maka elemen lain disekitar elemen yang kita edit akan ikut terpengaruh. 

Hal itu memang merupakan sifat dari **margin**, dimana ketika kita membuat margin pada suatu elemen, maka elemen lain akan ikut terpengaruh. Baik kotak tersebut kita geser ke bawah atau geser keatas dengan menggunakan kode CSS:

```css
.dua {
    background-color: violet;
    margin-left: 30px;
    margin-top: -30px;
}
```

. . .  maka kotak kuning atau kotak gold akan ikut terbawa dan terpengaruh:

![[11 CSS Positioning-5.png|500]]

Lalu, bagaimana caranya agar kita bisa menggeser kotak diatas, tanpa memengaruhi kotak disekitarnya? Jawabanya adalah kita menggunakan properti yang namanya **position**.

**position** memungkinkan kita, untuk menggeserkan sebuah elemen, tanpa memengaruhi elemen disekitarnya.
## CSS position
Untuk menggunakan properti ini, berikut value yang bisa digunakan didalamnya:
- **static** (default)
- **relative**
- **absolute**
- **fixed**

Jika kita tidak memberi nilai properti **position** pada sebuah elemen, maka secara default, nilai **position**-nya akan memiliki value *static*.

Berikut materi tentang **position**:
- *Static* adalah nilai default dari tiap-tiap elemen ketika tidak diberi properti position.
- Menggunakan position selain *static* (non-static), akan membuat sebuah elemen menjadi seolah-olah **berbeda dimensi** dari elemen lainya.
- Elemen yang diberi position selain *static* dapat menggunakan properti **top**, **left**, **bottom**, dan **right** untuk mengatur posisinya.
### Kasus pertama
Sekarang kita fokus pada kode CSS berikut:

```css
div {
    width: 200px;
    height: 200px;
}

.satu{
    background-color: lightgreen;
    position: static;
}

.dua {
    background-color: violet;
    position: relative;
}

.tiga {
    background-color: gold;
}
```

Maka outputnya akan menjadi seperti ini:

![[11 CSS Positioning-6.png]]

Untuk selector pertama, nilai `position: static` tidak akan mempengaruhi apapun, karena memang nilai default dari setiap properti **position** pada semua elemen adalah *static*.

Sedangkan ketika kita menggunakan `position: relative` pada selector kedua, juga tidak ada perubahan? Padahal bukan value default dari **position**? 

Untuk menjawab dan menjelaskan hal ini, kita perlu melihat kotak-kotak tersebut dalam kondisi 3 dimensi sebagai bantuan. Kita bisa menggunakan situs https://www.tinkercard.com , untuk membantu proses ini. 

## Ilustrasi value dari properti position
Jika kita menggunakan value *static*, maka posisi elemen div akan seperti ini:
--- start-multi-column: ID_m34r
```column-settings
Number of Columns: 2
Largest Column: standard
```

![[11 CSS Positioning-7.png]]

--- column-break ---

![[11 CSS Positioning-8.png]]

--- end-multi-column
Baik dari atas, maupun samping, elemen berada ditempat yang sama.

Jika salah satu elemen div yang kita gunakan, menggunakan properti **position** dengan value *relative*, maka ilustrasinya akan seperti ini:
--- start-multi-column: ID_r7mo
```column-settings
Number of Columns: 2
Largest Column: standard
```

![[11 CSS Positioning-9.png]]

--- column-break ---

![[11 CSS Positioning-10.png]]


--- end-multi-column
Jika kita melihatnya dari atas, mungkin tidak terlihat perbedaanya. Perbedaan baru terlihat ketika kita melihatnya dari samping, dimana ternyata, elemen div atau elemen kotak yang memiliki properti **position** dengan value *relative*, maju satu dimensi.

Ketika elemen ini maju satu dimensi, sekarang ia memiliki akses untuk menggunakan properti **top**, **left**, **bottom**, dan **right**, sehingga ia bisa bergeser kemanapun, tanpa memengaruhi elemen disekitarnya.
### Kasus kedua
Setelah kita tahu bagaimana cara menggunakanya, saatnya kita praktek. Tulis kode CSS berikut:

```css
div {
    width: 200px;
    height: 200px;
}

.satu{
    background-color: lightgreen;
    position: static;
}

.dua {
    background-color: violet;
    position: relative;
    top: 30px;
}

.tiga {
    background-color: gold;
}
```

Sekarang, dengan **position** berupa *relative*, kita bisa menggeser kotak pink tanpa masalah. Semisal kita geser kotak pink sebanyak **30px** kebawah, maka hasilnya seperti ini:

![[11 CSS Positioning-11.png]]

Pada intinya, value *relative* ini membuat sebuah elemen yang tadinya ada didalam **flow**, menjadi keluar dari **flow**, atau **out of flow**. Anggap saja maju satu dimensi. Dimomen ini, kotak bisa kita geser baik itu kebawah, keatas, kakanan, atau kekiri dengan leluasa, tanpa memengaruhi elemen disekitarnya. 
## Materi value Relative
Berikut adalah materi dari *relative*:
- 

