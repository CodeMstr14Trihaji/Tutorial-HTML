---
obsidianUIMode: preview
sumber: petanikode
level: pemula
bahasa: HTML
tanggal_study: 2024-10-08T16:18:00
total_study: 1
tags:
  - HTML
id: PTHTML14
sr-due: 2024-10-10
sr-interval: 2
sr-ease: 150
---
# Belajar HTML #14: Cara Menambahkan Audio pada HTML

---

![Menambahkan Audio pada HTML](https://www.petanikode.com/img/cover/html-audio.png)

Sekali lagi..

Konten dalam web, tidak hanya dalam bentuk teks dan gambar saja. Tapi juga bisa dalam bentuk multimedia seperti audio dan video.

Pada tutorial ini, kita akan fokus membahas tentang audio di HTML.

Konten audio biasanya berbentuk _podcast_, _audiobook_, dan musik.

Lalu pertanyaannya:

Bagaimana cara menambahkan audio di HTML?

Mari kita bahas…

## Cara Menambahkan Audio di HTML

Sebelum adanya HTML 5, audio di HTML ditambahkan dengan program eksternal seperti flash player.

Namun, kini HTML sudah punya tag sendiri yakni `<audio>`.

Tag `<audio>` adalah tag untuk membuat audio player. Lalu kita bisa memberikan file audio yang akan diputar dengan tag `<source>`.

![Tag audio di HTML](https://www.petanikode.com/img/html-audio/tag-audio.png)

Contoh: 📄 `contoh-audio.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Contoh Audio di HTML</title>
</head>
<body>
  <h1>Contoh Audio di Web</h1>
  <audio controls>
    <source src="Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
  </audio>
</body>
</html>
```

> File audionya bisa kamu download di: 🎵 [Ngoni.mp3](https://github.com/petanikode/belajar-html/raw/master/audio/Ngoni.mp3) (6.2 MB)

Hasilnya:

![Contoh audio di HTML](https://www.petanikode.com/img/html-audio/contoh-audio.png)

Perhatikan!

Pada atribut `src`, kita menulis langsung nama file audio yang akan diputar. Ini karena kita menaruh file tersebut dalam satu folder yang sama dengan file HTML.

![File audio dan HTML](https://www.petanikode.com/img/html-audio/file-audio-html.png)

Jika file audio tersimpan di folder yang berbeda, maka harus ditulis alamat path menuju folder tersebut.

Misalkan, saya menaruhnya di dalam folder 📁 `audio`,

![File audio dan HTML](https://www.petanikode.com/img/html-audio/folder-audio.png)

maka atribut `src` bisa diisi seperti ini:

```html
<audio controls>
    <source src="audio/Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
</audio>
```

…dan juga file audionya tersimpan di website yang berbeda, maka kita harus mengisinya dengan alamat URL.

```html
<audio controls>
    <source src="https://github.com/petanikode/belajar-html/raw/master/audio/Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
</audio>
```

## Format File Audio yang didukung

Audio player di HTML tidak mendukung semua jenis format file audio. Berikut ini daftar format file audio yang bisa diputar di HTML. [1](https://www.petanikode.com/html-audio/#fn:1)

|Format|Container|MIME type|
|---|---|---|
|PCM|WAV|audio/wav|
|MP3|MP3|audio/mpeg|
|AAC|MP4|audio/mp4|
|AAC|AAC|audio/aac|
|AAC|AAC|audio/aacp|
|Vorbis|Ogg|audio/ogg|
|Vorbis|WebM|audio/webm|
|Opus|Ogg|audio/ogg|
|Opus|WebM|audio/webm|
|FLAC|FLAC|audio/flac|
|FLAC|Ogg|audio/ogg|

Format file yang biasanya digunakan adalah MP3 dan MP4 (M4A), karena ukuran filenya relatif kecil. Sementara format FLAC adalah format file audio dengan kualitas tinggi dan ukuran filenya relatif lebih besar.

## Atribut untuk Audio

Tag `<audio>` punya beberapa atribut yang sering digunakan:

### 1. `controls`

Atribut ini berfungsi untuk mengaktifkan tombol kontrol seperti tombol play, pause, stop, scroll, dan volume).

Contoh penggunaan:

```html
<audio controls="true">
    <source src="audio/Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
</audio>

<!-- atau -->

<audio controls>
    <source src="audio/Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
</audio>
```

Jika bernilai `true`, maka nilainya boleh tidak diisi. Nilai `true` artinya, kita akan mengaktifkan tombol kontrol dan jika nilainya `false` maka artinya tombol kontrol tidak diaktifkan.

### 2. `autoplay`

Atribut ini berfungsi untuk memutar audio secara otomatis. Nilai yang bisa diberikan pada atribut ini adalah `true` dan `false`.

Nilai `true` artinya kita akan memutar audio secara otomatis, dan `false` artinya audio tidak akan diputar secara otomatis.

Contoh:

```html
<audio autoplay="true">
    <source src="audio/Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
</audio>

<!-- atau -->

<audio autoplay>
    <source src="audio/Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
</audio>
```

> ✍️ **Catatan**: Atribut ini mungkin saja tidak akan bekerja pada Google Chrome, karena ada [perubahan policy](https://developers.google.com/web/updates/2017/09/autoplay-policy-changes) (kebijakan) dalam memutar audio secara otomatis.

### 3. `loop`

Atribut `loop` berfungsi untuk mengulang-ulang pemutaran audio. Ini seperti _repeat one_. Nilai yang bisa diberikan adalah `true` dan `false`.

Contoh:

```html
<audio loop="true">
    <source src="audio/Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
</audio>

<!-- atau -->

<audio loop>
    <source src="audio/Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
</audio>
```

### 4. `muted`

Atribut ini berfungsi untuk mensenyapkan audio. Nilai yang bisa diberikan adalah `true` dan `false`.

Contoh:

```html
<audio muted="true">
    <source src="audio/Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
</audio>

<!-- atau -->

<audio muted>
    <source src="audio/Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio, upgrade donk!
</audio>
```

## Audio Sebagai Background

Audio kadang sering digunakan sebagai background. Biasanya menggunakan musik.

Tujuan menambahkan background agar menambah kesan tertentu pada web. Misalkan, ingin membuat pengunjung merasa santai.. maka kita bisa memutar audio musik yang santai.

Cara membuat musk sebagai background adalah dengan menambahkan atribut `autoplay`, `loop`, dan menghilangkan kontrol (`hidden`).

Contoh:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Contoh audio sebagai background</title>
</head>
<body>
  <h1>Contoh audio sebagai background</h1>
  <audio hidden autoplay loop>
    <source src="Ngoni.mp3" type="audio/mpeg">
    Browsermu tidak mendukung tag audio
  </audio>
</body>
</html>
```

Hasilnya:

![File audio dan HTML](https://www.petanikode.com/img/html-audio/audio-bg.png)

Nggak ada suaranya?

Sekali lagi, atribut `autoplay` mungkin tidak bekerja di Google Chrome karena ada pembaharuan kebijakan dalam memutar audio.

Sekarang kita coba buka dengan Mozilla Firefox.

![File audio dan HTML](https://www.petanikode.com/img/html-audio/audio-bg-firefox.png)

Hasilnya sama saja, tidak ada suaranya.

Ini karena `autoplay` diblokir otomatis.

Sekarang kita coba ubah izin untuk memutar audio secara otomatis. Klik ikon autoplay pada address bar di dekat ikon `(i)`, sehingga muncul seperti ini:

![Autoplay di Firefox](https://www.petanikode.com/img/html-audio/autoplay-firefox.png)

Pada bagian _Autoplay_, ubah _Block Audio_ menjadi _Allow Audio and Video_.

Setelah itu, coba _refresh_ atau _reload_.

Maka suaranya akan terdengar.

![Autoplay di Firefox](https://www.petanikode.com/img/html-audio/ikon-audio.png)

## Apa Selanjutnya?

Sejauh ini kita sudah belajar banyak tag. Sudah saatnya untuk belajar membuat web kecil-kecilan dengan ilmu HTML yang kita pelajari.

Karena itu, selanjutnya kita akan belajar:
- [[15 Belajar HTML  Membuat Project Web Pribadi dengan HTML]]