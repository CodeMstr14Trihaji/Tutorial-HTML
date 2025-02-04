# Panduan dan Pengenalan HTML

HTML adalah bahasa markup standar untuk halaman Web. Dengan HTML Anda dapat membuat situs Web Anda sendiri. HTML mudah dipelajari - Anda akan menikmatinya!
## Apa itu HTML?
- HTML adalah singkatan dari Hypert Text Markup Language
- HTML adalah bahasa markup standar untuk membuat halaman Web
- HTML menggambarkan struktur halaman Web
- HTML terdiri dari serangkaian elemen
- Elemen HTML memberi tahu browser cara menampilkan konten
- Elemen HTML memberi label pada bagian konten seperti "Ini adalah judul", "Ini adalah paragraf",  "Ini adalah tautan", dan lain-lain.
## Dokumen HTML Sederhana
Contoh:

```html
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```
### Penjelasan
- Deklarasi ini `<!DOCTYPE html>`mendefinisikan bahwa dokumen ini adalah dokumen HTML 5
- Elemen `<html>`adalah elemen akar dari halaman HTML
- Elemen ini `<head>`berisi informasi meta tentang halaman HTML
- Elemen ini `<title>`menentukan judul untuk halaman HTML (yang ditampilkan di bilah judul browser atau di tab halaman)
- Elemen `<body>`mendefinisikan badan dokumen, dan merupakan wadah untuk semua konten yang terlihat, seperti judul, paragraf, gambar, hyperlink, tabel, daftar, dll.
- Elemen ini `<h1>`mendefinisikan judul besar
- Elemen `<p>`mendefinisikan sebuah paragraf
## Apa itu Elemen HTML?
Elemen HTML didefinisikan oleh tag awal, beberapa konten, dan tag akhir:

```html
< tagname > Konten ada di sini... < /tagname >
```
**Elemen** HTML adalah segalanya dari tag awal hingga tag akhir:
```html
< h1 > Judul Pertamaku < /h1 >

< p > Paragraf pertama saya. < /p >
```

Umumnya elemen di HTML memiliki pembuka dan penutup, tetapi ada beberapa elemen HTML yang tidak memiliki konten, seperti elemen `<br>`. Elemen-elemen ini disebut elemen kosong. Elemen kosong tidak memiliki tag penutup.
## Peramban Web
Tujuan peramban web (Chrome, Edge, Firefox, Safari) adalah untuk membaca dokumen HTML dan menampilkannya dengan benar.

Peramban tidak menampilkan tag HTML, tetapi menggunakannya untuk menentukan cara menampilkan dokumen:

![[Pasted image 20250204114526.png]]
## Struktur Halaman HTML
Berikut adalah visualisasi struktur halaman HTML:

![[Pasted image 20250204114622.png]]

> Note : Konten di dalam bagian `<body>` akan ditampilkan di browser. Konten di dalam elemen `<title>` akan ditampilkan di bilah judul browser atau di tab halaman.
## Sejarah HTML
Sejak awal mula World Wide Web, telah ada banyak versi HTML:

| Year | Version                                  |
|------|------------------------------------------|
| 1989 | Tim Berners-Lee invented www            |
| 1991 | Tim Berners-Lee invented HTML           |
| 1993 | Dave Raggett drafted HTML+              |
| 1995 | HTML Working Group defined HTML 2.0     |
| 1997 | W3C Recommendation: HTML 3.2           |
| 1999 | W3C Recommendation: HTML 4.01          |
| 2000 | W3C Recommendation: XHTML 1.0          |
| 2008 | WHATWG HTML5 First Public Draft        |
| 2012 | WHATWG HTML5 Living Standard           |
| 2014 | W3C Recommendation: HTML5              |
| 2016 | W3C Candidate Recommendation: HTML 5.1 |
| 2017 | W3C Recommendation: HTML5.1 2nd Edition |
| 2017 | W3C Recommendation: HTML5.2            |



