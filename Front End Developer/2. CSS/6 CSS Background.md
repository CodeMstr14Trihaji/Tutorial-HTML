---
obsidianUIMode: preview
sumber: WPU
level: medium
bahasa: CSS
tanggal_study: 2024-10-10T16:13:00
total_study: 1
tags:
  - CSS
id: WPUCSSD6
sr-due: 2024-10-12
sr-interval: 2
sr-ease: 150
---
# CSS Background
Pada tutorial kali ini yang akan kita bahas adalah mengenai bagaimana cara memberi style pada background dari sebuah elemen. Setiap elemen bisa kita beri background, namun di tutorial ini hanya pada body saja. 

Selain warna, kita juga dapat menambahkan gambar pada background dan pengatur pengulangan dari gambar serta posisinya. Setelah menyelesaikan tutorial ini, silahkan berkreasi dengan background pada halaman web kalian.. :)
## background-color
Berguna untuk mengatur warna pada background. Berikut contoh penggunaanya:

Kode HTML:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Background Color pada CSS</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Hello World</h1>

    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, vero? Voluptates error nobis eveniet similique placeat esse, maiores impedit non perferendis obcaecati earum. Assumenda iusto molestias repellat voluptas dicta nam.
    </p>
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum vel facere voluptatum odio numquam ipsum, placeat eius quod eligendi vero eos totam soluta facilis dolorem rerum fugiat doloribus debitis et?
    </p>
</body>
</html>
```

Kode CSS:

```css
body{
    background-color: lightblue;
}
```

Maka, background akan berwarna biru langit atau *lightblue* sebagai berikut:

![[6 CSS Background.png]]
## background-image
Berguna untuk mengatur gambar yang akan digunakan pada background. Disini kita akan menggunakan background berpola yang tersedia di https://www.subtleepatterns.com. Unduh salah satu gambar berpola, atau lebih. Lalu, kita rubah kode CSS diatas menjadi seperti berikut:

Gambar bckground:

![[bgleaves.png]]

Kode CSS:

```css
body{
    background-color: lightblue;
    background-image: url(bgleaves.png);
}
```

Disini, nama background kita adalah *bgleaves.png*. Kita tulis menggunakan url dan didalam tanda kurung. Maka, akan tampil hasil sebagai berikut:

![[6 CSS Background-1.png]]

## background-repeat
Mengatur jenis pengulangan gambar pada background.

Jika gambar yang digunakan sebagai background berukuran kecil, katanklah 300x300px, maka gambar akan dimunculkan dalam kondisi diulang-ulang sejajar, sepanjang sumbu x dan sumbu y. Jika seadainya kita hanya menggunakan pengulangan terhadap sumbu x, maka hasilnya adalah sebagai berikut:

Kode CSS:

```css
body{
    background-color: lightblue;
    background-image: url(bgleaves.png);
    background-repeat: repeat-x;
}
```

Hasilnya, gambar hanya akan di repeat sepanjang sumbu x, bukan, sumbu y:

![[6 CSS Background-2.png]]

Hal ini juga bisa dilakukan dengan posisi yang berbeda, yaitu sumbu y. Ganti saja menjadi seperti berikut, yaitu *repeat-x* menjadi *repeat-y*. 

> Warna biru berasal dari **background-color: light-blue** yang masih berjalan!

```css
body{
    background-color: lightblue;
    background-image: url(bgleaves.png);
    background-repeat: repeat-y;
}
```

Hasilnya:

![[6 CSS Background-3.png]]

---
### Ekstra
Sekarang, mari kita bermain dengan 2 gambar berikut:

--- start-multi-column: ExampleRegion1  
```column-settings  
number of columns: 2  
```

![[bgcolordown.png|500]]

--- end-column ---

![[bgcolor.png|500]]

--- end-multi-column
Kita akan menampilkan dua gambar berikut dengan memainkan gradasi, background warna putih, dan property image-repeat seperti sebelumnya. Perhatikan kode CSS:

Kode CSS:

```css
body{
    background-color: white;
    background-image: url(bgcolor.png);
    background-repeat: repeat-x;
}

p{
    color: blue;
}
```

Hasilnya:

![[6 CSS Background-4.png]]

Jika dengan menggunakan kode CSS dengan property repeat-y, maka kita harus menggunakan gambar background yang memiliki gradasi yang turun ke bawah. Yaitu gambar kedua. Berikut kode CSS nya:

```css
body{
    background-color: white;
    background-image: url(bgcolordown.png);
    background-repeat: repeat-y;
}

p{
    color: blue;
}
```

Maka hasilnya:

![[6 CSS Background-5.png]]
## background-position
Mengatur posisi gambar pada background. Jika kita mengisi nilai *background-repeat* dengan nilai *no-repeat*, maka kita bisa menggunakan property lain berupa *background-position*, berikut cara menggunakanya:

Kita siapkan gambar, disini disiapkan gambar dengan nama **owl.png**, dan akan kita tampilkan dengan dengan kode css berikut:

```css
body{
    background-color: white;
    background-image: url(owl.jpeg);
    background-repeat: no-repeat;
    background-position: top right;
}

p{
    color: blue;
}
```

Hasilnya adalah :

![[6 CSS Background-6.png]]

Kombinasi yang bisa digunakan dalam menggunakan property ini adalah sebagai berikut:

![[6 CSS Background-7.png|400]]

---
Semua cara penulisan CSS tadi, juga bisa ditulis dengan shorthand, atau metode yang lebih singkat, yaitu dengan susunan sebagai berikut:

```css
background: lightgreen url(bg.png) top left no-repeat
```



