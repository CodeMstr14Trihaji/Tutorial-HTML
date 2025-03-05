---
obsidianUIMode: preview
sumber: WPU
level: pemula
bahasa: CSS
tanggal_study: 2024-10-12T21:34:00
total_study: 1
tags:
  - CSS
id: WPUCSSLOT7
sr-due: 2024-10-14
sr-interval: 2
sr-ease: 150
---
# Box Model CSS Reset
Topik yang akan kita bahas kali ini adalah **CSS reset**. Jadi, CSS reset adalah teknik yang dapat membuat kita mengatur ulang nilai-nilai default dari elemen-elemen yang ada di HTML, khususnya **margin** dan **padding**. 

Supaya lebih jelas, langsung saja ke contohnya, tulis kode HTML sebagai berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Latihan Box Model</title>
    <meta charset="utf-8"/>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div></div>
    <h1>Hello World</h1>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Magni, blanditiis! Temporibus eligendi id deserunt iusto, possimus fugit neque eum! Deserunt aut error voluptatibus ad pariatur quas sunt ex eius minima.</p>
</body>
</html>
```

Dengan kode CSS sebagai berikut:

```css
div {
    width: 200px;
    height: 200px;
    background-color: black;
}
```

Maka, akan dihasilkan tampilan seperti berikut:

![[6 Box Model CSS Reset-1.png|500]]

Tapi, jika kita perhatikan, kenapa disebelah kiri dan atas kotak hitam terdapat jarak? Padahal kita tidak memberi jarak? Jika kita rubah kode CSS menjadi seperti ini:

```css
div {
    width: 200px;
    height: 200px;
    background-color: black;
    margin: 0px;
}
```

Pun juga tidak mau berubah. Kenapa ini bisa terjadi?

Ini terjadi karena banyak elemen HTML yang secara default sudah memiliki **margin** dan **padding** sendiri. Contohnya disini adalah elemen **body** atau tag `<body>`, yang memiliki **margin** dan **padding** default. 

Jadi, solusinya adalah menghapus nilai **margin** pada elemen **body**, dengan kode CSS sebagai berikut:

```css
body {
    margin: 0px;
}

div {
    width: 200px;
    height: 200px;
    background-color: black;
    margin: 0px;
}
```

Maka, kotak hitam tersebut tidak akan memiliki jarak lagi, seperti ini, taaraaaaa:

![[6 Box Model CSS Reset-2.png|500]]

Dengan melakukan hal ini, artinya kita melakukan **reset** pada properti **margin** dari elemen HTML yang ada, dan nilai **margin** tersebut bukan hanya ada pada `<body>` saja, tetapi juga ada pada elemen lain, contohnya adalah `<h1>` - `<h6>`, dan juga elemen `<p>`.

Sehingga, ketika kita melakukan **reset** ini pada tag lain:

```css
body, h1, p{
    margin: 0px;
}

div {
    width: 200px;
    height: 200px;
    background-color: black;
    margin: 0px;
}
```

Maka, margin yang secara default dimiliki oleh elemen-elemen ini akah hilang:

![[6 Box Model CSS Reset-3.png|500]]

---
Baiklah, sekarang kita sampai pada satu pertanyaan. Kenapa kita perlu melakukan **reset**? 

Tujuanya adalah agar kita memiliki kendali penuh atas CSS yang kita buat. Namun, cara ini masih tergolong belum praktis, karena jika kita menulisnya seperti ini, maka kita hanya mengubah elemen yang kita miliki saja, bagaimana jika elemennya bertambah? Tentu menjadi kurang praktis.

Ada beberapa cara untuk melakukan reset ini, yaitu adalah dengan menggunakan **selector universal**, yaitu tanda bintang atau *asterisk* (\*). 

Menjadi seperti ini:

```css
* {
    margin: 0px;
}

div {
    width: 200px;
    height: 200px;
    background-color: black;
    margin: 0px;
}
```

Namun, ada yang bilang bahwa melakukan **reset** menggunakan **selector universal**  bukanlah cara  yang baik. Karena selector ini memberikan style ke semua elemen HTML, meskipun elemen itu tidak kita gunakan dalam project kita, sehingga membuat program lebih berat untuk berjalan.

Sehingga, ada cara **reset** yang lebih efektif lagi, yaitu cara yang ditemukan oleh ***Meyer Web***. Untuk bisa menggunakanya, kita bisa ketikan "CSS reset" pada searchbar, maka akan muncul situs yang bernama **meyerweb**. Klik saja.

Atau, bisa langsung klik link ini: https://meyerweb.com/eric/tools/css/reset/

Disitus ini, disediakan syntax CSS yang berguna untuk mereset elemen HTML dengan cara yang lebih efektif. Berikut syntax yang terdapat didalamnya yang tersedia untuk kita copy, dan tidak perlu kita ubah-ubah lagi:

```css
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}
```

Pastekan pada halaman CSS kita jika kita ingin menggunakanya, dan tuliskan syntax CSS kita dibawah copy paste syntax diatas untuk mereset elemen HTML kita

---
Sekian dari saya, semoga mudah dipahami 👍