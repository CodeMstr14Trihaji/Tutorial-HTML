---
obsidianUIMode: preview
sumber: petanikode
level: pemula
bahasa: HTML
tanggal_study: 2024-10-10T20:10:00
total_study: 4
tags:
  - HTML
id: PTHTML2
sr-due: 2024-10-13
sr-interval: 3
sr-ease: 170
---
# Belajar HTML #02: Apa itu Tag, Elemen, dan Atribut dalam HTML?

---

![Pengertian tag, elemen, dan atribut pada HTML](https://www.petanikode.com/img/html/html.png)

Tag, elemen, dan atribut merupakan tiga bagian penting yang ada di dalam HTML. Bagi kamu yang baru belajar HTML, wajib hukumnya untuk mengetahui ketiga Hal ini.

Apa itu Tag?

Apa itu Elemen?

Apa itu Atribut?

Serta apa perbedaan Tag, Elemen, dan Atribut?

Mari kita bahas…

## Apa itu Tag?

Tag adalah sebuah **penanda awalan** dan **akhiran** dari sebuah **elemen** di HTML. Tag dibuat dengan kurung sudut (`<...>`), lalu di dalamnya berisi nama tag dan kadang juga ditambahkan dengan atribut.

Contoh: `<p>`, `<a>`, `<body>`, `<head>`, dan sebagainya.

Tag selalu ditulis berpasangan. Ada tag pembuka dan ada tag penutupnya. Namun, ada juga beberapa [tag yang tidak memiliki pasangan penutup](https://www.petanikode.com/html-tag-tanpa-penutup/). Tag penutup ditulis dengan menambahkan garis miring (`/`) di depan nama tag.

![Penulisan tag pada HTML](https://www.petanikode.com/img/html/tag/tag.png)

Setiap tag memiliki fungsi masing-masing. Ada yang digunakan untuk membuat judul, membuat link, membuat paragraf, heading, dan lain-lain.

Masih ingat sejarah HTML?

Dulu.. awalnya HTML cuma punya **18 tag**. Sekarang HTML sudah punya sekitar **250** tag.

Wah! banyak ya.

Apa semua tag ini harus kita hafal?

Jawabannya:

**Tidak harus**, saja juga tidak bisa menghafal semuanya. Cukup ketahui tag-tag dasar saja.

Berikut ini daftar tag-tag dasar, yang menurut saya harus kamu ingat.

|Tag|Fungsi|
|---|---|
|`<html>`|untuk memulai dokumen HTML|
|`<head>`|untuk membuat bagian head|
|`<body>`|untuk membuat bagian body|
|`<h1>` sampai `<h6>`|[untuk membuat heading pada artikel](https://www.petanikode.com/html-heading/)|
|`<p>`|[untuk membuat paragraf](https://www.petanikode.com/html-paragraf/)|
|`<!-- -->`|untuk membuat komentar|

Beberapa tag ini sudah kita coba pada [tutorial pertama](https://www.petanikode.com/html-dasar/) dan juga ada yang belum.

Tenang saja.. Nanti juga saya akan perkenalkan tag-tag lain yang umum digunakan dalam pembuatan web.

Untuk saat ini, cukup pahami: **Apa itu tag dan cara menulisnya**.

### Cara Menulis Tag HTML yang Benar!

Beberapa orang kadang sering salah dalam menuliskan tag. Ada yang lupa menutup, ada yang salah mengetik namanya, dan semacamnya.

Berikut ini beberapa saran yang perlu diikuti agar bisa menulis tag dengan benar:

#### 1. Tag-tag wajib

Ada beberapa tag yang wajib ada di HTML. Tag ini harus kamu tulis.. kalau tidak, bisa jadi kode HTML-mu akan error menurut validator W3C.

Berikut ini daftar tag yang wajib ada di HTML:

- `<!DOCTYPE html>` — untuk deklarasi type dokumen;
- `<html>` — tag utama dalam HTML;
- `<head>` — untuk bagian kepala dari dokumen;
- `<title>` — untuk judul web;
- `<body>` — untuk bagian body dari dokumen.

#### 2. Gunakan Huruf Kecil

Hindari menggunakan huruf besar dalam menuliskan nama tag dan sebaiknya gunakan huruf kecil saja.

Huruf kecil lebih gampang diketik dan juga akan membuat kode HTML terlihat lebih bersih dan rapi.

Contoh: (bagus)

```html
<body>
<p>Belajar tentang tag di HTML</p>
</body> 
```

Contoh: (buruk)

```html
<BODY>
<P>Belajar tentang tag di HTML</P>
</BODY> 
```

Tapi khusus untuk tag `<!DOCTYPE html>`.. ia ditulis dengan huruf besar. Sebenarnya bisa juga dengan huruf kecil dan akan valid menurut validator W3C.

Tapi untuk dokumen XHTML, menggunakan `DOCTYPE` dengan huruf kecil akan mengakibatkan error.

#### 3. Pastikan Menutup Tag dengan Benar

Tag HTML nantinya akan ditulis bertumpuk-tumpuk. Artinya, di dalam tag ada tag lagi. Kadang kita sering salah dalam menutup tag yang bertumpuk ini. Akibatnya, kode HTML kita tidak valid.

Tapi tenang saja.. saya punya resep agar kamu mudah mengingatnya:

Jika kamu paham maksud dari jokes di atas, maka bagus.. saya tidak perlu jelaskan lagi.

Tapi kalau belum paham, berikut ini penjelasannya:

Tag yang pertama dibuat, harus ditutup terakhir. Bukan ditutup pertama.

Contoh:

```html
<i><b><u>memasak</u></b></i>
```

Tag `<i>` ditutup terakhir, karena ia yang ditulis pertama. Lalu tag `</u>` ditutup pertama kali karena ia berada di dalam tag `<b>` dan `<i>`.

## Apa itu Elemen?

Elemen dalam HTML adalah sebuah komponen yang menyusun dokumen HTML. Elemen kadang juga disebut sebagai _node_, karena ia merupakan salah satu jenis _node_ yang menyusun dokumen HTML dalam diagram HTML tree.

![HTML Tree (sumber: w3schools.com)](https://www.petanikode.com/img/js/dom/pohon-html.gif)

HTML Tree (sumber: w3schools.com)

Pada diagram tersebut, terdapat tiga macam _node_.. yakni: **Node elemen**, **Node atribut**, dan **Node teks**.

Elemen dibentuk dari **tag pembuka**, **isi tag**, dan **tag penutup**. Kadang juga ditambahkan beberapa atribut.

Contoh:

![Elemen di HTML](https://www.petanikode.com/img/html/tag/element.png)

Pada contoh di atas, terdapat satu elemen `<p>` dengan atribut `align="center"` dan memiliki isi berupa teks, yakni `Hello World!`.

Elemen tidak selalu berisi teks, kadang ia juga akan berisi elemen lain. Ini biasanya kita sebut dengan _nested element_ atau elemen di dalam elemen.

Bila digambarkan dalam bentuk kotak persegi, maka akan terlihat seperti ini:

![Elemen pada HTML](https://www.petanikode.com/img/html/tag/element-html.png)

Elemen HTML ada banyak jenisnya. Ada elemen khusus untuk teks, ada elemen untuk multimedia, script, tabel, metadata, dll. Nanti kita akan pelajari ini secara bertahap. Semua jenis elemen HTML bisa kamu baca di sini: [HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

Beberapa elemen HTML kadang ditambahkan atribut sebagai pelengkap.

## Apa itu Atribut?

Atribut adalah kata kunci khusus yang berada di dalam tag pembuka. Atribut juga disebut sebagai _modifier_ yang akan menentukan perilaku dari elemen.

![Atribut dalam HTML](https://www.petanikode.com/img/html/tag/atribut.png)

Atribut dapat ditambahkan pada elemen manapun. Ada juga elemen yang mewajibkan menggunakan atribut seperti elemen `<a>`, `<img>`, `<video>`, dll.

Contoh:

```html
<a href="https://petanikode.com">Petani Kode.com</a>
```

Tag `<a>` adalah tag untuk membuat link. Tag ini mewajibkan menambahkan atribut `href` untuk menyatakan halaman tujuan dari link.

Jumlah atribut pada elemen bisa lebih dari satu.

Contoh:

```html
<img src="gambar.jpg" width="100" height="100" />
```

Atribut `src` adalah atribut khusus untuk tag `<img>` yang fungsinya untuk menentukan gambar yang akan ditampilkan. Lalu atribut `width` dan `height` adalah atribut yang mengatur ukurannya.

### Jenis-jenis Atribut HTML

Tiap-tiap elemen kadang memiliki atribut khusus yang hanya bisa digunakan pada elemen tersebut. Ada juga atribut yang bersifat global dan bisa ditambahkan ke semua elemen.

Berikut ini jenis-jenis atribut yang harus diketahui:

#### 1. Atribut Global

Atribut Global adalah atribut yang bisa ditambahkan pada semua elemen HTML.

Berikut ini daftar atribut global dan fungsinya:

|Nama Atribut|Deskripsi atau fungsi|
|---|---|
|`accesskey`|Menentukan tombol _shortcut_ untuk mengaktifkan atau fokus pada elemen|
|`class`|Menentukan _class CSS_ yang akan digunakan|
|`contenteditable`|Menentukan isi elemen bisa diedit atau tidak|
|`data-*`|Digunakan untuk menyimpan data|
|`dir`|Menentukan arah teks dari elemen (kiri ke kanan atau sebaliknya)|
|`draggable`|Menentukan apakah elemen bisa di _drag_ atau tidak|
|`hidden`|untuk menyembunyikan elemen|
|`id`|Menentukan id unik untuk elemen|
|`lang`|Menentukan bahasa yang digunakan untuk isi elemen|
|`spellcheck`|Menentukan apakah isi elemen harus dilakukan pengejaan _grammar_ atau tudak|
|`style`|Menentukan _inline CSS_ untuk elemen|
|`tabindex`|Menentukan urutan atau indeks tab dari elemen (saat tombol tab ditekan)|
|`title`|Menentukan informasi tambahan tentang elemen|
|`translate`|Menentukan apakah konten dari elemen bisa diterjemahkan atau tidak|

#### 2. Atribut Event

Atribut event adalah atribut yang digunakan untuk menentukan aksi yang akan dilakukan saat terjadi sesuatu pada elemen. Atribut ini nanti akan banyak digunakan pada [pemrograman Javascript](https://www.petanikode.com/tutorial/javascript/).

Berikut ini daftar atribut event saat terjadi sesuatu pada Jendela browser:

|Nama atribut|Nilai|Fungsi: Menjalankan script|
|---|---|---|
|`onafterprint`|kode javascript|setelah dokumen dicetak|
|`onbeforeprint`|kode javascript|sebelum dokumen dicetak|
|`onbeforeunload`|kode javascript|sebelum saat dokumen tidak ter-load|
|`onerror`|kode javascript|saat terjadi error|
|`onhashchange`|kode javascript|saat terjadi perubahan pada bagian _anchor_ di URL|
|`onload`|kode javascript|setelah _loading_ selesai|
|`onmessage`|kode javascript|saat ada pesan|
|`onoffline`|kode javascript|saat tiba-tiba offline|
|`ononline`|kode javascript|saat tiba-tiba online|
|`onpagehide`|kode javascript|saat user tidak sedang membuka halaman web|
|`onpageshow`|kode javascript|saat user membuka kembali halaman web|
|`onpopstate`|kode javascript|saat history browser berubah|
|`onresize`|kode javascript|saat ukuran jendela browser berubah|
|`onstorage`|kode javascript|saat area penyimpanan (Web Storage) di-update|
|`onunload`|kode javascript|saat web browser ditutup|

Selain atribut tersebut, masih banyak lagi atribut event yang lainnya. Semuanya bisa kamu lihat di: [HTML Event Attributes](https://www.w3schools.com/tags/ref_eventattributes.asp).

#### 3. Atribut Khusus

Atribut khusus adalah atribut yang hanya bisa dipakai pada elemen tertentu dan kadang atribut ini tidak bisa digunakan pada elemen yang lain.

Contoh:

|Nama atribut|Bisa dipakai di tag|
|---|---|
|`src`|`<audio>`, `<embed>`, `<iframe>`, `<img>`, dll|
|`href`|`<a>`, `<link>`|
|`action`|`<form>`|
|`autoplay`|`<audio>`, `<video>`|

### Cara Menulis Atribut yang Benar!

Penulisan atribut sebenarnya gampang.. kita hanya perlu menambahkannya pada tag pembuka dengan format seperti ini:

```html
bana-atribut="nilai"
```

Namun, ada beberapa hal yang perlu diperhatikan agar penulisannya benar dan valid:

#### 1. Gunakan Huruf Kecil

Menulis atribut dengan huruf besar sah-sah saja, dan bahkan valid menurut validator W3C.

Tapi saya sarankan menggunakan huruf kecil saja. Karena lebih umum digunakan dan juga mudah terbaca.

Contoh: (bagus)

```html
<p align="center">Belajar HTML di Petani Kode</p>
```

Contoh: (kurang bagus)

```html
<p ALIGN="CENTER">Belajar HTML di Petani Kode</p>
```

#### 2. Gunakan Tanda Petik

Gunakan tanda petik untuk mengisi nilai atribut yang mengandung teks.

Mengapa?

Karena jika terdapat lebih dari satu kata, ia akan menciptakan spasi dan akan dianggap sebagai atribut baru.

Contoh: (bagus)

```html
<h1 title="tutorial HTML untuk pemula">Belajar HTML</h1>
```

Contoh: (buruk)

```html
<h1 title=tutorial HTML untuk pemula>Belajar HTML</h1>
```

Tanda petik yang digunakan, boleh petik ganda (`"`) dan juga petik tunggal (`'`).

Nah untuk nilai angka, boleh pakai tanda petik dan juga boleh tidak.

Contoh:

```html
<img src="gambar.jpg" width=120 height=120 />
```

Lalu, untuk atribut yang bernilai boolean (`true` dan `false`).. nilainya boleh ditulis dan boleh tidak.

Contoh:

```html
<input type="text" required="true" />
<input type="text" required />
```

#### 3. Penggunaan Spasi

Jika ada atribut yang memiliki lebih dari satu nama, maka ia ditulis dengan tanda min (`-`), bukan spasi.

Contoh:

```html
<img data-src="gambar.jpg" />
```

Lalu, spasi juga digunakan untuk memisahkan dua atau lebih atribut.

Contoh:

```html
<img class="lazyload" data-src="gambar.jpg" src="placeholder.jpg" />
```

Bisa juga ditulis seperti ini:

```html
<img class="lazyload" 
    data-src="gambar.jpg" 
    src="placeholder.jpg" />
```

## Apa Selanjutnya?

Kita baru saja belajar tentang Tag, Atribut, dan Elemen dalam HTML. Saya kira kamu sudah dapat membedakan ketiga hal ini.

Elemen adalah komponen yang menyusun dokumen HTML. Sedangkan Tag adalah penanda untuk memulai dan mengakhiri elemen. Lalu atribut adalah _modifier_ untuk menentukan perilaku elemen.

Nah, selanjutnya kita akan berkenalan dengan elemen-elemen dasar di HTML seperti paragraf, heading, list, tabel, link, form, dan lain-lain.

Karena itu, silakan lanjutkan pelajari tentang:

- [[3 Belajar HTML Membuat Paragraf pada HTML]]

