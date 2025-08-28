# Bab 5: Form dan Input HTML

## 🎯 Tujuan Pembelajaran
Setelah menyelesaikan bab ini, kalian akan mampu:
- Memahami konsep form dan interaksi user dalam web
- Menggunakan tag `<form>` dengan berbagai atribut
- Mengimplementasikan berbagai jenis input HTML
- Menggunakan label untuk aksesibilitas
- Membuat form yang user-friendly dan responsive
- Menerapkan validasi form HTML5
- Memahami pengiriman data form

## 📚 Konsep Dasar

### Apa itu Form HTML?
**Form** adalah elemen yang memungkinkan pengguna memasukkan dan mengirim data ke server web. Form adalah jembatan komunikasi antara user dan aplikasi web.

**Analogi Sederhana:**
Form HTML seperti formulir kertas yang kalian isi di bank atau rumah sakit. Kalian mengisi kolom-kolom yang tersedia, kemudian menyerahkannya kepada petugas untuk diproses.

### Kenapa Form Penting?
1. **Interaksi User** - Memungkinkan user berpartisipasi aktif
2. **Pengumpulan Data** - Mengumpulkan informasi dari user
3. **Komunikasi** - Channel komunikasi antara user dan website
4. **Fungsionalitas** - Membuat website menjadi interaktif dan dinamis

---

## 📝 Tag `<form>` - Container Utama

### Definisi dan Tujuan
Tag `<form>` adalah container yang menampung semua elemen input dan mengatur bagaimana data dikirim ke server.

### Syntax Dasar
```html
<form action="/submit" method="post">
    <!-- Elemen form di sini -->
</form>
```

### Atribut Form Utama
| Atribut | Tujuan | Nilai | Contoh |
|---------|--------|-------|---------|
| `action` | URL tujuan pengiriman data | URL | `action="/submit"` |
| `method` | Cara pengiriman data | `get`, `post` | `method="post"` |
| `enctype` | Tipe encoding data | `application/x-www-form-urlencoded`, `multipart/form-data` | `enctype="multipart/form-data"` |
| `target` | Target pembukaan response | `_self`, `_blank`, `_parent`, `_top` | `target="_blank"` |
| `novalidate` | Menonaktifkan validasi HTML5 | boolean | `novalidate` |

### Contoh Form Dasar
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Dasar</title>
</head>
<body>
    <h1>Form Pendaftaran</h1>

    <form action="/daftar" method="post">
        <label for="nama">Nama Lengkap:</label>
        <input type="text" id="nama" name="nama" required>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>

        <button type="submit">Daftar</button>
    </form>
</body>
</html>
```

---

## 🔤 Tag `<input>` - Elemen Input Utama

### Definisi dan Tujuan
Tag `<input>` adalah elemen self-closing yang digunakan untuk membuat berbagai jenis input field.

### Input Type Text
```html
<label for="nama">Nama:</label>
<input type="text" id="nama" name="nama" placeholder="Masukkan nama Anda">
```

**Atribut Umum untuk Input Text:**
- `placeholder` - Teks petunjuk
- `maxlength` - Panjang maksimal karakter
- `minlength` - Panjang minimal karakter
- `pattern` - Regex pattern untuk validasi
- `required` - Field wajib diisi

### Input Type Email
```html
<label for="email">Email:</label>
<input type="email" id="email" name="email" placeholder="nama@email.com" required>
```

### Input Type Password
```html
<label for="password">Password:</label>
<input type="password" id="password" name="password" minlength="8" required>
```

### Input Type Number
```html
<label for="umur">Umur:</label>
<input type="number" id="umur" name="umur" min="1" max="100" step="1">
```

### Input Type Date
```html
<label for="tanggal">Tanggal Lahir:</label>
<input type="date" id="tanggal" name="tanggal" min="1900-01-01" max="2023-12-31">
```

### Input Type Range
```html
<label for="rating">Rating (1-10):</label>
<input type="range" id="rating" name="rating" min="1" max="10" value="5">
```

### Input Type File
```html
<label for="foto">Upload Foto:</label>
<input type="file" id="foto" name="foto" accept="image/*">
```

### Input Type Radio
```html
<fieldset>
    <legend>Jenis Kelamin:</legend>
    <label>
        <input type="radio" name="gender" value="pria" required>
        Pria
    </label>
    <label>
        <input type="radio" name="gender" value="wanita" required>
        Wanita
    </label>
</fieldset>
```

### Input Type Checkbox
```html
<label>
    <input type="checkbox" name="hobi" value="membaca">
    Membaca
</label>
<label>
    <input type="checkbox" name="hobi" value="olahraga">
    Olahraga
</label>
```

---

## 🏷️ Tag `<label>` - Label Aksesibilitas

### Definisi dan Tujuan
Tag `<label>` menghubungkan teks deskripsi dengan elemen form, meningkatkan aksesibilitas dan user experience.

### Cara Penggunaan Label

#### 1. Dengan Atribut `for`
```html
<label for="username">Username:</label>
<input type="text" id="username" name="username">
```

#### 2. Wrap Input di Dalam Label
```html
<label>
    Email:
    <input type="email" name="email">
</label>
```

#### 3. Kombinasi dengan Radio/Checkbox
```html
<label for="setuju">
    <input type="checkbox" id="setuju" name="setuju" value="yes">
    Saya setuju dengan syarat dan ketentuan
</label>
```

---

## 📄 Tag `<textarea>` - Input Teks Panjang

### Definisi dan Tujuan
Tag `<textarea>` digunakan untuk input teks multi-baris seperti komentar, alamat, atau pesan.

### Syntax dan Atribut
```html
<label for="pesan">Pesan:</label>
<textarea id="pesan"
          name="pesan"
          rows="5"
          cols="40"
          placeholder="Tulis pesan Anda di sini..."
          maxlength="500"
          required></textarea>
```

**Atribut Textarea:**
- `rows` - Jumlah baris yang terlihat
- `cols` - Jumlah kolom (lebar)
- `maxlength` - Panjang maksimal karakter
- `placeholder` - Teks petunjuk
- `readonly` - Hanya bisa dibaca
- `disabled` - Nonaktif

---

## 🔽 Tag `<select>` dan `<option>` - Dropdown

### Definisi dan Tujuan
Tag `<select>` membuat dropdown menu, dengan pilihan didefinisikan oleh tag `<option>`.

### Select Dasar
```html
<label for="kota">Pilih Kota:</label>
<select id="kota" name="kota" required>
    <option value="">-- Pilih Kota --</option>
    <option value="jakarta">Jakarta</option>
    <option value="surabaya">Surabaya</option>
    <option value="bandung">Bandung</option>
    <option value="medan">Medan</option>
</select>
```

### Select Multiple
```html
<label for="bahasa">Bahasa yang Dikuasai:</label>
<select id="bahasa" name="bahasa" multiple>
    <option value="indonesia">Bahasa Indonesia</option>
    <option value="english">English</option>
    <option value="mandarin">Mandarin</option>
    <option value="arab">Arab</option>
</select>
```

### Select dengan Optgroup
```html
<label for="makanan">Pilih Makanan:</label>
<select id="makanan" name="makanan">
    <optgroup label="Makanan Indonesia">
        <option value="nasi-gudeg">Nasi Gudeg</option>
        <option value="rendang">Rendang</option>
        <option value="sate">Sate</option>
    </optgroup>
    <optgroup label="Makanan Internasional">
        <option value="pizza">Pizza</option>
        <option value="burger">Burger</option>
        <option value="sushi">Sushi</option>
    </optgroup>
</select>
```

---

## 🎛️ Tag `<fieldset>` dan `<legend>`

### Definisi dan Tujuan
`<fieldset>` mengelompokkan elemen form yang berkaitan, sedangkan `<legend>` memberikan judul untuk grup tersebut.

### Contoh Penggunaan
```html
<form>
    <fieldset>
        <legend>Informasi Pribadi</legend>

        <label for="nama-depan">Nama Depan:</label>
        <input type="text" id="nama-depan" name="nama-depan" required>

        <label for="nama-belakang">Nama Belakang:</label>
        <input type="text" id="nama-belakang" name="nama-belakang" required>

        <fieldset>
            <legend>Jenis Kelamin</legend>
            <label>
                <input type="radio" name="gender" value="pria">
                Pria
            </label>
            <label>
                <input type="radio" name="gender" value="wanita">
                Wanita
            </label>
        </fieldset>
    </fieldset>

    <fieldset>
        <legend>Informasi Kontak</legend>

        <label for="email-kontak">Email:</label>
        <input type="email" id="email-kontak" name="email" required>

        <label for="telepon">Telepon:</label>
        <input type="tel" id="telepon" name="telepon">
    </fieldset>
</form>
```

---

## 🔘 Tag `<button>` - Tombol Aksi

### Definisi dan Tujuan
Tag `<button>` membuat tombol interaktif yang dapat melakukan berbagai aksi pada form.

### Jenis-Jenis Button
```html
<form>
    <!-- Submit Button - mengirim form -->
    <button type="submit">Kirim Data</button>

    <!-- Reset Button - reset form ke nilai awal -->
    <button type="reset">Reset Form</button>

    <!-- Button biasa - untuk JavaScript -->
    <button type="button" onclick="validasiData()">Validasi</button>
</form>
```

### Button dengan Konten HTML
```html
<button type="submit">
    <img src="icon-send.png" alt="" width="16" height="16">
    Kirim Pesan
</button>
```

---

## ✅ Validasi Form HTML5

### Atribut Validasi Built-in
```html
<form>
    <!-- Required - wajib diisi -->
    <input type="text" name="nama" required>

    <!-- Pattern - harus sesuai regex -->
    <input type="text" name="kode" pattern="[A-Z]{3}[0-9]{3}" title="Format: ABC123">

    <!-- Min/Max untuk number dan date -->
    <input type="number" name="umur" min="17" max="65">
    <input type="date" name="tanggal" min="2024-01-01" max="2024-12-31">

    <!-- Minlength/Maxlength untuk text -->
    <input type="password" name="password" minlength="8" maxlength="20">

    <!-- Step untuk number -->
    <input type="number" name="harga" step="0.01" min="0">
</form>
```

### Custom Validation Messages
```html
<input type="email"
       name="email"
       required
       title="Masukkan alamat email yang valid"
       oninvalid="this.setCustomValidity('Format email tidak benar')"
       onchange="this.setCustomValidity('')">
```

---

## 🎨 Styling Form dengan CSS

### CSS Dasar untuk Form
```css
/* Form container */
form {
    max-width: 600px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 8px;
    background-color: #f9f9f9;
}

/* Label styling */
label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #333;
}

/* Input styling */
input[type="text"],
input[type="email"],
input[type="password"],
input[type="number"],
input[type="date"],
textarea,
select {
    width: 100%;
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 16px;
    box-sizing: border-box;
}

/* Input focus state */
input:focus,
textarea:focus,
select:focus {
    border-color: #007bff;
    outline: none;
    box-shadow: 0 0 0 2px rgba(0, 123, 255, 0.25);
}

/* Button styling */
button {
    background-color: #007bff;
    color: white;
    padding: 12px 24px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    margin-right: 10px;
}

button:hover {
    background-color: #0056b3;
}

button[type="reset"] {
    background-color: #6c757d;
}

button[type="reset"]:hover {
    background-color: #545b62;
}

/* Fieldset styling */
fieldset {
    border: 1px solid #ddd;
    border-radius: 4px;
    padding: 15px;
    margin-bottom: 20px;
}

legend {
    font-weight: bold;
    padding: 0 10px;
}

/* Radio dan checkbox styling */
input[type="radio"],
input[type="checkbox"] {
    width: auto;
    margin-right: 8px;
    margin-bottom: 0;
}

/* Error state */
input:invalid {
    border-color: #dc3545;
}

input:invalid:focus {
    border-color: #dc3545;
    box-shadow: 0 0 0 2px rgba(220, 53, 69, 0.25);
}

/* Required field indicator */
input[required] + label::after,
label[required]::after {
    content: " *";
    color: #dc3545;
}
```

---

## 🚫 Kesalahan Umum dan Solusi

### 1. Label Tanpa For atau Tidak Terhubung
**❌ Kesalahan:**
```html
<label>Nama</label>
<input type="text" name="nama">
```

**✅ Perbaikan:**
```html
<label for="nama">Nama</label>
<input type="text" id="nama" name="nama">
```

### 2. Form Tanpa Action
**❌ Kesalahan:**
```html
<form>
    <input type="text" name="nama">
    <button type="submit">Submit</button>
</form>
```

**✅ Perbaikan:**
```html
<form action="/submit" method="post">
    <input type="text" name="nama">
    <button type="submit">Submit</button>
</form>
```

### 3. Input Tanpa Name
**❌ Kesalahan:**
```html
<input type="text" id="email">  <!-- Tidak ada name -->
```

**✅ Perbaikan:**
```html
<input type="text" id="email" name="email">
```

### 4. Radio Button Tanpa Name yang Sama
**❌ Kesalahan:**
```html
<input type="radio" name="gender1" value="pria">
<input type="radio" name="gender2" value="wanita">
```

**✅ Perbaikan:**
```html
<input type="radio" name="gender" value="pria">
<input type="radio" name="gender" value="wanita">
```

---

## 🔧 Troubleshooting

### Masalah Umum dan Solusi

| Masalah | Penyebab | Solusi |
|---------|----------|---------|
| Form tidak mengirim data | Tidak ada action atau method | Tambahkan `action` dan `method` |
| Label tidak clickable | Label tidak terhubung dengan input | Gunakan `for` dan `id` yang sama |
| Radio button bisa dipilih semua | Name berbeda untuk setiap radio | Gunakan `name` yang sama |
| Data tidak sampai server | Input tanpa `name` attribute | Tambahkan `name` pada semua input |
| File upload tidak berfungsi | Enctype salah | Gunakan `enctype="multipart/form-data"` |
| Validasi tidak bekerja | Browser lama atau novalidate | Check browser support dan hapus novalidate |

---

## 📱 Responsive Form Design

### Mobile-Friendly Form
```css
/* Mobile-first approach */
@media (max-width: 768px) {
    form {
        padding: 15px;
        margin: 10px;
    }

    input, textarea, select {
        font-size: 16px; /* Prevent zoom on iOS */
        padding: 12px;
    }

    button {
        width: 100%;
        padding: 15px;
        font-size: 18px;
    }

    /* Stack radio buttons vertically */
    input[type="radio"] + label {
        display: block;
        margin-bottom: 10px;
    }
}
```

---

## ♿ Aksesibilitas Form

### Prinsip Aksesibilitas
1. **Label yang Jelas** - Setiap input harus memiliki label
2. **Fokus yang Terlihat** - Focus state harus jelas
3. **Error yang Deskriptif** - Pesan error yang mudah dipahami
4. **Navigasi Keyboard** - Dapat diakses dengan Tab

### Implementasi Aksesibilitas
```html
<form>
    <!-- Required field dengan aria-required -->
    <label for="nama">Nama Lengkap *</label>
    <input type="text"
           id="nama"
           name="nama"
           aria-required="true"
           aria-describedby="nama-help">
    <small id="nama-help">Masukkan nama lengkap sesuai KTP</small>

    <!-- Error message dengan aria-describedby -->
    <label for="email">Email *</label>
    <input type="email"
           id="email"
           name="email"
           aria-required="true"
           aria-describedby="email-error"
           aria-invalid="false">
    <div id="email-error" role="alert" style="display: none;">
        Format email tidak valid
    </div>

    <!-- Fieldset untuk radio group -->
    <fieldset>
        <legend>Pilih jenis kelamin *</legend>
        <input type="radio" id="pria" name="gender" value="pria">
        <label for="pria">Pria</label>

        <input type="radio" id="wanita" name="gender" value="wanita">
        <label for="wanita">Wanita</label>
    </fieldset>
</form>
```

---

## 📝 Latihan

### Latihan 1: Form Kontak Sederhana
Buat form kontak dengan:
- Nama (required)
- Email (required, type email)
- Subjek (select dengan pilihan)
- Pesan (textarea)
- Submit button

### Latihan 2: Form Registrasi
Buat form registrasi dengan:
- Informasi pribadi (nama, tanggal lahir, gender)
- Informasi kontak (email, telepon)
- Password dengan konfirmasi
- Checkbox persetujuan

### Latihan 3: Form Survey
Buat form survey dengan:
- Rating menggunakan radio button
- Multiple choice dengan checkbox
- Dropdown untuk kategori
- Range slider untuk skala
- Textarea untuk saran

---

## 📋 Rangkuman

### Yang Telah Dipelajari:
1. **Tag `<form>`** - Container utama dengan action dan method
2. **Tag `<input>`** - Berbagai jenis input (text, email, password, number, date, dll.)
3. **Tag `<label>`** - Label untuk aksesibilitas
4. **Tag `<textarea>`** - Input teks panjang
5. **Tag `<select>` dan `<option>`** - Dropdown menu
6. **Tag `<fieldset>` dan `<legend>`** - Pengelompokan form
7. **Tag `<button>`** - Tombol aksi
8. **Validasi HTML5** - Validasi built-in browser
9. **Styling dan responsiveness** - CSS untuk form
10. **Aksesibilitas** - Form yang dapat diakses semua user

### Konsep Penting:
- Form adalah jembatan komunikasi antara user dan server
- Label penting untuk aksesibilitas dan UX
- Validasi HTML5 meningkatkan data quality
- Name attribute wajib untuk pengiriman data
- Responsive design crucial untuk mobile users

### Next Step:
Lanjut ke **Bab 6: Atribut Form HTML** untuk belajar lebih dalam tentang atribut-atribut form yang lebih advanced dan teknik validasi yang lebih kompleks.

---

**💡 Tips Pro:**
- Selalu test form di berbagai browser dan device
- Gunakan placeholder text yang membantu, bukan menggantikan label
- Implementasikan progressive enhancement
- Consider user experience dalam setiap keputusan design
- Test aksesibilitas dengan screen reader

**🔗 File Terkait:**
- [`contoh-kode/form-dasar-demo.html`](contoh-kode/form-dasar-demo.html) - Demo form basic
- [`contoh-kode/input-types-demo.html`](contoh-kode/input-types-demo.html) - Demo berbagai input types
- [`contoh-kode/form-validation-demo.html`](contoh-kode/form-validation-demo.html) - Demo validasi
- [`contoh-kode/form-styling-demo.html`](contoh-kode/form-styling-demo.html) - Demo styling form
- [`proyek-mini/form-pendaftaran.html`](proyek-mini/form-pendaftaran.html) - Proyek form pendaftaran lengkap
