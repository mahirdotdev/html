# Bab 9: Atribut HTML (ID dan Class)

## 🎯 Tujuan Pembelajaran
Setelah menyelesaikan bab ini, kalian akan mampu:
- Memahami perbedaan `id` dan `class` serta kapan menggunakannya
- Memberi penamaan yang rapi dan konsisten pada elemen
- Menggunakan `id` untuk anchor/link bagian halaman
- Menggunakan `class` untuk pengelompokan elemen yang berulang
- Menghindari kesalahan umum seperti duplikasi `id` dan class yang tidak bermakna
- Menyusun struktur halaman dengan sistem `id`/`class` yang siap untuk CSS dan JavaScript

## 📚 Konsep Dasar

### Apa Itu `id` dan `class`?
- `id`: penanda unik untuk SATU elemen. Analogi: NISN siswa — tidak boleh sama.
- `class`: label kelompok yang bisa dipakai oleh BANYAK elemen. Analogi: nama ekstrakurikuler — banyak siswa bisa tergabung di kelas/ekskul yang sama.

### Kenapa Penting?
- Memudahkan styling dengan CSS dan interaksi dengan JavaScript
- Menata struktur halaman agar rapi, mudah dipahami, dan terpelihara
- Membuat anchor (bookmark) yang bisa dilompati dari daftar isi

---

## 🆔 9.1 Atribut `id` — Penanda Unik

### Definisi & Tujuan
`id` memberikan identitas unik pada sebuah elemen. Cocok untuk:
- Target anchor (bookmark) seperti “kembali ke atas”
- Pengait spesifik untuk JavaScript
- Elemen yang benar-benar unik di halaman (misal: `main-nav`, `site-footer`)

### Syntax Dasar
```html
<h2 id="tentang">Tentang Sekolah</h2>
<a href="#tentang">Lompat ke bagian Tentang</a>
```

### Aturan & Best Practices
- Satu `id` hanya muncul sekali di satu halaman
- Nama `id` deskriptif dan konsisten (`kebab-case` disarankan: `main-header`, `menu-utama`)
- Hindari spasi dan karakter spesial (gunakan huruf, angka, tanda hubung)

### Kesalahan Umum
- Duplikasi `id` pada beberapa elemen
- Nama `id` generik/abstrak: `id="div1"` (tidak bermakna)

### Contoh Lengkap
- `contoh-kode/id-anchor-demo.html:1`

### Latihan Singkat
- Tambahkan `id` pada 3 heading lalu buat daftar isi yang menaut ke masing-masing bagian.

---

## 🏷️ 9.2 Atribut `class` — Kelompok Reusable

### Definisi & Tujuan
`class` digunakan untuk memberi label pada sekelompok elemen yang punya gaya/peran yang sama. Cocok untuk:
- Kartu artikel, item menu, tombol aksi, section sejenis
- Menentukan pola styling berulang

### Syntax Dasar
```html
<article class="card berita">
  <h3 class="card-title">Lomba Sains</h3>
  <p class="card-body">Informasi lomba…</p>
  <a class="card-link" href="#">Baca Selengkapnya</a>
</article>
```

### Aturan & Best Practices
- Gunakan nama yang deskriptif dan konsisten (`kebab-case`): `card`, `card-title`, `nav-item`
- Boleh lebih dari satu class pada elemen: `class="card highlight"`
- Hindari class yang tidak bermakna: `class="box1"`, `class="style-red"` (terlalu presentasional)
- Pikirkan modularitas: satu class = satu tujuan yang jelas

### Kesalahan Umum
- Menggunakan `class` untuk sesuatu yang unik (harusnya `id`)
- Nama class menggambarkan warna/posisi (presentasional) bukan peran (semantik)

### Contoh Lengkap
- `contoh-kode/class-grouping-demo.html:1`

### Latihan Singkat
- Buat 3 kartu artikel dengan class yang konsisten untuk judul, ringkas, dan tautan.

---

## ⚖️ ID vs Class — Kapan Memakai yang Mana?
- Pakai `id` jika elemen benar-benar unik dan perlu target spesifik (anchor/JS)
- Pakai `class` jika ingin mengelompokkan banyak elemen dengan tujuan yang sama
- Hindari berlebihan: jangan menaruh `id` pada semua elemen

Contoh kombinasi:
```html
<nav id="main-nav" class="nav">
  <a class="nav-item" href="#berita">Berita</a>
  <a class="nav-item" href="#agenda">Agenda</a>
</nav>
```

---

## 🧭 Best Practices Penamaan
- Konsisten: pilih satu gaya (kebab-case) dan gunakan di seluruh proyek
- Deskriptif: `article-card`, `site-header`, `main-footer`
- Hindari singkatan yang membingungkan
- Dokumentasikan pola penamaan di README proyek

---

## ❌ Kesalahan Umum & ✅ Perbaikan

### 1) `id` Ganda
**❌ Salah:**
```html
<h2 id="profil">Profil</h2>
<h2 id="profil">Ekstrakurikuler</h2>
```
**✅ Benar:**
```html
<h2 id="profil">Profil</h2>
<h2 id="ekskul">Ekstrakurikuler</h2>
```

### 2) Class Tidak Bermakna
**❌ Salah:**
```html
<div class="div1"></div>
<div class="div2"></div>
```
**✅ Benar:**
```html
<div class="card"></div>
<div class="card highlight"></div>
```

### 3) Nama Mengandung Spasi
**❌ Salah:** `id="main nav"`

**✅ Benar:** `id="main-nav"`

---

## 🔧 Troubleshooting
| Masalah | Penyebab | Solusi |
|--------|----------|--------|
| Anchor tidak bekerja | `id` tujuan tidak ada/typo | Samakan `href="#id"` dan `id` elemen |
| Styling tidak terpakai | Nama class salah/typo | Cocokkan ejaan di HTML dan CSS |
| Konflik interaksi | Duplikasi `id` | Pastikan setiap `id` unik |

---

## 📝 Latihan

### Latihan 1: Daftar Isi Anchor
Beri `id` pada tiga heading di halaman, lalu buat daftar isi di bagian atas yang menaut ke setiap heading.

### Latihan 2: Kartu Artikel Konsisten
Buat tiga kartu artikel dengan class yang konsisten: `card`, `card-title`, `card-body`, `card-link`.

### Latihan 3: Refactor Penamaan
Ubah class yang kurang bermakna (misal `box1`, `box2`) menjadi nama yang deskriptif.

Template tersedia di folder `latihan/`.

---

## 🏗️ Proyek Mini Bab 9
Buat halaman “Profil & Berita Sekolah” dengan sistem `id` dan `class` yang terorganisir:
- Navigasi atas dengan `id="main-nav"` dan item `class="nav-item"`
- Bagian `#profil`, `#berita`, `#kontak` sebagai anchor
- Kartu berita menggunakan class konsisten (`card`, `card-title`, `card-body`, `card-link`)
- Daftar isi di atas yang menaut ke setiap bagian

Mulai dari: `proyek-mini/profil-berita-sekolah.html`.

---

## 📋 Rangkuman

### Yang Telah Dipelajari
1. Perbedaan peran `id` (unik) dan `class` (kelompok)
2. Praktik penamaan yang konsisten dan deskriptif
3. Penggunaan `id` untuk anchor dan `class` untuk pola berulang
4. Kesalahan umum (duplikasi `id`, class tidak bermakna) dan cara memperbaikinya

### Next Step
Dengan `id` dan `class` yang rapi, halaman siap untuk styling CSS dan interaksi JavaScript.

---

**💡 Tips Pro:**
- Dokumentasikan aturan penamaan di awal proyek
- Uji anchor secara manual: klik tautan dan lihat apakah halaman melompat ke bagian yang tepat
- Gunakan validator HTML untuk mendeteksi duplikasi `id`

**🔗 File Terkait:**
- `contoh-kode/id-anchor-demo.html:1`
- `contoh-kode/class-grouping-demo.html:1`
- `proyek-mini/profil-berita-sekolah.html:1`
- `latihan/latihan-bab-9-1.html:1`
- `latihan/latihan-bab-9-2.html:1`
- `latihan/latihan-bab-9-3.html:1`
