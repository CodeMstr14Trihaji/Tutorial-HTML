---
obsidianUIMode: preview
sumber: WPU
level: pemula
bahasa: CSS
tanggal_study: 2024-10-09T18:35:00
total_study: 1
tags:
  - CSS
id: WPUCSSD2
sr-due: 2024-10-11
sr-interval: 2
sr-ease: 150
---
# Anatomi CSS
Sama halnya seperti HTML, CSS juga memiliki anatomi tersendiri yang menyusun kode CSS, Berikut penjelasanya

CSS memilliki anatomi sebagai berikut:

```css
selector { property: value; }
```

Contoh penulisan CSS yang sesuai dengan anatomi yang disebutkan diatas adalah sebagai berikut:

```css
h1 { color: blue; }
```

Arti kode diatas artinya: "Buat semua tulisan didalam `<h1>`, dihalaman saya, menjadi berwarna biru"

h1 = selector
color = property
blue = value

Sekarang pahamkan, bagaimana anatomi CSS itu?
## Macam-macam cara penulisan CSS

CSS bisa dituliskan dengan 2 cara, jika style yang akan ditambahkan sedikit, mungkin bisa dibuat satu baris sebagai berikut:

```css
h1 {font-family:"Courier New"; text-align:"center"; font-size:30px; color: blue;}
```

Namun, jika style CSS yang diberikan sangat banyak, biasanya programmer membuat beberapa baris, dan cara ini juga lebih disarankan, karena lebih rapi, dan mudah dievaluasi jika seandainya terjadi kesalahan atau ingin dirubah nilainya:

```css
h1 {font-family: "Courier New";
	text-align: "center";
	font-size: 30px;
	color: blue;
	}
```

Jadi, setiap menulis satu style dan diakhiri tanda titik koma, kita berganti baris, dan menuliskan kode style baru, dan seterusnya.
# Selector
Berikut adalah materi tentang Selector:
- Digunakan untuk memilih dan memanipulasi elemen spesifik pada HTML
- Elemen HTML dipilih berdasarkan tag, id, class bahkan pola / pattern
- Semakin kompleks struktur HTML, selector juga bisa semakin kompleks / spesifik

Untuk memahami bagaimana cara kerja Selector, lihat ilustrasi berikut:

```css
h1 { color:blue; }
```

Maksudnya : *CSS, pilih seluruh elemen h1, lalu ubah teks didalamnya menjadi berwarna biru*
# Property & Value
Ada banyak sekali property pada CSS, namun kita cukup kenal property CSS yang umum digunakan saja pada tutorial selanjutnya, karena property CSS juga berjumlah 350++. Untuk contoh property dan value adalah sebagai berikut:

```css
background-color
background-image
background-position
background-repeat
border
border-collapse
border-color
border-spacing
border-top
border-right
float
font
font-family
font-size
font-style
font-variant
height
left

dst...
```

Jika ingin lebih memahami bagaimana cara kerja Property dan value secara lebih lengkap, bisa kunjungi https://developer.mozilla.org/en-US/docs/Web/CSS/Reference, atau kunjungi http://css-tricks.com/almanac. Disitus tersebut, kita bisa melihat, mulai dari A sampai Z tentang properti CSS, bagaimana cara menggunakanya, dan seperti apa contohhya.

