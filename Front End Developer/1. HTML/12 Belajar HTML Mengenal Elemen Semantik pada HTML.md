---
obsidianUIMode: preview
sumber: petanikode
level: medium
bahasa: HTML
tanggal_study: 2024-10-08T15:37:00
total_study: 1
tags:
  - HTML
id: PTHTML12
sr-due: 2024-10-10
sr-interval: 2
sr-ease: 152
---
# Belajar HTML #12: Mengenal Elemen Semantik pada HTML

---

![Html Semantics](https://www.petanikode.com/img/html/semantik/html-semantik.png)

Sejauh ini kita sudah mengenal beberapa tag dasar di HTML, seperti elemen [paragraf](https://www.petanikode.com/html-paragraf/), [heading](https://www.petanikode.com/html-heading/), [list](https://www.petanikode.com/html-list/), [tabel](https://www.petanikode.com/html-tabel/), [link](https://www.petanikode.com/html-link/), dan [form](https://www.petanikode.com/html-form/).

Lalu pertanyaannya:

Bagaimana cara menata elemen-elemen ini agar terlihat bagus?

Jawabannya:

Kita butuh sebuah _layout_.

Nah, di HTML terdapat beberapa elemen yang khusus untuk melakukan ini. Yakni elemen semantik seperti `<header>`, `<aside>`, `<footer>`, `<article>`, dll.

Elemen semantik sebenarnya tidak hanya digunakan untuk membuat layout saja. Ia juga digunakan untuk membuat elemen lain.

Untuk lebih jelasnya, mari kita pelajari lebih detail.

## Apa itu Elemen Semantik?

Jadi gini..

Di awal-awal hadirnya HTML dulu, elemen semantik belum ada.

Orang-orang membuat layout dengan menggunakan **tag yang salah**.

Ada yang membuatnya dengan tag `<tabel>` dan ada juga dengan tag `<div>`.

Ini sebenarnya tidak sepenuhnya salah, karena membuat layout dengan kedua tag itu benar-benar bisa.

Tapi..

Ini bukanlah cara yang baik dan akan membuat kode HTML kita sulit terbaca.

Karena itu.. hadirlah elemen semantik sebagai solusi.

Elemen semantik mulai ditambahkan pada HTML 5.

**Elemen semantik** adalah elemen-elemen yang **menyatakan makna** atau tujuan dari elemen itu sendiri. [1](https://www.petanikode.com/html-semantik/#fn:1)

Misalnya tag `<footer>`, tag ini digunakan untuk membuat elemen footer atau bagian kaki dari web.

Jangan gunakan tag ini di bagian paling atas, karena maknanya sudah jelas untuk footer.

Jadi tidak akan ada lagi yang namanya penyalahgunaan tag. Karena setiap tag sudah punya tujuan masing-masing.

Berikut ini daftar elemen-elemen semantik:

- `<article>` — untuk membuat elemen artikel;
- `<aside>` — untuk membuat elemen bagian samping;
- `<details>` — untuk membuat elemen detail atau spoiler;
- `<figcaption>` — untuk membuat teks caption pada figure;
- `<figure>` — untuk membuat figur atau gambar pada artikel;
- `<footer>` — untuk membuat elemen bagian kaki dari web;
- `<header>` — untuk membuat kepala kop dari web;
- `<main>` — untuk membuat elemen utama;
- `<mark>` — untuk menandai teks;
- `<nav>` — untuk membuat navigasi;
- `<section>` — untuk membuat bagian artikel;
- `<summary>` — untuk membuat ringkasan artikel atau isi spoiler;
- `<time>` — untuk membuat elemen yang menyatakan waktu;
- dan masih banyak lagi.

## Mengapa Harus Pakai Elemen Semantik?

Salah satu keuntungan menggunakan elemen semantik adalah dokumen HTML kita akan **mudah dibaca**, baik itu oleh manusia maupun mesin.

Coba perhatikan kode berikut:

```html
<div id="header"></div>
<div class="section">
	<div class="article">
		<div class="figure">
			<img>
			<div class="figcaption"></div>
		</div>
	</div>
</div>
<div id="footer"></div>
```

Ini adalah contoh layout yang dibuat dengan tag `<div>`. Tag ini memang bagus untuk membungkus elemen HTML.

Kamu mungkin akan mudah paham dengan membaca nama-nama class yang diberikan pada elemen `<div>`.

Ada `<div>` yang bertugas untuk membuat elemen _header_, _article_, _footer_, dan sebagainya.

Sekilas, tidak ada masalah dengan ini..

Tapi nanti kalau elemen `<div>` nya sudah banyak, kita akan kesulitan membacanya.

![Terlalu banyak tag div](https://www.petanikode.com/img/html/semantik/ryu-html.png)

Sekarang coba bandingkan dengan kode ini:

```html
<header></header>
<section>
	<article>
		<figure>
			<img>
			<figcaption></figcaption>
		</figure>
	</article>
</section>
<footer></footer>
```

Ini tentunya akan lebih muda dibaca.

Oh iya, elemen semantik juga **bagus untuk SEO**. Jadi kalau mau websitemu disukai mesin pencari, sebaiknya gunakanlah elemen ini.

## Membuat Layout dengan Elemen Semantik

Nah, sekarang mari kita belajar membuat layout dengan elemen semantik.

Buatlah file baru dengan nama `layout.html`, kemudian isi dengan kode berikut:

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Contoh Layout dengan Elemen Semantik</title>
</head>

<body>

  <header>
    <h1>Belajar Elemen Semantik di HTML</h1>
  </header>

  <nav>
    <a href="#">Home</a> |
    <a href="#">About</a> |
    <a href="#">Contact</a>
  </nav>

  <article>
    <h1>Tutorial Semantik Elemen untuk Pemula</h1>
    <p>Semantik elemen adalah elemen yang memiliki makna dan tujuan.
      Tujuannya agar kode HTML mudah dibaca dan tidak ada penyalahgunaan tag.
      Elemen semantik bagus untuk SEO dan juga dapat meningkatkan accessibility.
    </p>
  </article>

  <footer>
    Copyright &copy; 2020 by Petani Kode
  </footer>

</body>

</html>
```

Setelah itu, buka dengan web browser.

Maka hasilnya:

![Contoh semantik elemen di HTML](https://www.petanikode.com/img/html/semantik/contoh-semantik.webp)

Hasilnya akan terlihat biasa saja dan sama seperti contoh-contoh sebelumnya. Ini karena kita belum memberikan style CSS.

Karena itu, mari kita coba memberikan style CSS untuk elemen semantik.

## Style untuk Elemen Semantik

Cara memberikan style untuk elemen semantik sama saja seperti memberikan style pada elemen lainnya. Tinggal membuat atribut `style`, lalu mengisinya dengan kode style CSS.

Oke, sekarang coba ubah contoh yang tadi menjadi seperti ini:

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Contoh Layout dengan Elemen Semantik</title>
</head>

<body style="background-color: silver;">

  <header style="background-color: white;">
    <h1>Belajar Elemen Semantik di HTML</h1>
  </header>

  <nav>
    <a href="#">Home</a> |
    <a href="#">About</a> |
    <a href="#">Contact</a>
  </nav>

  <article style="background-color: white;">
    <h1>Tutorial Semantik Elemen untuk Pemula</h1>
    <p>Semantik elemen adalah elemen yang memiliki makna dan tujuan.
      Tujuannya agar kode HTML mudah dibaca dan tidak ada penyalahgunaan tag.
      Elemen semantik bagus untuk SEO dan juga dapat meningkatkan accessibility.
    </p>
  </article>

  <footer style="background-color: white;">
    Copyright &copy; 2020 by Petani Kode
  </footer>

</body>

</html>
```

Kita memberikan warna latar untuk elemen body dan juga beberapa elemen semantik.

Maka hasilnya:

![Contoh Style untuk Elemen Semantik](https://www.petanikode.com/img/html/semantik/contoh-style-semantik.webp)

## Mencoba Elemen Semantik Lainnya

Tidak semua elemen semantik bertujuan untuk membuat layout, ada juga beberapa elemen semantik lainnya yang bertujuan untuk membuat elemen tertentu.

Mari kita pelajari elemen semantik lainnya..

### Elemen `<detail>` dan `<summary>`

Tag `<detail>` dan `<summary>` merupakan tag untuk membuat elemen spoiler.

Tag `<detail>` akan berisi semua detail konten, lalu tag `<summary>` akan menjadi tombol yang bisa diklik untuk menampikan detail isinya.

![Elemen details di HTML](https://www.petanikode.com/img/html/semantik/details.png)

Contoh:

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Contoh Elemen Semantik</title>
</head>

<body>

  <article>
    <h1>Laptop Terbaik untuk Programmer</h1>

    <details>
      <summary>Lihat Spesifikasi</summary>
      Prosesor: Intel Core i9, RAM 32GB, SSD 1TB, HDD 4TB
    </details>
  </article>

</body>

</html>
```

Hasilnya:

### Elemen `<time>`

Tag `<time>` merupakan tag untuk membuat elemen waktu. Elemen waktu biasanya dibutuhkan untuk menampilkan waktu.

Misalnya:

Waktu saat sebuah postingan dibuat, waktu saat sebuah pesan dibaca, waktu keberangkatan, dan lain sebagainya.

Contoh:

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Contoh Elemen Semantik</title>
</head>

<body>

  <article>
    <h1>Waktu di HTML</h1>

    <p>
      Ditulis pada <time datetime="2020-20-07">20 July 2020</time>
    </p>
    <p>
      Hari ini saya ada acara dari pukul <time>08:00</time> sampai pukul
      <time>10:00</time>.
    </p>
  </article>

</body>
</html>
```

Hasilnya:

![Contoh elemen semantik time](https://www.petanikode.com/img/html/semantik/contoh-time.webp)

Elemen `<time>` akan ditampilkan apa adanya. Atribut `datetime` berfungsi untuk memberikan nilai tanggal dan waktu yang nantinya akan dibaca oleh program.

## Apa Selanjutnya?

Kita baru saja belajar tentang elemen semantik.

Intinya, kamu harus menggunakan elemen semantik agar kode HTML-nya mudah dibaca.

Nggak pakai elemen semantik, websitemu bisa dibilang masih kuno 😄.

Jadi pakailah elemen semantik.

Selanjutnya silakan pelajari tentang:
- [[13 Belajar HTML Cara Menambahkan Video pada Web]]