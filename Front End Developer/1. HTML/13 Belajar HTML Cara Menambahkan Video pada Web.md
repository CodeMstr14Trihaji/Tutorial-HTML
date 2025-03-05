---
obsidianUIMode: preview
sumber: petanikode
level: medium
bahasa: HTML
tanggal_study: 2024-10-08T15:53:00
total_study: 1
tags:
  - HTML
id: PTHTML13
sr-due: 2024-10-10
sr-interval: 2
sr-ease: 150
---
# Belajar HTML #13: Cara Menambahkan Video pada Web

---

![Cara Menambahkan Video pada Web](https://www.petanikode.com/img/cover/html-video.png)

Pada tutorial sebelumnya, kita sudah belajar cara [menambahkan gambar di HTML](https://www.petanikode.com/html-img/). Namun, ini belumlah cukup.. karena sekarang konten di web tidak hanya dalam bentuk teks dan gambar saja.

Konten lainnya yang bisa ditambahkan di HTML adalah audio dan juga video.

Nah, pada tutorial ini.. kita akan belajar cara menambahkan video di HTML.

Mari kita mulai…

## Cara Menambahkan Video di HTML

Kita membutuhkan sebuah media player untuk menampilkan video di HTML.

Dulu..

Sebelum ada HTML 5, media player di HTML dibuat dengan program eksternal seperti adobe flash.

Namun, kini sudah tidak dipakai lagi.

![Comic Adobe Flash dan HTML 5](https://www.petanikode.com/img/html-video/flash-html.jpg)

HTML sekarang punya tag baru untuk membuat media player, yakni tag `<video>`.

![Format dasar tag Video](https://www.petanikode.com/img/html-video/tag-video.png)

Jika tag video di buka pada browser yang tidak mendukungnya, maka teks `browser tidak mendukung tag video` akan ditampilkan.

Tapi, kalau mendukung.. videonya yang akan ditampilkan.

Contoh:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Contoh Video di HTML</title>
</head>
<body>
  <h1>Contoh Video di HTML</h1>
  <video controls>
    <source src="cat-herd.webm" type="video/webm" />
    Browsermu tidak mendukung tag ini, upgrade donk!
  </video>
</body>
</html>
```

> File videonya kamu bisa download di: 🎞 [cat-herd.webm](https://www.petanikode.com/img/html-video/cat-herd.webm)

Hasilnya:

Live Demo

Pada contoh di atas, kita menuliskan secara langsung nama video yang akan ditampilkan. Ini karena videonya berada dalam satu folder dengan file HTML.

![File video dan HTML](https://www.petanikode.com/img/html-video/file-video.png)

Jika video tersebut tersimpan di folder yang berbeda, maka perlu ditulis alamat folder atau path-nya.

Misalkan, saya meneruh videonya di dalam folder `video`. Maka, alamat path yang digunakan adalah:

```html
<video>
<source src="video/nama-video.mp4">
</video>
```

..dan jika videonya berada di website yang berbeda, maka kita harus mengisi atribut `src` dengan URL lengkap dari video.

```html
<video>
<source src="https://www.petanikode.com/img/html-video/cat-herd.webm">
</video>
```

## Format Video yang Didukung

Tidak semua format video dapat ditampilkan di HTML. Berikut ini beberapa format video yang didukung: [1](https://www.petanikode.com/html-video/#fn:1)

|Format FILE|Media Type|
|---|---|
|MP4|video/mp4|
|WebM|video/webm|
|Ogg|video/ogg|

Jika kamu punya video dengan format yang berbeda dari ketiga format tersebut, maka kamu harus mengubahnya agar bisa ditambahkan ke HTML.

## Atribut untuk Video

Tag `<video>` punya beberapa atribut yang bisa diberikan:

|Nama Atribut|Nilai|Fungsi|
|---|---|---|
|`autoplay`|`true`/`false`|Agar video diputar otomatis|
|`controls`|`true`/`false`|Untuk mengaktifkan control video player|
|`loop`|`true`/`false`|Untuk memutar video terus menerus|
|`muted`|`true`/`false`|Untuk menonaktifkan audio|
|`poster`|Image Path|Untuk menentukan gambar cover dari video|
|`width` & `height`|angka|Untuk menentukan tinggi dan lebar video|
|`playsinline`|`true`/`false`|Untuk memutar video secara ‘inline’|

Jika atribut bernilai `true`, maka ia boleh ditulis namanya saja.

Contoh:

```html
<video loop="true">
<source src="video.mp4" />
</video>
```

Bisa disingkat menjadi:

```html
<video loop>
<source src="video.mp4" />
</video>
```

Jika nilai atribut bernilai `false`, maka atribut tersebut boleh tidak ditulis atau juga boleh ditulis.

Contoh:

```html
<video loop="false">
<source src="video.mp4" />
</video>

<!-- boleh juga seperti ini: -->
<video>
<source src="video.mp4" />
</video>
```

Nah, untuk atribut lainnya, kamu bisa cek di [MDN: The Video Embed element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video#Attributes).

## Video Sebagai Gambar Animasi Gif

Banyak website modern saat ini menggunakan video sebagai ganti dari animasi gif. Bahkan juga Google menyarankan untuk menggunakan video daripada gif.[2](https://www.petanikode.com/html-video/#fn:2)

Mengapa?

Karena ukuran file dari video jauh lebih kecil dibandingkan dengan gif dan juga tentunya akan mempengaruhi kecepatan download.

Nggak percaya?

Mari kita bandingkan:

![gif-vs-video](https://www.petanikode.com/img/html-video/gif-vs-video.png)

File [cat-herd.gif](https://gif-to-video.glitch.me/img/cat-herd.gif) punya ukuran `3,6 MB` setelah saya covert formatnya menjadi MP4 dan Webm, ukurannya menjadi sangat kecil.

Terbukti kan, file video lebih kecil daripada gif.

Lalu, bagaimana cara membuat video menjadi gambar gif di HTML.

Caranya sama seperti menambahkan video biasa, tapi kita harus mengaktifkan beberapa atribut seperti `autoplay`, `muted`, `playsinline` dan `loop`.

Contoh:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Contoh Video di HTML</title>
</head>
<body>
  <h1>Contoh Video sebagai gif</h1>
  <video autoplay loop muted playsinline>
    <source src="cat-herd.webm" type="video/webm" />
    <source src="cat-herd.mp4" type="video/mp4" />
  </video>  
</body>
</html>
```

Hasilnya:

Live Demo

## Subtitle untuk Video

Subtitle adalah teks yang akan ditampilkan dalam video. Biasanya digunakan untuk terjemahan atau alih bahasa dari video dan juga untuk membantu tuna rungu (orang tuli) untuk menyerap informasi pada video.

Subtitle pada HTML dapat kita tambahkan dengan tag `<track>`. Tag ini memiliki atribut `src` yang akan digunakan untuk menambahkan file subtitle.

![Kode Subtitle di HTML](https://www.petanikode.com/img/html-video/tag-track.png)

Format file subtitle untuk video di dalam HTML adalah WebVTT (`.vtt`) atau _Web Video Text Track_. File `.vtt` ini bisa dibuat dengan teks editor.

Jika kamu punya subtitle dengan format SubRip Text (`.srt`), kamu bisa mengubahnya menjadi `.vtt` di [srt2vtt](https://atelier.u-sub.net/srt2vtt/).

Sekarang mari kita coba contohnya: `video-subtitle.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Contoh Video di HTML</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</head>
<body>
  <h1>Video Subtitle</h1>
  <video controls>
    <source src="cat-herd.webm" type="video/webm"/>
    <source src="cat-herd.mp4" type="video/mp4"/>
    <track src="cat-herd-id.vtt" kind="subtitles" srclang="id" label="Indonesia"/>
  </video>  
</body>
</html>
```

Dan berikut ini isi file: `cat-herd-id.vtt`

```txt
WEBVTT

0
00:00:00.000 --> 00:00:03.000
Para penunggang kuda.

1
00:00:04.000 --> 00:00:08.000
Kucing berlari.
```

Hasilnya:

Catatan penting:

Subtitle tidak akan ditampilkan jika kita membuka file HTML secara langsung dari browser.

Coba perhatikan di bagian _address bar_, jika di sana ada tulisan **File**.. berarti kita membuka file HTML secara langsung.

![Membuka file html secara langsung](https://www.petanikode.com/img/html-video/file-html-direct.png)

Namun, jika di _address bar_ ada HTTP atau HTTPS.. itu artinya kita membuka file HTML melalui web server.

..dan juga jika format file `.vtt` tidak benar, subtile tidak akan ditampilkan.

Pastikan formatnya valid, silakan gunakan [Live WebVTT Validator](https://quuz.org/webvtt/) untuk pengecekan.

## Menmabahkan Video dari Youtube

Saat tidak ingin repot-repot mengubah format video, kita bisa manfaatkan Youtube.

Tinggal upload saja videonya ke Youtube. Nanti kita akan dapat id unik dari video. Id unik ini bisa kita dapatkan dari URL video.

Contoh: `N7iY-jNWeFc`

Youtube sendiri sudah punya media player, jadi kita tidak perlu membuatnya dengan tag `<video>`.

Tag yang kita butuhkan untuk menambahkan video dari Youtube adalah `<iframe>`. Tag ini sebenarnya berfungsi untuk menambahkan halaman lain dalam sebuah _frame_.

Contoh:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Contoh Video di HTML</title>
</head>
<body>
  <h1>Video dari Youtube</h1>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/N7iY-jNWeFc"></iframe>
</body>
</html>
```

Perhatikan URL yang digunakan pada atribut `src`, di sana kita menggunakan `/embed/`. Ini adalah halaman yang digunakan khusus untuk _embed_ video dari Youtube.

Hasilnya:

![Contoh video dari Youtube](https://www.petanikode.com/img/html-video/contoh-video-youtube.webp)

Sebenarnya ada cara gampangnya..

Pada video Youtube yang ingin kita _embed_, klik saja tombol _share_.

![Tombol share di Youtube](https://www.petanikode.com/img/html-video/btn-share.png)

Maka akan muncul opsi untuk share video, pilih saja _embed_..

![Tombol embed di Youtube](https://www.petanikode.com/img/html-video/embed.png)

..dan kita akan mendapatkan kode HTML untuk _embed_ videonya.

Kode ini bisa kita _copy_ ke file HTML.

## Apa Selanjutnya?

Kita sudah belajar cara menampilkan video. Baik itu video dari file lokal dan juga video dari Youtube.

Nah, berikutnya silakan pelajari tentang:
- [[14 Belajar HTML Cara Menambahkan Audio pada HTML]]