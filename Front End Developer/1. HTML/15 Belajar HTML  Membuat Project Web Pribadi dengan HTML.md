---
obsidianUIMode: preview
sumber: petanikode
level: sulit
bahasa: HTML
tanggal_study: 2024-10-08T16:20:00
total_study: 1
tags:
  - HTML
id: PTHTML15
sr-due: 2024-10-10
sr-interval: 2
sr-ease: 152
---
# Belajar HTML #15: Membuat Project Web Pribadi dengan HTML

---

![Membuat Project Web Pribadi dengan HTML](https://www.petanikode.com/img/cover/html-project.png)

Kini tiba saatnya kamu melatih ilmu HTML yang sudah dipelajari.

Pada tutorial ini, kita akan mencoba membuat project web kecil-kecilan. Tujuannya untuk berlatih dan memahami bagaimana cara membuat web.

Baiklah..

Langsung saja kita mulai.

## Step 1 – Membuat Desain Web

Pembuatan web dimulai dengan desain. Kalau tidak ada desain, nanti kita akan kesulitan dan tidak akan tahu mau buat apa.

Biasanya desain web dikerjakan oleh desainer, setelah itu diserahkan ke programmer untuk diubah menjadi HTML.

Pada project ini, kita akan membuat tiga halaman web, yakni _home_, _contact_, dan _about_. Desain yang digunakan adalah desain dalam bentuk _wireframe_ atau sketsa.

Berikut ini desain untuk tiap-tiap halaman:

### 1. Desain Halaman Home

![Desain halaman home](https://www.petanikode.com/img/html-project/desain-home.png)

Halaman home adalah halaman utama yang akan dibuka pertama kali saat pengunjung membuka website. Halaman ini berisi menu, foto, teks, dan tabel.

### 2. Desain Halaman Contact

![Desain halaman home](https://www.petanikode.com/img/html-project/desain-contact.png)

Halaman contact adalah halaman yang berisi form untuk menghubungi pemilik website.

### 3. Desain Halaman About

![Desain halaman home](https://www.petanikode.com/img/html-project/desain-about.png)

Halaman about adalah halaman yang berisi informasi lengkap tentang website.

## Step 2 – Memulai Project Web

Silakan buat folder baru dengan nama `websiteku`.

Setelah itu buat folder `image` dan `video` di dalam folder `websiteku`. Folder `image` akan kita gunakan untuk menyimpan gambar dan `video` untuk menyimpan video.

Sehingga nanti struktur folder kita akan menjadi seperti ini:

- 📁 `image`
    - 🖼️ `foto-profile.jpg`
- 📁 `video`
    - 🎞 `video-about.webm`
- 📄 `cv-name.pdf`
- 📜 `index.html`
- 📜 `contact.html`
- 📜 `about.html`
- 🖼️ `favicon.ico`

File yang perlu kamu persiapkan di tahapan ini adalah `foto-profile.jpg` dan `video-about.webm`.

Berikutnya, kita akan mulai menulis kode. Silakan buka folder `websiteku` dengan Visual Studio Code.

Caranya:

Klik menu **File**, lalu pilih **Open Folder** dan carilah folder `websiteku`.

Dengan begini, kita sudah siap untuk menulis kode.

![Open Folder di Visual Studio Code](https://www.petanikode.com/img/html-project/vscode-websiteku.webp)

## Step 3 – Membuat Halaman Home

Silakan buat file baru bernama `index.html` di dalam folder websiteku.

Setelah itu, isi dengan kode berikut:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmad Muhardian Personal Website</title>
</head>

<body>
    <nav>
        <a href="index.html">Home</a> |
        <a href="cv-dian.pdf">Download CV</a> |
        <a href="contact.html">Contact</a> |
        <a href="about.html">About me</a>
    </nav>

    <hr />

    <header style="text-align: center;">
        <img src="image/foto-profile.jpg" width="200" height="200" style="border-radius: 50%;"/>
        <h1>Ahmad Muhardian</h1>
        <p>(Web Developer)</p>
    </header>

    <hr />

    <article style="text-align: center;">
        <h2>Overview</h2>
        <p>
            Hi, saya adalah web developer yang berdomisili di Jakarta.
            Saat ini sedang belajar HTML di Petani Kode
        </p>
    </article>

    <div style="max-width: 600px; margin: 3em auto">
        <table border="1" width="100%">
            <thead>
                <tr>
                    <th>Skill</th>
                    <th>Pengalaman</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>
                        <ul>
                            <li>HTML (Expert)</li>
                            <li>CSS (Beginner)</li>
                            <li>Javascript (Beginner)</li>
                        </ul>
                    </td>
                    <td>
                        <ul>
                            <li>Freelancer di Internet</li>
                            <li>Leader Local Linux Community</li>
                            <li>Leader Local Linux Community</li>
                        </ul>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>

    <hr>
    <footer style="text-align: center;">
        <p>Copyright &copy; 2020 Ahmad Muhardian.</p>
    </footer>
</body>
</html>
```

Jangan lupa untuk mengubah nama `Ahmad Muardian` dengan nama kamu.

Jika kita coba membuka file `index.html`, maka hasilnya akan seperti ini:

![Halaman home tidak ada gambar](https://www.petanikode.com/img/html-project/home-no-image.webp)

Gambarnya tidak bisa tampil karena kita belum menambahkan file gambar di dalam folder `image`.

Silakan tambahkan file gambar dengan nama `foto-profile.jpg`. Pastikan gambar yang ditambahkan memiliki ukuran persegi atau rasio 1:1. Pada proyek ini, saya menggunakan gambar dengan ukuran 200x200 piksel.

> Download file gambar: ⬇️ [foto-profile.jpg](https://github.com/petanikode/belajar-html/raw/master/websiteku/image/foto-profile.jpg)

![Menambahkan file gambar](https://www.petanikode.com/img/html-project/add-image.png)

Setelah itu, coba refresh halaman home atau `index.html`.

Maka hasilnya:

![Halaman home dengan gambar](https://www.petanikode.com/img/html-project/home-with-image.webp)

## Step 4 – Membuat Halaman About Me

Buatlah file HTML baru dengan nama `about.html`.

Kemudian isi dengan kode berikut:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmad Muhardian Personal Website</title>
</head>

<body>
    <nav>
        <a href="index.html">Home</a> |
        <a href="cv-dian.pdf">Download CV</a> |
        <a href="contact.html">Contact</a> |
        <a href="about.html">About me</a>
    </nav>

    <hr />

    <article>
        <h1>About Me</h1>
        <p>
            Hi, saya adalah web developer yang berdomisili di Jakarta.
            Saat ini sedang belajar HTML di Petani Kode.
        </p>
        <p>
            Saya memang masih baru dalam web development, karena itu
            saya tidak akan pernah berhenti belajar.
        </p>
        <p>
            Saya ingin menguasai bahasa HTML, CSS, dan Javascript.
            Simak video lengkap tentang saya.
        </p>
        <p>
            <video controls>
                <source src="video/video-about.webm" type="video/webm"/>
            </video>
        </p>
    </article>

    <hr>
    <footer style="text-align: center;">
        <p>Copyright &copy; 2020 Ahmad Muhardian.</p>
    </footer>
</body>
</html>
```

Sama seperti halaman home, halaman ini juga memiliki konten berupa video untuk ditampilkan. Tapi file videonya belum ada.

Sudah pasti videonya tidak akan bisa ditampilkan:

![Halaman About tanpa video](https://www.petanikode.com/img/html-project/about-no-video.webp)

Karena itu, silakan tambahkan file video-nya ke dalam folder `video` dengan nama `video-about.webm.`

![Menambahkan File Video](https://www.petanikode.com/img/html-project/add-video.png)

> Jika kamu belum punya filenya, silakan download di link ini:
> 
> ⬇️ [video-about.webm](https://github.com/petanikode/belajar-html/raw/master/websiteku/video/video-about.webm)

Setelah itu, coba buka dan refresh halaman about.

Maka hasilnya:

![Halaman About dengan video](https://www.petanikode.com/img/html-project/about-with-video.webp)

## Step 5 – Membuat Halaman Contact

Buatlah file baru dengan nama `contact.html`.

Kemudian isi dengan kode berikut:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmad Muhardian Personal Website</title>
</head>

<body>
    <nav>
        <a href="index.html">Home</a> |
        <a href="cv-dian.pdf">Download CV</a> |
        <a href="contact.html">Contact</a> |
        <a href="about.html">About me</a>
    </nav>

    <hr />

    <div>
        <h1>Contact Me</h1>
        <form>
            <label for="email">Email</label><br />
            <input type="email" name="email" placeholder="alamat email"/>
            <br />
            <label for="message">Pesan</label><br />
            <textarea name="message" placeholder="Tulis pesan anda..." rows="4" cols="80"></textarea>
            <br />
            <br />
            <input type="submit" value="Kirim" />
        </form>
    </div>

    <hr>
    <footer style="text-align: center;">
        <p>Copyright &copy; 2020 Ahmad Muhardian.</p>
    </footer>
</body>
</html>
```

Hasilnya:

![Halaman contact me](https://www.petanikode.com/img/html-project/contact.webp)

Form contact ini belum bisa berfungsi, karena kita belum membuat kode untuk mengirim data.

## Step 6 – Membuat Fitur Download CV

Fitur ini sebenarnya paling gampang dibuat. Kita hanya perlu menambahkan file `cv-dian.pdf` ke dalam folder websiteku.

> Download file: ⬇️ [cv-dian.pdf](https://github.com/petanikode/belajar-html/raw/master/websiteku/cv-dian.pdf)

![Menambahkan file pdf](https://www.petanikode.com/img/html-project/add-pdf.png)

Setelah itu, coba klik menu **Download CV**. Jika PDF-nya terbuka, maka link ini sudah benar.

## Step 7 – Membuat Ikon untuk Web

Agar websitenya terlihat menarik, kita akan membuat ikon atau _favicon_. Silakan buka [favicon-generator.org](https://www.favicon-generator.org/) kemudian pilih gambar yang akan dijadikan ikon.

![Membuat favicon](https://www.petanikode.com/img/html-project/create-favicon.png)

Setelah itu, kita akan mendapatkan link download dan juga kode HTML yang harus ditambahkan ke dalam tag `<head>` agar ikon bisa ditampilkan.

![Download favicon](https://www.petanikode.com/img/html-project/download-favicon.png)

Setelah kita mendapatkan ikon, simpan ikonnya ke dalam folder `websiteku`.

![Menambahkan favicon](https://www.petanikode.com/img/html-project/add-favicon.png)

Terakhir, tugas kita tinggal membuat kode HTML untuk menampilkan ikon. Silakan copy kode berikut:

```html
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

Kemudian paste di dalam tag `<head>` pada setiap halaman.

![Menambahkan kode favicon](https://www.petanikode.com/img/html-project/kode-favicon.png)

Maka hasilnya:

![Menampilkan favicon](https://www.petanikode.com/img/html-project/favicon.png)

## Apa Selanjutnya?

Akhirnya selesai juga..

Sebenarnya kamu bisa berkreasi sebebas mungkin, tanpa harus mengikuti desain di tutorial ini.

Selanjutnya silakan pelajari tentang: