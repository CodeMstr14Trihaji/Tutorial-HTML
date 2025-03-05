---
obsidianUIMode: preview
sumber: WPU
level: medium
bahasa: CSS
tanggal_study: 2024-10-11T14:29:00
total_study: 1
tags:
  - CSS
id: WPUCSSD10
sr-due: 2024-10-12
sr-interval: 1
sr-ease: 130
---
# Specificity dalam CSS
Specificity memiliki pengertian, bahwa setiap deklarasi CSS (selector) memiliki berat yang berbeda-beda. Berat tersebut menentukan seberapa spesifik sebuah elemen dapat dipilih oleh selector.  (W3school source)

Hal ini sudah pernah kita bahas dibagian sebelumnya, tapi mari kita perdalam lagi dikesempatan kali ini.
## Kasus Pertama
Perhatikan kode HTML berikut:

```html
  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis earum a dignissimos sed aliquam! Quia, sed perferendis corporis quidem deleniti, ex delectus quo iusto impedit animi blanditiis, quasi praesentium cumque.</p>
```

Jika kita memberinya kode CSS seperti ini: 

```css
p { color: red;}

p { color: green;}
```

Maka paragraf yang dimunculkan akan menjadi berwarna hijau:

![[10 Specificity-1.png]]

Hal ini dikarenakan, terjadi override, yaitu setelah selector pertama memberi warna elemen `<p>` dengan warna *merah*, selector kedua akan menimpanya lagi dengan warna *hijau*. Selain itu, jika kita menggunakan `p` sebagai selector, maka style selector yang berlaku hanyalah selector yang terakhir, tidak peduli berapa banyak selector `p` yang memberi warna berbeda, pasti selector terakhirlah yang akan menimpa semua itu.
## Kasus Kedua
Sekarang, mari kita rubah kode HTML kita menjadi seperti ini:

```html
  <p id="p1" >Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis earum a dignissimos sed aliquam! Quia, sed perferendis corporis quidem deleniti, ex delectus quo iusto impedit animi blanditiis, quasi praesentium cumque.</p>
```

Lalu, kita coba kode CSS berikut:

```css
#p1 { color: red;}

p { color: green;}
```

Maka hasilnya akan berbeda seperti sebelumnya, yaitu:

![[10 Specificity-2.png]]

Kenapa selector kedua tidak menimpa selector pertama, seperti kasus pertama? Ini terjadi karena **#p1 lebih spesifik dari p**. Bagaimana cara kerjanya? Mari kita pelajari cara penghitungan **specificity** berikut.
### Cara kerja 

![[10 Specificity-3.png]]

Gunakan rumus diatas, untuk menentukan specificity dari sebuah selector, dimana jika ada element, maka kita tambahkan satu(1) pada elemen. Jika ada class, maka kita tambahkan satu(1) pada class, dan seterusnya sampai inline. Khusus untuk inline, akan kita bahas dipembahasan tersendiri, karena kita baru belajar sampai *elemen*, *class*,dan *id* saja.

Perhatikan perhitungan berikut:

| Selector | inline | id  | class | element |
| -------- |:------:|:---:|:-----:|:-------:|
| \#p1     |   0    |  1  |   0   |    0    |
| p        |   0    |  0  |   0   |    1    |
100 vs 1, maka 100 yang menang, sehingga jelas, \#p1 lebih besar nilai specificitynya, sehingga \#p1 akan dimunculkan.
## Kasus ketiga
Baiklah, coba perhatikan kode HTML ini:

```html
<ul id="sarapan">
	<li class="favorit">Nasi Goreng</li>
	<li>Mie Goreng<li>
	<li>bubur Ayam</li>
	<li>Nasi Kuning</li>
</ul>
```

Lalu beri kode CSS:

```css
ul#sarapan li {
	color: green;
}

.favorit{
color: red;
}
```

Apakah anda bisa menebak, kira-kira apa hasiilnya? 

Hasilnya adalah berwarna hijau semua, seperti ini:

![[10 Specificity-4.png]]

Kenapa bisa berwarna hijau semua, sekarang mari kita cari tahu dengan cara menghitung nilai specificitynya, seperti yang sebelumnya kita lakukan:

| Selector       | inline | id  | class | element |
| -------------- | :----: | :-: | :---: | :-----: |
| ul\#sarapan li |   0    |  1  |   0   |    2    |
| .favorit       |   0    |  0  |   1   |    0    |
102 vs 10, tentu menang yang 102, yaitu selector pertama yang memberi nilai hijau, karena lebih spesifik daripada class *.favorit*. Sehingga warna hijau pada tekslah yang ditampilkan.

Lalu bagaimana jika kita ingin tetap menampilkan teks nasi goreng dengan warna merah? Caranya adalah dengan membuat elemen tersebut lebih spesifik lagi. Bagaimana caranya agar suatu elemen lebih spesifik lagi? Berikut caranya:
- Buat elemen yang diinginkan agar menjadi lebih spesifik.
- Tambahkan beban pada elemen tersebut agar semakin berat.

Baiklah, sekarang kita akan mengubah selector *.favorit* menjadi seperti ini:
- **ul#sarapan li.favorit**

```css
ul#sarapan li {
	color: green;
}

ul#sarapan li.favorit{
color: red;
}
```

Perhitunganya akan menjadi seperti ini:

| Selector               | inline | id  | class | element |
| ---------------------- | :----: | :-: | :---: | :-----: |
| ul\#sarapan li         |   0    |  1  |   0   |    2    |
| ul\#sarapan li.favorit |   0    |  1  |   1   |    2    |
Mana lebih besar antara 102 vs 112? Tentu 112, sehingga tampilan pada browser akan berubah, mau untuk berwarna merah menjadi seperti ini:

![[10 Specificity-5.png]]

> Kita juga bisa menggunakan bantuan website untuk melakukan penghitungan ini, salah satunya adalah http://specificity.keegan.st

Sekian, terima kasih.