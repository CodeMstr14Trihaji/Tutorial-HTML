---
obsidianUIMode: preview
sumber: WPU
level: pemula
bahasa: CSS
tanggal_study: 2024-10-10T05:51:00
total_study: 1
tags:
  - CSS
id: WPUCSSD5
sr-due: 2024-10-12
sr-interval: 2
sr-ease: 150
---
# Text Styling pada CSS
Setelah di tutorial sebelumnya kita mempelajari tentang bagaimana memberi style pada font, di kesempatan kali ini yang akan kita bahas adalah memberikan style pada text seperti pengaturan paragraf, pengaturan warna, dll.

## color
Color pada CSS berguna untuk memberikan warna pada tulisan. Pemberian warna pada CSS bisa menggunakan 3 cara seperti berikut:
- nama warna (*red, lightseagreen, royalblue, dll*)
- hexadecimal (*\#ff0000, \#20b2aa, \#4169e1*, dll)
- rgb (*rgb(255,0,0), rgb(32,178,170), rgb (65, 105,225), dll*)

Jika kita ingin menambahkan warna tertentu yang kita tidak tahu apa namanya, dan berapa nilai hexadecimalnya, kita bisa menggunakan bantuan situs web seperti [http://www.colorpicker.com](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa2lMemJWejdtUm9COFpnRXRaanlzWVZVcXRSZ3xBQ3Jtc0tubEI2b0VSeHFlTkRPcDZ6YkpNb0VXUDBUUTFDOWl6U3hfR1lVTW14VVNoaUVrU25NVDZKS0J6TXFNQ2xwaXlsd0pxVjZTS0ZJaG9wSzNWQ0pBcmxjNDRnaFdKd2RkcW5uREFJQjNMMjlSZ2NHTUZKQQ&q=http%3A%2F%2Fwww.colorpicker.com%2F&v=xih8giA7S3Q), atau yang sejenisnya.

Berikut contoh penggunaan color:

Kode HTML yang akana kita gunakan sepanjang tutorial ini sama, yaitu sebagai berikut:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Text Styling pada CSS</title>
        <meta charset="UTF-8">
        <link rel="stylesheet" href="style.css">
    </head>
    <body>

        <h1>Hello Dunia</h1>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque necessitatibus provident nobis officiis recusandae sunt, molestiae accusantium debitis deleniti, velit, aliquid minus nesciunt! Ullam velit, vitae expedita iure beatae magni.
        </p>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate recusandae laboriosam repellendus vitae, quae aliquid dolor fugit animi adipisci architecto facilis iure aliquam voluptas quis, beatae, quas doloremque nemo ratione!
        </p>

    </body>
</html>
```

Kode CSS:

```css
h1{
    font-size: 150px;
    color: skyblue;
}
```

Maka, hasilnya menjadi seperti berikut:

![[5 Text Styling.png]]

Jika kita mengganti cara pemberian warna dengan menggunakan metode hexadecimal, pun juga bisa dilakukan. Kini kita ganti warnanya menjadi warna merah, berikut kode CSS-nya:

```css
h1{
    font-size: 150px;
    color: #ff0000;
}
```

![[5 Text Styling-1.png]]

Untuk bisa mencari warna dengan nilai hexadecimal, juga bisa menggunakan bantuan situs web, ada banyak sekali situs web yang menyediakan jasa menyediakan nilai hexadecimal warna. Seperti https://www.color-hex.com/ .

Sedangkan untuk penyedia kode rgb untuk pemberian warna dengan metode rgb, bisa menggunakan situs https://www.rapidtables.com/web/color/RGB_Color.html
## text-align
Mengatur format paragraf / teks. Memiliki value seperti:
- **left** (teks rata kiri)
- **right** (teks rata kanan)
- **center** (teks rata tengah)
- **justify** (teks rata keseluruhan)

Jika kita menggunakan kode HTML yang sama, maka kita cukup tambah kode CSS menjadi seperti berikut:

```css
h1{
    font-size: 100px;
    color: #ff0000;
    text-align: right;
}

p {
    text-align: center;
}
```

Maka, isi tag h1 akan bergeser ke kanan (*text-align:right*), dan paragraf akan menjadi di tengah. Hasilnya seperti berikut:

![[5 Text Styling-2.png]]
## text-indent
Berguna untuk memberi indentasi pada paragraf / teks. Value yang bisa diberikan seperti **px** dan **%**.

Kode CSS:

```css
h1{
    font-size: 100px;
    color: #ff0000;
    text-align: right;
}

p {
    text-indent: 100px;
}
```

Maka, hasilnya akan terdapat indentasi sebanyak **100px** di kedua paragraf. Jika ada 100 paragraf sekalipun, maka semuanya pun akan terindentasi, karena selector yang digunakan adalah tag `<p>`.

![[5 Text Styling-3.png]]
## text-decoration
Berguna untuk mengatur dekorasi pada teks, value yang ada seperti:
- **none** (tidak ada dekorasi)
- **underline** (garis bawah)
- **overline** (garis diatas text)
- **line-through** (garis membelah tulisan ditengah / tercoret)

Berikut kode CSS-nya:

```css
h1{
    font-size: 100px;
    color: #ff0000;
    text-decoration: line-through;
}

p {
    text-indent: 100px;
    text-decoration: underline;
}
```

Untuk penggunaan value **none**, biasanya digunakan untuk menghapus tanda garis bawah pada link, jika kita menambahkan link. Dan hasil dari perubahan kode CSS diatas, hasilnya adalah sebagai berikut:

![[5 Text Styling-4.png]]
## text-transform
Mengubah jenis huruf menjadi huruf besar, kecil, atau kapital. Nilai value yang bisa diberikan diantaranya:
- **none** (tidak ada perubahan)
- **lowercase** (huruf kecil semua)
- **uppercase** (semua huruf kapital)
- **capitalize** (huruf awal kata berupa kapital)

Berikut contoh penggunaanya dengan kode CSS:

```css
h1{
    font-size: 100px;
    color: #ff0000;
    text-transform: uppercase;
}

p {
    text-indent: 100px;
    text-decoration: underline;
    text-transform: capitalize;
}
```

Maka akan dihasilkan output sebagai berikut:

![[5 Text Styling-5.png]]

h1 akan besar semua, dan paragraf akan diawali huruf besar untuk setiap katanya.
## letter-spacing
Mengatur spasi antar huruf, value yang bisa digunakan adalah **px**, **cap**, dan **normal**.

Contoh kode CSS:

```css
h1{
    font-size: 100px;
    color: #ff0000;
    text-transform: uppercase;
}

p {
    text-indent: 100px;
    text-transform: capitalize;
    letter-spacing: 5px;
}
```

Maka hasilnya, akan terdapat spasi antar huruf seperti berikut:

![[5 Text Styling-6.png]]
## word-spacing
Mengatur spasi antar kata, value yang bisa digunakan antara lain adalah **px**, dan **normal**. Berikut adalah contoh penggunaanya:

Kode CSS:

```css
h1{
    font-size: 100px;
    color: #ff0000;
    text-transform: uppercase;
}

p {
    text-indent: 100px;
    text-transform: capitalize;
    word-spacing: 20px;
}
```

Hasilnya, akan terdapat spasi antar kata pada tampilan paragraf.

![[5 Text Styling-7.png]]

---

> [!NOTE] Catatan Penting!
> Ada banyak sekali perubahan yang terjadi pada CSS, mengingat ini adalah tutorial 9 tahun lalu. Jadi, value yang bisa ditambahkan sebenarnya sangat banyak, namun konsepnya sama saja. Yaitu berbeda value, maka berbeda ukuran atau outputnya, jadi gunakan mana yang cocok sesuai penggunaan saja.
> 
> Jika anda menggunakan VS Code, instal saja exstension CSS, maka saat anda menuliskan kode CSS, tepatnya ketika mengetikan nilai value, semua value yang bisa dipakai akan muncul sebagai fitur **auto complete**, tinggal sesuaikan saja.




