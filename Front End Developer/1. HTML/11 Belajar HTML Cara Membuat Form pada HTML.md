---
obsidianUIMode: preview
sumber: petanikode
level: medium
bahasa: HTML
tanggal_study: 2024-10-08T12:02:00
total_study: 1
tags:
  - HTML
id: PTHTML11
sr-due: 2024-10-10
sr-interval: 2
sr-ease: 150
---
# Belajar HTML #11: Cara Membuat Form pada HTML

---

![Tutorial Belajar HTML 5](https://www.petanikode.com/img/html/html.png)

Web tidak hanya digunakan untuk menampilkan informasi saja…

…Web juga digunakan untuk mengambil informasi atau data dari pengunjung.

Salah satu cara untuk mengambil informasi dari pengunjung ialah menggunakan **form**.

Form dalam web bisa disamakan dengan formulir di dunia nyata.

Form dapat diisi, kemudian diproses dengan program tertentu.

Pada tutorial ini, kita akan belajar **cara membuat form di HTML**.

Hanya membuat saja ya…

Tidak sampai memproses datanya.

Karena itu masuk ke dalam topik pembahasan yang lain.

Baiklah…

Mari kita mulai.

## Cara Membuat Form di HTML

Form di HTML dapat kita buat dengan tag `<form>`.

Tag ini memiliki beberapa atribut yang harus diberikan, seperti:

- `action` untuk menentukan aksi yang akan dilakukan saat data dikirim;
- `method` metode pengiriman data.

Contoh:

```html
<form action="proses.php" method="GET">
<!-- form field di sini -->
</form>
```

Untuk atribut `action`, kita dapat mengisinya dengan alaman URL dari _endpoint_ yang akan memproses form.

Secara sederhana,—pada contoh di atas— kita akan menyuruh file `proses.php` untuk memproses data form.

Ini nanti akan kita pelajari pada PHP.

Kode HTML di atas, tidak akan menghasilkan apa-apa.

Karena kita belum membuat field-nya.

## Apa itu Field?

**Field** adalah ruas yang dapat diisi dengan data.

Contoh field:

```html
<input type="text" name="info" />
```

Field memiliki beberapa atribut yang harus diberikan:

1. `type` merupakan type dari field.
2. `name` merupakan nama dari field yang akan menjadi kunci dan variabel di dalam program.

## Latihan: Membuat Form Login

Sebagai latihan, mari kita buat form login.

Pada form login, terdapat beberapa field dan elemen:

1. Field untuk input username atau email;
2. Field untuk input password;
3. Checkbox untuk remember me;
4. Tombol untuk login.

Berikut ini kodenya:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Form Login</title>
</head>
<body>
    <form action="login.php" method="POST">
        <fieldset>
        <legend>Login</legend>
        <p>
            <label>Username:</label>
            <input type="text" name="username" placeholder="username..." />
        </p>
        <p>
            <label>Password:</label>
            <input type="password" name="password" placeholder="password..." />
        </p>
        <p>
            <label><input type="checkbox" name="remember" value="remember" /> Remember me</label>
        </p>
        <p>
            <input type="submit" name="submit" value="Login" />
        </p>
        </fieldset>
    </form>
</body>
</html>
```

Hasilnya:

![Form login dengan HTML](https://www.petanikode.com/img/html/form/form-login.png)

Sekarang perhatikan!

Pada kode di atas, kita membuat empat buah filed:

1. input `username` dengan tipe `text`;
2. input `password` dengan tipe `password`;
3. input `remember` dengan tipe `checkbox`;
4. input `submit` dengan tipe `submit`;

Lalu ketiga filed ini dibungkus ke dalam tag `<fieldset>`.

Nanti tag `<fieldset>` ini akan membuat sebuah garis.

Di dalam tag `<fieldset>`, kita membuat tag `<legend>` untuk memberikan teks pada _fieldset_.

Lalu, perhatikan juga atribut yang digunakan pada setiap field.

- Atribut `placeholder` untuk menampilkan teks sementara _(placeholder)_;
- Atribut `value` untuk memberikan nilai default pada field.

Setiap field kita bungkus dalam tag `<p>` agar terlihat rapi dan juga kita berikan sebuah label dengan tag `<label>`.

## Latihan: Membuat Form Contact

Latihan Selanjutnya, kita akan membuat form _contact_. Form ini berfungsi untuk menghubungi atau kontak admin.

Silakan ikuti kode berikut:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Contact Us</title>
</head>
<body>
    <form action="contact.php" method="POST">
        <fieldset>
        <legend>Contact</legend>
        <p>
            <label>Name:</label>
            <input type="text" name="name" placeholder="your name..." />
        </p>
        <p>
            <label>Subject:</label>
            <input type="text" name="subject" placeholder="subject..." />
        </p>
        <p>
            <label>Email:</label>
            <input type="email" name="email" placeholder="your email..." />
        </p>
        <p>
            <input type="submit" name="submit" value="Send" />
        </p>
        </fieldset>
    </form>
</body>
</html>
```

Hasilnya:

![Form Contact dengan HTML](https://www.petanikode.com/img/html/form/form-contact.png)

Pada contoh di atas, kita memberikan `type="email"` untuk field `email`, agar filed ini harus diisi dengan email saja.

Coba saja isi dengan yang lain, lalu klik **Send**…maka akan muncul pesan peringatan.

![Form contact error](https://www.petanikode.com/img/html/form/form-contact-error.png)

## Latihan: Membuat Form Register

Semakin banyak latihan, semakin bagus.

Berikutnya kita akan coba membuat form registrasi.

Form ini berisi field untuk:

- Input nama lengkap;
- Input username;
- Input email;
- Input password;
- Input jenis kelamin;
- Input Agama;
- Input Biografi.
- dsb.

Mari kita buat…

```html
<!DOCTYPE html>
<html>
<head>
    <title>Registrasi</title>
</head>
<body>
    <form action="contact.php" method="POST">
        <fieldset>
        <legend>Registrasi</legend>
        <p>
            <label>Nama:</label>
            <input type="text" name="nama" placeholder="Nama lengkap..." />
        </p>
        <p>
            <label>Username:</label>
            <input type="text" name="username" placeholder="Username..." />
        </p>
        <p>
            <label>Email:</label>
            <input type="email" name="email" placeholder="Your email..." />
        </p>
        <p>
            <label>Password:</label>
            <input type="password" name="password" placeholder="Passowrd..." />
        </p>
        <p>
            <label>Jenis kelamin:</label>
            <label><input type="radio" name="jenis_kelamin" value="laki-laki" /> Laki-laki</label>
            <label><input type="radio" name="jenis_kelamin" value="perempuan" /> Perempuan</label>
        </p>
        <p>
            <label>Agama:</label>
            <select name="agama">
                <option value="islam">Islam</option>
                <option value="kristen">Kristen</option>
                <option value="hindu">Hindu</option>
                <option value="budha">Budha</option>
            </select>
        </p>
        <p>
            <label>Biografi:</label>
            <textarea name="biografi"></textarea>
        </p>
        <p>
            <input type="submit" name="submit" value="Daftar" />
        </p>
        </fieldset>
    </form>
</body>
</html>
```

Hasilnya:

![Form register dengan HTML](https://www.petanikode.com/img/html/form/form-register.png)

Apa saja field baru yang ada di form tersebut?

1. Field `radio`;
2. Field `<select><option>`;
3. Field `<textearea>`.

Apa bedanya `radio` dengan `checkbox`?

Jika kita ingin agar pengunjung memilih salah satu, maka kita gunakan `radio`.

Tapi kalau kita ingin pengunjung memilih lebih dari satu, maka kita gunakan `checkbox`.

Lalu untuk `<select></option>`, sifatnya sama seperti `radio`. Cuma dia bentuknya berbeda.

Lalu untuk menginputkan teks yang panjang, kita gunakan tag `<textarea>`.

## Latihan: Membuat Form Tingkat Lanjut

Field-field di atas merupakan jenis field yang sering digunakan dalam pembuatan form.

Masih ada jenis field lagi yang belum kita coba, seperti `meter`, `color`, `url`, `number`, `date`, `datetime`, dsb.

Mari kita coba beberapa:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Form HTML</title>
</head>
<body>
    <form action="contact.php" method="POST">
        <fieldset>
        <legend>Form</legend>
        <p>
            <label>Alamat Web:</label>
            <input type="url" name="name" placeholder="Masukan URL Web..." />
        </p>
        <p>
            <label>Tanggal Lahir:</label>
            <input type="date" name="tanggal" />
        </p>
        <p>
            <label>Umur:</label>
            <input type="number" min="10" max="90" name="umur" />
        </p>
        <p>
            <input type="submit" name="submit" value="Send" />
        </p>
        </fieldset>
    </form>
</body>
</html>
```

Hasilnya:

![Form dengan tipe field yang lain](https://www.petanikode.com/img/html/form/misc.png)

Apabila di browser anda tidak tampil kalender seperti di atas, coba gunakan browser versi terbaru.

## Apa Selanjutnya?

Apa yang kita pelajari pada tutorial ini adalah tag dan field dasar—dan sering digunakan—dalam pembuatan form.

Masih terdapat banyak tipe field lagi yang belum kita coba. Seperti: `meter`, `color`, `time`, dsb.

Karena itu, silakan berlatih terus…
- [[12 Belajar HTML Mengenal Elemen Semantik pada HTML]]