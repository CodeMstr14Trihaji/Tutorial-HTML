---
obsidianUIMode: preview
sumber: petanikode
level: pemula
bahasa: HTML
tanggal_study: 2024-10-09T16:21:00
total_study: 2
tags:
  - HTML
id: PTHTML5
sr-due: 2024-10-12
sr-interval: 3
sr-ease: 170
---
# Belajar HTML #05: Cara Membuat Komentar di HTML

---

![Html Komentar](https://www.petanikode.com/img/html/html.png)

Sampai ditahap ini.. apakah kamu sudah ingat semua tag HTML yang dipelajari?

Sudah lupa?

Tidak apa-apa, itu adalah sifat dari manusia. Otak kita memang tidak seperti komputer yang bisa mengingat dengan cepat dan permanen.

Karena itu, kita membutuhkan catatan agar bisa mengingat.

Coba perhatikan ini:

![Komentar pada libre office](https://www.petanikode.com/img/html/komentar/komentar-office.png)

Yang saya lingkari merah itu adalah komentar atau catatan yang akan mengingatkan saya tentang pekerjaan yang harus dilakukan di bagian tersebut.

Karena tulisan saya sangat panjang, jadi komentar ini sangatlah berguna.

Nah, di HTML juga kita akan menemukan hal yang demikian. Nantinya, dokumen HTML kita akan semakin banyak dan panjang.

Agar bisa mengingat strukturnya, sebaiknya ditambahkan komentar.

Bagaimana cara membuatnya?

Mari kita pelajari..

## Apa itu Komentar dalam HTML?

Komentar adalah elemen yang akan diabaikan oleh browser. Ia tidak akan ditampilkan di dalam web.

Komentar biasanya digunakan untuk memberikan informasi tambahan pada kode HTML dan kadang juga digunakan untuk menon-aktifkan beberapa kode HTML.

## Cara Membuat Komentar di HTML

Komentar dapat kita buat dengan tag `<!-- -->`.

![Cara Membuat Komentar di HTML](https://www.petanikode.com/img/html/komentar/komentar.png)

Contoh:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Belajar Membuat Komentar di HTML</title>
    </head>
    <body>
      <!-- ini adalah komentar -->
      <p>Hello World!</p>
      <!-- ini juga komentar
      dan ditulis dalam dua baris -->
    </body>
</html>
```

Hasilnya:

![Contoh hasil komentar](https://www.petanikode.com/img/html/komentar/contoh-hasil-komentar.webp)

Komentar tidak akan ditampilkan oleh browser, tapi kita bisa melihatnya dengan cara view source.

Klik kanan pada browser, lalu pilih **view page source**.

![View source browser](https://www.petanikode.com/img/html/komentar/view-source.webp)

## Jalan Pintas untuk Membuat Komentar

Jika kamu menggunakan teks editor [Visual Studio Code](https://www.petanikode.com/text-editor-vscode), kamu bisa membuat komentar dengan menekan `Ctrl`+`/`.

![Komentar dengan VS Code](https://www.petanikode.com/img/html/komentar/komentar-vscode.gif)

Cara ini lebih cepat dibandingkan dengan harus menulis secara manual tag komentarnya.

## Atribut untuk Komentar

Komentar tidak bisa ditambahkan atribut. Jika kamu mencoba menambahkannya, itu akan sia-sia. Soalnya komentar merupakan elemen yang tidak akan diproses oleh browser.

## Fungsi Komentar

Komentar memang tidak akan ditampilkan di web, namun bukan berarti ia tidak memiliki fungsi.

Berikut ini beberapa fungsi komentar:

### 1. Komentar untuk Menjelaskan Arti Tag

Saat belajar HTML, kamu mungkin akan kesulitan mengingat fungsi dan arti dari tag HTML. Karena itu, kamu harus membuat catatan untuk mengingatnya.

Ini bisa kamu lakukan dengan mencatat di buku, maupun media lain. Tapi, alangkah baiknya memanfaatkan komentar untuk mencatat.

Contoh:

```html
<!DOCTYPE html> <!-- ini tag untuk menentukan type dokumen -->
<html lang="en">
    <head>
      <title>Belajar Membuat Komentar di HTML</title>
        <!-- tag title berfungsi untuk membuat judul web dan akan ditampilkan
        pada title bar di browser -->
    </head>
    <body>
      <p>Ini tag paragraf yang aktif</p>
      <!-- 
        tag <p> adalah tag untuk membuat paragraf 
      -->
    </body>
</html>
```

Jika kita lupa, kita bisa membuka kembali dan mempelajari kode tersebut.

Tapi ingat, jangan buat komentar seperti ini pada proyek websitemu. Karena akan sangat mengganggu dan membuat kode sulit terbaca.

Sebaiknya, komentar yang berisi penjelasan semacam ini dibuat pada kode HTML yang kita pakai untuk belajar. Bukan kode HTML untuk web asli.

### 2. Komentar untuk Menyimpan Todo List

Komentar kadang sering digunakan juga untuk menyimpan todo list, ini akan membantu kita mengingat apa yang harus dikerjakan pada bagian HTML tertentu.

Contoh:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Belajar Membuat Komentar di HTML</title>

        <!-- TODO: Tambahkan tag meta di sini -->
    </head>
    <body>
      <h1>Komentar di HTML</h1>

      <!-- TODO: Buat konten web di ini -->
    </body>
</html>
```

Jika kita sudah mengerjakan apa yang dituliskan di todo list tersebut, kita bisa hapus komentarnya.

### 3. Komentar untuk Menonaktifkan Kode HTML

Komentar kadang sering digunakan untuk menon-aktifkan kode HTML.

Contoh:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Belajar Membuat Komentar di HTML</title>
    </head>
    <body>
      <p>Ini tag paragraf yang aktif</p>
      <!-- 
        <p>ini tag paragraf yang tidak aktif
        karena berada di dalam komentar
        </p> 
      -->
      <p>ini paragraf yang lainnya</p>
    </body>
</html>
```

Hasilnya:

![Disable kode dengan komentar](https://www.petanikode.com/img/html/komentar/disable-code.webp)

## Apa Selanjutnya?

Itulah cara membuat komentar di HTML, intinya kamu hanya perlu mengingat tag untuk membuatnya.

Selanjutnya silakan pelajar tentang:

- [[6 Belajar HTML Text Formatting di HTML (Bold, Italic, Underline, dll)]]