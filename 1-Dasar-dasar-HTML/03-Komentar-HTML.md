# Komentar HTML
**Komentar HTML** adalah teks dalam dokumen HTML yang tidak ditampilkan oleh browser. Komentar ini memungkinkan Anda untuk meninggalkan catatan dan penjelasan langsung dalam kode, yang dapat sangat membantu selama proses pengembangan atau saat Anda perlu melakukan pembaruan di masa mendatang.

> Untuk menambahkan komentar di kode HTML Anda, Anda melampirkan teks yang ingin Anda sembunyikan dari tampilan di dalam `<!--`  dan `-->`

## Contoh Komentar HTML
```html
<!-- Ini adalah komentar pada HTML, tidak ditampilkan di peramban web -->
<p>Ini adlah teks yang terlihat</p> 
```
Dalam contoh ini:
- Teks dalam tag `<!--` dan `-->` tidak akan muncul di halaman web
- Komentar ini dapat mencakup pengingat, peringatan, atau penjelasan tentang kode, yang dapat berguna bagi siapa saja yang membaca atau mengedit dokumen HTML.
## Berbagai Cara Menambahkan Komentar di HTML
Ada dua cara utama untuk menulis komentar dalam HTML: komentar satu baris dan komentar multi-baris. Keduanya menggunakan sintaks dasar yang sama tetapi berbeda dalam cara penerapannya.

| Komentar    | Deskripsi                                                                                      | Sintaks                                        |
| ----------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------- |
| Satu baris  | Komentar satu baris diberikan <br>di dalam tag (`<!--` komentar -->)                           | `<!-- komentar -->`                            |
| Multi baris | Ia mengikuti sintaksis komentar satu baris dengan<br>menambahkan beberapa baris dalam komentar | `<!-- komentar`<br>`multi`<br>`baris`<br>`-->` |
> Note : Pintasan untuk menambahkan komentar melalui papan ketik adalah dengan mengetik **Ctrl + /** pada Windows , dan **Command + /** untuk pengguna Mac .
## Contoh Komentar
**Komentar Satu Baris dan Komentar Sebaris**: Contoh ini menujukan cara menulis komentar satu baris dan komentar sebaris dalam HTML:

```html
<!DOCTYPE html>
<html>

<body>
    <!--This is heading Tag-->
    <h1>GeeksforGeeks</h1>

    <!--This is single line comment-->
    <h2>This is <!--given for--> single line comment</h2>

</body>

</html>
```

Jika dijalankan, Anda kaan melihat, bahwa komentar tidak akan ditampilkan di browser.

**Komentar Multi-Baris dan Bagian Kode Tersembunyi**: Contoh berikut menunjukkan cara menggunakan komentar multi-baris untuk menambahkan penjelasan yang lebih panjang dan menyembunyikan bagian kode sementara:

```html
<!DOCTYPE html>
<html>

<body>

    <!-- This is 
         heading tag -->
    <h1>GeeksforGeeks</h1>

    <!-- This is
         multi-line
         comment -->
    <h2>This is multi-line comment</h2>
    <!-- <button style="font-family: Sans-serif;">
           Click Me
         </button> -->

</body>

</html>
```

Jika dijalankan, hasilnya juga sama, bagian komentar tidak akan ditampilkan di browser.
## Penggunaan Komentar HTML
- **Organisasi Kode:** Komentar dapat membantu memecah bagian-bagian kode, membuatnya lebih mudah dinavigasi, terutama dalam proyek yang lebih besar.
- **Kolaborasi:** Saat bekerja dengan orang lain, komentar sangat penting untuk menjelaskan mengapa elemen HTML tertentu digunakan, atau untuk meninggalkan instruksi bagi anggota tim.
- **Debugging:** Menonaktifkan sementara bagian kode HTML dengan memberikan komentar merupakan penggunaan umum, yang memungkinkan pengembang untuk mengisolasi masalah.
- **Dokumentasi:** Menyediakan rincian atau dokumentasi dalam kode untuk referensi di masa mendatang tanpa memerlukan dokumentasi eksternal.
## Praktik Terbaik untuk Menulis Komentar yang Berguna dan Jelas
1. **Ringkas dan Relevan** : Tulis komentar yang singkat dan bermakna yang menjelaskan  __alasan__  di balik kode tersebut, bukan  __hal__ yang sudah jelas.
	
    *Contoh* :

	```html
	<!-- Menyesuaikan margin untuk penyelarasan yang lebih baik pada layar ponsel -->
	```

2. **Hindari berkomentar berlebihan** : Jangan mengomentari semuanya. Fokus pada bagian kode yang rumit atau tidak intuitif.  
    
    *Buruk* :
	```html
	 <!-- Ini adalah paragraf -->   
	<p>Selamat datang!</p>
	```

3. **Perbarui Komentar** : Revisi komentar secara berkala untuk memastikan komentar tetap akurat seiring perkembangan kode.
4. **Gunakan Gaya yang Konsisten** : Pertahankan nada dan format yang seragam untuk komentar di seluruh proyek guna memastikan kejelasan.  
    
    *Contoh* :
	```html
	<!-- Bagian: Bilah Navigasi -->
	```
5. **Hindari Informasi Sensitif** : Jangan pernah menyertakan kata sandi, kunci, atau data sensitif dalam komentar
