---
obsidianUIMode: preview
sumber: WPU
level: pemula
bahasa: CSS
tanggal_study: 2024-10-09T17:46:00
total_study: 1
tags:
  - CSS
id: WPUCSSD1
sr-due: 2024-10-11
sr-interval: 2
sr-ease: 150
---
CSS atau Cascading Style Sheet, adalah mekanisme sederhana yang mengatur gaya / style (contoh: warna, posisi, ukuran, font, dll) pada halaman web.

Tanpa CSS, tampilan semua web hanya akan seperti tampilan hasil kode HTML saja. 
## Sebelum ada CSS
Sebelum adanya CSS, sebuah halaman dihias dengan menambahkan banyak atribut pada tag HTML. Semisal kita ingin membuat tampilan seperti dibawah ini, tanpa CSS, yaitu dengan menggunakan HTML saja, maka kita harus menuliskan kode seperti dibawah ini:

![[Hello world.png]]

```html
<font size="+6" color="ligthblue" face="arial">
	<center>
		<h1>Hello World</h1>
	</center>
</font>
```

Bisa dilihat dikode diatas, bahwa untuk memberi style pada satu tag HTML, membutuhkan banyak sekali atribut tambahan. Hal ini tentu tidak menjadi masalah ketika kita hanya menambahkan satu atau beberapa style pada header h1. Tapi bayangkan jika kita harus memberi banyak style pada banyak tag lain, tag h1, dan banyak tag h2, tentu ini sangat tidak efisien, dan memakan terlalu banyak waktu.
## Setelah ada CSS
 Tapi, ketika kita menggunakan CSS, untuk menampilkan style yang sama dengan gambar diatas, kita hanya perlu mengetikan kode yang lebih singkat dan rapi. Penulisan kode HTML dan kode CSS pun bisa dilakukan di file yang berbeda, sehingga tidak menumpuk di satu file:
 
 Kode HTML:
```html
<h1>Hello World</h1>
```

Kode CSS:
```css
h1 {
	font-size: 120px;
	font-family: arial;
	color: lightblue;
	text-align: center;
}
```

Bisa dilihat perbedaanya bukan? Penulisan dengan menggunakan kode CSS, jauh lebih rapi, dan lebih singkat. Selain itu, ada banyak keunggulan lain, yang akan dijelaskan di penjelasan selanjutnya.

# Teori CSS
Berikut ini teori tentang CSS:
- Aturan yang digunakan untuk menampilkan elemen / tag HTML
- Dibuat terpisah dengan HTML
- Bertujuan untuk memisahkan konten dengan style
- 1 file CSS dapat digunakan untuk banyak halaman HTML
- 1 halaman HTML dapat terlihat berbeda jika menggunakan CSS yang berbeda pula. Untuk melihat praktek ini, bisa mengunjungi www.csszengarden.com