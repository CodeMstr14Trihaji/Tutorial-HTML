---
obsidianUIMode: preview
sumber: petanikode
level: pemula
bahasa: HTML
tanggal_study: 2024-10-08T22:00:00
total_study: 1
tags:
  - HTML
id: PTHTML16
sr-due: 2024-10-11
sr-interval: 2
sr-ease: 150
---
# Belajar HTML #16: Cara Hosting Website di Netlify (Kurang dari 30 detik, langsung go online)

---

![Cara Hosting Website di Netlify](https://www.petanikode.com/img/cover/html-netlify.png)

Sebenarnya banyak penyedia layanan hosting untuk web statis.

Ada yang berbayar, ada juga yang gratis.

Lalu..

Mengapa memilih Netlify?

Netlify, sangat cepat dan mudah.

Mereka mengklaim:

“Hosting web di netlify tidak sampai 30 detik”

Apakah benar demikian?

Mari kita sama-sama buktikan..

## Apa itu Netlify?

Netlify adalah penyedia layanan hosting untuk _static site_ dengan berbagai fitur menarik.

Netlify menyediakan semua kebutuhan untuk workflow web development _zaman now_.

Mengapa saya bilang _zaman now_?

Karena di Netlify tidak menggunakan FTP seperti yang biasa kita temukan pada _shared hosting_.

Netlify menggunakan [Git](https://www.petanikode.com/topik/git/) dan CI/CD untuk melakukan _deployment_. Kedua alat ini sangat membantu dalam melakukan _deployment_.

Selain itu, Netlify juga menyediakan fitur untuk mengelola DNS, SSL atau HTTPS diberikan gratis, _form_, _function_, dan lain-lain.

Soal Harga bagaimana?

Tenang saja, kabar baiknya Netlify sangat bersahabat dengan kantong mahasiswa. Cek saja di [halaman _pricing_](https://www.netlify.com/pricing/) untuk melihat paket hosting yang tersedia.

![Harga paket hosting di Netlify](https://www.petanikode.com/img/hugo/netlify/pricing.png)

Ada paket Starter, yang ini **gratis**. Tapi jika ingin berlangganan yang Pro juga bisa.

Saran saya, mulai dulu pakai paket Starter. Kalau ingin fitur yang lebih, baru upgrade ke Pro.

Oh iya, web petanikode juga pernah pakai yang starter dan sudah berjalan hampir selama 2 tahun. 😊

Tapi karena ramainya pengunjung membuat bandwidth-nya cepat habis. Netlify memberikan jatah 100GB bandwidth per bulan untuk paket starter.

Jika melewati batasan bandwidth tersebut, websitemu tidak akan bisa dibuka.

## Cara Mendaftar Akun Netlify

Silakan buka halaman [pendaftaran akun Netlify](https://app.netlify.com/signup).

Kemudian, kita bisa daftar dengan akun Github, Gitlab, Bitbucket, dan Email. Silakan pilih salah satu metode pendaftaran yang akan kamu gunakan.

![Halaman Register Netlify](https://www.petanikode.com/img/hugo/netlify/signup.png)

Jika kita menggunakan email, maka kita akan diminta alamat email dan password.

![Pendaftaran akun Netlify dengan email](https://www.petanikode.com/img/html-netlify/signup-email.png)

Setelah sukses mendaftar, kita akan memiliki halaman dashboard seperti berikut.

![Dashboard Netlify](https://www.petanikode.com/img/html-netlify/dashboard-netlify.png)

## Upload Website ke Netlify

Netlify tidak seperti shared hosting yang harus pakai FTP untuk upload website.

Di sini kita bisa gunakan dua cara:

1. Menggunakan Git
2. Drag/Drop

Yang paling gampang adalah **drag/drop**, jika kamu ingin menggunakan Git.. pastikan sudah paham dulu tentang git.

O ya, kamu bisa belajar Git di:

- 📖 [Tutorial Git untuk Pemula](https://www.petanikode.com/tutorial/git/)

Tapi, karena kondisi kita di sini belum tau Git.. maka kita akan gunakan teknik drag/drop.

Baiklah, siapkan terlebih dahulu website yang akan di-upload. Kita akan menggunakan 📁 `websiteku` yang sudah buat pada [project web di tutorial sebelumnya](https://www.petanikode.com/html-project/).

![Folder website yang akan di-upload ke Netlify](https://www.petanikode.com/img/html-netlify/file-website.png)

Silakan drag/drop folder 📁 `websiteku` ke dashboard Netlify dan tunggulah sampai proses upload selesai.

Tunggulah sampai status production-nya menjadi **published**.

![Deploy status di netlify](https://www.petanikode.com/img/html-netlify/published.png)

Ini artinya, website kita sudah berhasil di-upload dan dipublikasi di Netlify.

Wow, benar kan..

**Tidak sampai 30 detik, website kita sudah go online 🤩.**

Keren ya.

Jika kita perhatikan, website yang di-upload akan mendapatkan alamat domain acak seperti `silly-blackwell-3e7430.netlify.app`.

Domain ini gratis diberikan oleh Netlify..

![Alamat domain app di netlify](https://www.petanikode.com/img/html-netlify/netlify-domain.png)

..dan kita juga bisa mengubahnya sesuai selera.

Sekarang coba klik alamat domain tersebut, maka kita akan bisa melihat hasil website yang baru saja kita upload.

![Demo website](https://www.petanikode.com/img/html-netlify/demo-web.png)

Gampang banget kaan…

Nah, sekarang kita akan coba mengubah nama domainnya agar mudah diingat.

## Mengubah Nama Domain

Silakan masuk ke **Domain Settings**.

![Menu domain setting](https://www.petanikode.com/img/html-netlify/menu-domain-setting.png)

Pada bagian sebelah kanan, klik **option** kemudian pilih **Edit site name**.

![Edit site name](https://www.petanikode.com/img/html-netlify/edit-site-name.png)

Pada jendela pop-up yang muncul, ubahlah nama domainnya dengan nama yang kamu inginkan.

Sebagai contoh, saya akan mengubah namanya dengan `belajarhtml`.

![Mengubah nama domain di netlify](https://www.petanikode.com/img/html-netlify/rename-domain.png)

Jika nama domain tersebut, belum diambil orang atau belum ada yang pakai.. maka saya akan bisa menggunakannya.

Jadi nanti websitenya akan bisa dibuka melalui `https://belajarhtml.netlify.app`.

Oh iya, kita juga bisa menambahkan custom domain dengan mengklik **add custom domain**.

![Menu custom domain](https://www.petanikode.com/img/html-netlify/menu-custom-domain.png)

Jika kamu sudah punya alamat domain, kamu bisa pointing alamat Name Server-nya ke server Netlify.

## Cara Update Website di Netlify

Website sudah berhasil kita upload.

Tapi, bagaimana cara update jika ada perubahan?

Caranya sangat gampang..

Kita hanya perlu meng-upload ulang folder websitenya.

Silakan masuk ke menu **Deploys**.

![Menu deploys](https://www.petanikode.com/img/html-netlify/menu-deploys.png)

Setelah halaman _deploys_ terbuka, di sana kita bisa upload ulang websitenya.

![Drop area untuk upload website](https://www.petanikode.com/img/html-netlify/drop-area.png)

Website akan di-deploy ulang dengan yang baru.

## Konfigurasi Netlify Form

Netlify form adalah fitur yang diberikan netlify untuk mengelola form. Fitur ini memungkinkan pengunjung web untuk mengisi form dan mengirimnya ke pemilik website.

Cara mengaktifkan netlify form sangat gampang, kita hanya perlu menambahkan atribut `netlify` pada tag `<form>`.

```html
<form method="POST" netlify>
</form>

<!-- atau bisa juga -->

<form method="POST" netlify="true>
</form>
```

Oke sekarang mari kita ubah lagi website yang sudah kita buat. Buka file `contact.html`, kemudian ubah kode di bagian tag `<form>` menjadi seperti ini:

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmad Muhardian Personal Website</title>

    <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
    <link rel="icon" href="favicon.ico" type="image/x-icon">
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
        <form method="POST" netlify>
            <label for="email">Email</label><br />
            <input type="email" name="email" placeholder="alamat email" />
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

Setelah itu, upload ulang websitenya di halaman _deploys_. Tunggulah sampai status deploy-nya menjadi **published**.

![Publish new deploy](https://www.petanikode.com/img/html-netlify/update-form.png)

Nah, sekarang coba [buka websitenya](https://belajarhtml.netlify.app/contact.html) dan isilah form kontak.

Jika berhasil tampil halaman **Thank you!** berarti data yang kita inputkan berhasil terkirim ke pemilik website.

Untuk memastikan sudah terkirim atau tidak, kita bisa cek di menu form atau inbox dari email yang digunakan untuk mendaftar netlify.

![Menu form](https://www.petanikode.com/img/html-netlify/menu-form.png)

Berikut ini contoh isi pesan yang kita terima dari form.

![Contoh isi pesan form](https://www.petanikode.com/img/html-netlify/form-message.png)

Sejauh ini website kita sudah berjalan dengan baik.

## Lalu.. apa Selanjutnya?

Selamat! 🎉 🎉 🎉

Kamu baru saja menyelesaikan seri tutorial HTML untuk pemula. Tutorial basic ini, kita akhiri sampai di sini ya..

Berikutnya, kamu bisa lanjutkan dengan belajar CSS ataupun belajar Javascript:

- 📖 [Tutorial CSS untuk Pemula](https://www.petanikode.com/tutorial/css/)
- 📖 [Tutorial Javascript untuk Pemula](https://www.petanikode.com/tutorial/javascript/)

Saran saya:

Sebaiknya belajar CSS dulu.. baru setelah itu belajar Javascript.

Nah, untuk meningkatkan pemahamanmu tentang HTML, cobalah untuk berlatih lagi membuat website sederhana dan pelajari tag-tag yang belum dibahas di seri tutorial ini.

Seperti:
- [Tag canvas untuk pemrograman grafis di HTML](https://www.petanikode.com/html-canvas/)
- [Cara Menampilkan Gambar dari Webcam di HTML](https://www.petanikode.com/html-webcam/)
- [Membuat Getaran di Website dengan Vibration di HTML](https://www.petanikode.com/tutorial-html-vibrations/)
- dll.

Akhir kata..

Semoga bermanfaat.