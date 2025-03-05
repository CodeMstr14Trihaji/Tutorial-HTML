---
obsidianUIMode: preview
sumber: WPU
level: pemula
bahasa: CSS
tanggal_study: 2024-10-12T13:13:00
total_study: 1
tags:
  - CSS
id: WPUCSSLOT4
sr-due: 2024-10-14
sr-interval: 2
sr-ease: 150
---

# Box Model CSS
Konsep dasar dari Box Model:
- Setiap elemen di halaman berada di dalam sebuah box (kotak)
- kita bisa mengatur ukuran dan posisi kotak tersebut
- Kita bisa memberi warna / gambar sebagai background kotak tersebut

Untuk memahami apa itu konsep box model dalam CSS, coba buka situs, katakanlah situs https://www.kompas.com/. Lalu lakukan step-step berikut:
1. Klik kanan, lalu pilih *inspect*
2. ![[3 Box Model-1.png]]
Maka akan tampil tampilan seperti berikut, selanjutnya masuk ke menu *style*:

![[3 Box Model-2.png]]

Maka, akan tampil kode CSS yang digunakan oleh situs tersebut. Selanjutnya, klik tanda tambah (*+*), supaya kita bisa menambah kode CSS sendiri. Lalu ketik kode CSS berikut:

```css
* {
 border: 1px solid red;
 }
```

> Selector \* berguna untuk memilih semua elemen yang ada, dan lalu kita beri style berupa border berwarna merah dengan ketebalan 1px

Setelah menambahkan kode CSS diatas, maka otomatis tampilan browser kita akan menjadi seperti ini:

![[3 Box Model-3.png]]

Wow, sekarang semua isi web kita memiliki garis merah berbentuk kotak. Apa maksudnya?

**CSS Box Model** mendefinisikan 'kotak' yang dihasilkan oleh sebuah elemen, lalu menampilkanya sesuai dengan format visualnya.

**CSS Box Model** terdiri dari 4 komponen, yaitu:
1. **margin** : Area transparan disekitar kotak (diluar *border*)
2. **padding** : area transparan didalam kotak (antara *content* dan *border*)
3. **border** : Batas disekeliling *content* dan *padding*
4. **content** : konten sebenarnya di dalam box, bisa berupa teks atau gambar

Ilustrasinya adalah sebagai berikut:

![[3 Box Model-4.png]]

Yang bisa kita atur propertinya hanya 3, yaitu *margin*, *padding*, dan *border*. Properti untuk *margin*, *padding*, dan *border* contohnya adalah sebagai berikut:

| margin:       | padding:       | border:       |
| ------------- | -------------- | ------------- |
| margin-top    | padding-top    | border-top    |
| margin-right  | padding-right  | border-right  |
| margin-bottom | padding-bottom | border-bottom |
| margin-left   | padding-left   | border-left   |
| margin        | padding        | border        |
> kita juga bisa melihat box model dengan menggunakan fitur 3D view pada browser Firefox, bisa dicari sendiri bagaimana cara menampilkanya!

Untuk fase belajarnya, kita masuk ke tutorial selanjutnya!