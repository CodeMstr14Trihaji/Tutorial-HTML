---
obsidianUIMode: preview
sumber: petanikode
level: medium
bahasa: HTML
tanggal_study: 2024-10-09T21:04:00
total_study: 2
tags:
  - HTML
id: PTHTML9
sr-due: 2024-10-12
sr-interval: 3
sr-ease: 170
---
# Belajar HTML #09: Cara Membuat List di HTML

---

![Cara Membuat List di HTML](https://www.petanikode.com/img/html/html.png)

Jika kamu diminta menuliskan daftar barang yang harus dibeli pada dengan HTML..

..apa yang akan kamu lakukan?

Mungkin kamu bisa membuatnya seperti ini:

```html
<h1>Daftar Barang untuk dibeli:</h1>
<p>- Flash disk 64GB</p>
<p>- Kabel Data USB 3.0</p>
<p>- Kertas A4</p>
```

Hasilnya memang akan terlihat seperti sebuah list.

![List dengan paragraf](https://www.petanikode.com/img/html/list/list-paragraf.png)

Tapi, ini bukanlah cara membuat list yang benar di HTML.

## Elemen List di HTML

HTML sudah menyediakan elemen untuk membuat list. Ada tiga macam jenis list yang bisa dibuat di HTML:

1. **Ordered List** adalah list yang terurut;
2. **Unordered List** adalah list yang tak terurut;
3. dan **Descriptiona List** adalah list yang berisi definisi.

Mari kita bahas satu-per-satu…

### 1. Ordered List di HTML

_Ordered list_ dibuat dengan tag `<ol>`. Lalu di dalamnya diisi dengan item-item yang akan dimasukkan ke dalam list. Item dibuat dengan tag `<li>` _(list item)_.

![Ordered list](https://www.petanikode.com/img/html/list/ol.png)

Contoh:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Membuat Ordered List</title>
</head>

<body>
    <h1>Buah Favoritku:</h1>
    <ol>
        <li>Jeruk</li>
        <li>Durian</li>
        <li>Pisang</li>
        <li>Pepaya</li>
        <li>Mangga</li>
    </ol>
</body>
</html>
```

Hasilnya:

![Contoh ordered list](https://www.petanikode.com/img/html/list/contoh-ol.png)

List di atas diurutkan berdasarkan angka dari `1`, `2`, `3`, sampai `5`.

Lalu bagaimana kalau kita ingin menggunakan huruf seperti `a`, `b`, `c` atau angka romawi seperti `I`, `II`, `III`?

Gampang..

Untuk membuat yang seperti itu, kita bisa menggunakan atribut `type` pada tag `ol` dan berikut ini nilai yang bisa diberikan:

- `a` untuk alfabet `a`, `b`, `c`, dan seterusnya;
- `A` untuk alfabet `A`, `B`, `C`, dan seterusnya;
- `i` untuk angka romawi `i`, `ii`, `iii`, dan seterusnya;
- `I` untuk angka romawi `I`, `II`, `III`, dan seterusnya.

Contoh:

```html
<!DOCTYPE html>
<html>

<head>
    <title>Ordered List dengan Atribut Type</title>
</head>

<body>
    <h3>List dengan type alfabet</h3>
    <ol type='a'>
        <li>Tutorial List di HTML</li>
        <li>Tutorial Link di HTML</li>
        <li>Tutorial Tabel di HTML</li>
    </ol>
    <h3>List dengan type alfabet kapital (huruf besar)</h3>
    <ol type='A'>
        <li>Tutorial List di HTML</li>
        <li>Tutorial Link di HTML</li>
        <li>Tutorial Tabel di HTML</li>
    </ol>
    <h3>List dengan type romawi</h3>
    <ol type='i'>
        <li>Tutorial List di HTML</li>
        <li>Tutorial Link di HTML</li>
        <li>Tutorial Tabel di HTML</li>
    </ol>
    <h3>List dengan type romawi kapital</h3>
    <ol type='I'>
        <li>Tutorial List di HTML</li>
        <li>Tutorial Link di HTML</li>
        <li>Tutorial Tabel di HTML</li>
    </ol>
</body>

</html>
```

Hasilnya:

![Contoh ordered list dengan type](https://www.petanikode.com/img/html/list/ol-type.png)

### 2.Unordered List di HTML

_Unordered list_ adalah list yang tak terurut yang menggunakan simbol-simbol pada item-nya. _Unordered list_ dibuat dengan tag `<ul>` dan untuk item-nya dibuat juga dengan tag `<li>`.

![Tag ul di HTML](https://www.petanikode.com/img/html/list/ul.png)

Contoh:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Membuat Unordered List</title>
</head>

<body>
    <h1>Bahasa Pemrograman untuk dipelajari:</h1>
    <ul>
        <li>Javascript</li>
        <li>PHP</li>
        <li>Java</li>
        <li>Python</li>
        <li>Kotlin</li>
    </ul>
</body>
</html>
```

Hasilnya:

![Contoh unordered list](https://www.petanikode.com/img/html/list/contoh-ul.png)

Secara default simbol yang digunakan oleh unordered list adalah lingkaran kecil _(disc)_. Kita juga bisa menggantinya dengan atribut `type`.

Berikut ini nilai yang bisa diberikan untuk atribut `type`:

- `square` untuk simbol persegi;
- `disc` (default) untuk simbol lingkaran disc;
- `none` tidak memakai simbol;
- `circle` untuk simbol lingkaran;

Contoh:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Membuat Unordered List</title>
</head>

<body>
    <h1>Bahasa Pemrograman untuk dipelajari:</h1>
    <ul type="square">
        <li>Javascript</li>
        <li>PHP</li>
        <li>Java</li>
        <li>Python</li>
        <li>Kotlin</li>
    </ul>
    <h1>Framework untuk dipelajari:</h1>
    <ul type="circle">
        <li>Vuejs</li>
        <li>Svelte</li>
        <li>Reactjs</li>
    </ul>
    <h1>Tools untuk dipelajari:</h1>
    <ul type="none">
        <li>Gulp</li>
        <li>NPM</li>
        <li>Js Lint</li>
    </ul>
    <h1>Pelajari juga:</h1>
    <ul type="disc">
        <li>JSON</li>
        <li>XML</li>
        <li>Markdown</li>
    </ul>
</body>
</html>
```

Hasilnya:

![Contoh type untuk ul](https://www.petanikode.com/img/html/list/ul-type.png)

Selain menggunakan type, kita juga bisa menggunakan gambar.

Ini dilakukan dengan style CSS.

Contohnya:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Membuat Unordered List</title>
</head>

<body>
    <h1>Bahasa Pemrograman untuk dipelajari:</h1>
    <ul style="list-style-image: url(https://assets.ubuntu.com/sites/ubuntu/latest/u/img/favicon.ico)">
        <li>Javascript</li>
        <li>PHP</li>
        <li>Java</li>
        <li>Python</li>
        <li>Kotlin</li>
    </ul>
</body>
</html>
```

Hasilnya:

![UL dengan icon](https://www.petanikode.com/img/html/list/ul-image.png)

### 3. Description List di HTML

_Description List_ adalah list yang berisi deskripsi atau penjelasan dari sesuatu.

Ada tiga tag yang digunakan untuk membuat description list:

- `<dl>` (description list) tag untuk memulai description list;
- `<dt>` (description term) tag untuk membuat kata yang akan dideskripsikan;
- `<dd>` (description description) tag untuk membuat penjelasan dari kata.

Format penulisannya seperti ini:

![Description list di HTML](https://www.petanikode.com/img/html/list/dl.png)

Contoh:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Membuat Description List</title>
</head>

<body>
    <h1>Daftar istilah:</h1>
    <dl>
        <dt>Kopi</dt>
        <dd>Sebuah minuman berwarna hitam. Menurut pendapat lain kopi adalah air yang dimasak sampai gosong.</dd>
        <dt>Kopi Black Magic</dt>
        <dd>Kopi hitam atau kopi tradisional yang dibuat dengan mantra-mantra.</dd>
        <dt>White Coffee</dt>
        <dd>Kopi berwarna putih, kandungan kafeinnya sedikit.</dd>
        <dt>Kopi++</dt>
        <dd>Kopi ini mampu meningkatkan imajinasi 99 kali lipat.</dd>
    </dl>
</body>

</html>
```

Hasilnya:

![Contoh description list](https://www.petanikode.com/img/html/list/contoh-dl.png)

## List di dalam List (Nested List)

List juga dapat dibuat di dalam list, misalkan kita ingin menggabungkan ordered list dengan unordered list.

Caranya, list yang di dalam ditulis di dalam tag `<li>`.

Contoh:

```html
<!DOCTYPE html>
<html lang='en'>

<head>
    <title>List di dalam List</title>
</head>

<body>
    <h1>Distro Linux dan Keluarganya</h1>
    <ol>
        <li>Debian
            <ul>
                <li>Ubuntu</li>
                <li>Mint</li>
                <li>elementaryOS</li>
            </ul>
        </li>
        <li>RedHat
            <ul>
                <li>Fedora</li>
            </ul>
        </li>
        <li>Slackware</li>
    </ol>
</body>

</html>
```

Hasilnya:

![Contoh list nested](https://www.petanikode.com/img/html/list/list-nested.png)

## Apa Selanjutnya?

Materi tentang list sampai di sini ya..

Intinya:

Kamu harus tahu cara membuat list, baik itu ordered list, unordered list, dan juga description list.

Jika masih bingung, silakan tanyakan di komentar.

Selanjutnya silakan pelajari:
- [[10 Belajar HTML Cara Membuat Tabel di HTML]]