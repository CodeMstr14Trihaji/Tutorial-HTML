---
obsidianUIMode: preview
sumber: WPU
level: pemula
bahasa: CSS
tanggal_study: 2024-10-09T19:12:00
total_study: 1
tags:
  - CSS
id: WPUCSSD3
sr-due: 2024-10-11
sr-interval: 2
sr-ease: 150
---
# Penempatan CSS
CSS berguna untuk memberi style pada file HTML, benar bukan? Pertanyaanya sekarang adalah, dimana file CSS ditempatkan pada HTML? Apakah didalam file yang sama dengan HTML bisa? Atau malah harus terpisah dengan file HTML? Mari kita cari tahu.

Jadi, penggunaan CSS bisa dilakukan dengan 3 cara, yaitu:
### 1. embed
Yaitu ditempatkan didalam tag `<style>...</style>` yang berada di tag `<head>`
### 2. inline
yaitu menambahkan langsung style pada atribut yang ingin diberi style. Sebagai contoh, jika ingin merubah paragraf padda HTML menjadi berwarna biru, maka bisa menggunakan cara berikut:

```html
<p style="color: lightblue;"> ... </p>
```
### 3. external
yaitu dengan membuat file CSS yang terpisah dengan file HTML. Supaya file HTML dan file CSS saling terkait, maka di file HTML, kita perlu memanggil file CSS dengan menggunakan tag `<link>`, dan menambahkan atribut **rel** dan **href**. Contohnya sebagai berikut:

```html
<link rel="stylesheet" href="style.css">
```

---
Baiklah, saatnya mencoba cara diatas, satu persatu.

# Embed
Berikut adalah contoh menggunakan CSS dengan sistem embed:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba CSS</title>
    <meta charset="utf-8"/>
    <style>
        body {font-family:arial ;}
        h1 {color: lightblue;}
        p {
            line-height: 1.6em;
            color: grey;
        }
    </style>
</head>
<body>

    <h1>Hello world</h1>

    <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
        Numquam beatae, quisquam voluptatibus culpa facere 
        exercitationem ipsum assumenda debitis velit aliquid quam 
        quibusdam quas dolor laborum odit ducimus deserunt odio suscipit?
    </p>

</body>
</html>
```

Penggunaan tag `<style>` biasanya digunakan didalam tag `<head>`, dan dibawah tag `<title>`.
# Inline
Berikut adalah contoh penggunaan inline dalam penempatan CSS:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Coba CSS</title>
    <meta charset="utf-8"/>
</head>
<body>

    <h1 style="text-align: center; font-size: 60px">Hello world</h1>

    <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
        Numquam beatae, quisquam voluptatibus culpa facere 
        exercitationem ipsum assumenda debitis velit aliquid quam 
        quibusdam quas dolor laborum odit ducimus deserunt odio suscipit?
    </p>

</body>
</html>
```

Gunakan atribut `<style>` pada tag yang ingin kita beri style CSS. Namun, cara ini tentu tidak dianjurkan, karena seperti alasan pertama yang sudah dijelaskan.
# External
Penempatan CSS dengan menggunakan sistem External, maksudnya adalah memisahkan file CSS dari file HTML.

![[CSS external.png]]

Berikut contoh penggunaanya:

Kode HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>External CSS</title>
    <link rel="stylesheet" href="style.css"> 
    <!-- tag link berguna untuk mengaitkan file HTML dan CSS yang dituju -->

</head>
<body>
    <h1>Hello World</h1>
    <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. 
        Quam aliquam id voluptatum possimus quos praesentium 
        corporis quod doloremque cumque deserunt, illo tempore nulla. 
        Repudiandae natus temporibus magnam! Ea, distinctio aut!
    </p>
</body>
</html>
```

Kode CSS:

```css
h1 {
    color: blue;
    font-family: arial;
    font-size: 100px;
}
```

File dibuat terpisah, dan dikaitkan dengan bantuan tag `<link>` yang dituliskan di file HTML.