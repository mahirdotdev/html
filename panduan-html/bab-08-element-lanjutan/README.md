# Bab 8: Elemen Lanjutan & Praktik Modern

## 🎯 Tujuan Pembelajaran
Setelah menyelesaikan bab ini, kalian akan mampu:
- Memutar audio/video dengan kontrol yang tepat dan aksesibilitas dasar
- Membangun form yang nyaman digunakan dan tervalidasi
- Menyusun layout semantic HTML5 yang rapi dan mudah dinavigasi
- Menggunakan elemen formatting teks lanjutan (`mark`, `time`, `small`, dll.)
- Menyematkan konten eksternal (YouTube, Maps, PDF) dengan aman
- Mengoptimalkan bagian `<head>` untuk SEO dan social preview
- Meningkatkan aksesibilitas dengan atribut ARIA seperlunya
- Menyediakan tampilan responsif (viewport, gambar `srcset`, tabel dapat digeser)
- Membuat tautan aksi (bookmark, email, telepon) secara aman
- Mengenali elemen deprecated dan menggantinya dengan praktik modern

## 📚 Konsep Dasar

### Mengapa Elemen “Lanjutan” Ini Penting?
Seperti upgrade fasilitas sekolah (proyektor, speaker, papan pengumuman digital), elemen lanjutan HTML meningkatkan pengalaman belajar pengguna situs: konten jadi hidup (audio/video), mudah diisi (form), enak dinavigasi (semantic + aksesibilitas), dan nyaman di HP (responsif). Semua ini membuat halaman terasa profesional dan siap dipublikasikan.

### Cara Belajar di Bab Ini
Kita pakai pola yang sama setiap topik:
1) Definisi dan tujuan, 2) Syntax dasar, 3) Atribut penting, 4) Contoh, 5) Best practices, 6) Kesalahan umum, 7) Latihan singkat.
File contoh bisa langsung dicoba di folder `contoh-kode/`.

---

## 🎵 8.1 Audio & 🎥 Video

### Definisi & Tujuan
`<audio>` dan `<video>` adalah “pemutar” bawaan browser. Cocok untuk podcast sekolah, teaser event, atau dokumentasi lomba.

### Syntax Dasar
```html
<audio controls preload="metadata">
  <source src="lagu.mp3" type="audio/mpeg">
  <source src="lagu.ogg" type="audio/ogg">
  Peramban tidak mendukung audio. <a href="lagu.mp3">Unduh audio</a>
</audio>

<video controls poster="poster.jpg">
  <source src="video.mp4" type="video/mp4">
  <track src="subtitle-id.vtt" kind="subtitles" srclang="id" label="Indonesia" default>
  Peramban tidak mendukung video.
</video>
```

### Atribut Penting
- `controls`, `autoplay` (+ `muted` untuk mobile), `loop`, `preload`, `poster` (video), `<track>` untuk subtitle.

### Contoh Penggunaan
- Buka: `contoh-kode/audio-video-advanced.html:1`

### Best Practices
- Sediakan beberapa format (mp4/webm untuk video) dan caption/transkrip.
- Gunakan `preload="metadata"` dan kompres file.

### Kesalahan Umum
- Autoplay tanpa `muted` di ponsel; tidak menyediakan fallback/track.

### Latihan Singkat
- Tambahkan audio lalu video dengan poster dan subtitle.

---

## 🧾 8.2 Form & Input Types

### Definisi & Tujuan
Form adalah lembar pendaftaran digital. `input type` yang tepat membantu validasi otomatis.

### Syntax Dasar
```html
<form action="/daftar" method="post">
  <label for="nama">Nama</label>
  <input id="nama" name="nama" type="text" required>
  <label for="email">Email</label>
  <input id="email" name="email" type="email" placeholder="nama@sekolah.id" required>
  <button type="submit">Kirim</button>
</form>
```

### Atribut Penting
- `required`, `pattern`, `min/max/step`, `placeholder`, `autocomplete`, `aria-*`.

### Contoh Penggunaan
- Buka: `contoh-kode/form-interaktif-advanced.html:1`

### Best Practices
- Selalu hubungkan `label` ↔ `id`, dan pastikan `name` terisi.
- Mulai dari validasi bawaan browser.

### Kesalahan Umum
- Lupa `name`, label tidak terhubung, validasi tidak jelas.

### Latihan Singkat
- Form dasar → tambah validasi → tambah upload file.

---

## 🏷️ 8.3 Semantic HTML5 Elements (Layout Modern)

### Definisi & Tujuan
Elemen semantic memberi makna pada struktur: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`.

### Syntax Dasar
```html
<header>Judul Situs</header>
<nav aria-label="Navigasi utama">…</nav>
<main>
  <article>
    <h1>Judul</h1>
    <section><h2>Subtopik</h2><p>...</p></section>
  </article>
  <aside>Info terkait</aside>
  </main>
<footer>Hak Cipta</footer>
```

### Best Practices
- Satu `<main>` per halaman, setiap `<section>` punya heading, jangan nested berlebihan.

### Contoh & Latihan
- Contoh: `contoh-kode/layout-semantic-modern.html:1`
- Latihan: refactor halaman div-only menjadi semantic.

---

## ✍️ 8.4 Advanced Text Formatting (mark, time, small, dll.)

### Definisi & Tujuan
Elemen inline untuk makna: highlight, waktu terstruktur, catatan kecil, singkatan, dan konteks teknis.

### Syntax Dasar
```html
Hasil: <mark>biologi</mark>
Ujian: <time datetime="2025-09-10T07:30">10 Sept 2025 07:30</time>
<small>*Jadwal dapat berubah</small>
<abbr title="Kegiatan Belajar Mengajar">KBM</abbr>
```

### Best Practices
- `time` pakai `datetime` ISO, gunakan `<strong>/<em>` untuk penekanan makna.

### Contoh & Latihan
- Contoh: `contoh-kode/text-formatting-advanced.html:1`
- Latihan: sorot istilah → buat `abbr` → pasang `time`.

---

## 🌐 8.5 Embedded Content (Iframe & Object)

### Definisi & Tujuan
Menyematkan konten eksternal seperti YouTube, Google Maps, dan PDF.

### Syntax Dasar
```html
<iframe src="..." title="..." loading="lazy" sandbox="allow-scripts allow-same-origin"></iframe>
<object data="dokumen.pdf" type="application/pdf" width="600" height="400"></object>
```

### Best Practices
- Selalu beri `title`, batasi izin dengan `sandbox`, buat responsif dengan wrapper.

### Contoh & Latihan
- Contoh: `contoh-kode/embedded-iframe-object.html:1`
- Latihan: sematkan peta → atur parameter → responsifkan.

---

## 🧠 8.6 Metadata di Head (Optimasi)

### Definisi & Tujuan
Mengatur identitas halaman untuk browser, mesin pencari, dan social preview.

### Yang Harus Ada
`<title>`, meta `description`, `charset`, `viewport`, Open Graph (`og:title`, `og:description`, `og:image`), `link rel="icon"`.

### Contoh & Tips
- Contoh: `contoh-kode/head-optimization.html:1`
- Letakkan meta penting di awal. Uji preview share.

### Kesalahan Umum
- Meta duplikat, viewport salah, deskripsi tidak spesifik.

---

## ♿ 8.7 Accessibility Features (ARIA & Struktur Semantik)

### Definisi & Tujuan
Membuat situs nyaman dipakai semua orang: jelas untuk pembaca layar dan bisa dinavigasi dengan keyboard.

### Praktik Utama
- Pakai elemen semantic dahulu; ARIA jika perlu. Fokus harus terlihat.
- ARIA umum: `aria-label`, `aria-expanded`, `aria-controls`, `role`.

### Contoh & Latihan
- Contoh: `contoh-kode/aksesibilitas-aria.html:1`
- Latihan: tambahkan skip link dan label deskriptif pada form.

---

## 📱 8.8 Responsive Elements (Viewport & Media Queries)

### Definisi & Tujuan
Tampilan adaptif di berbagai perangkat.

### Komponen HTML Penting
`<meta name="viewport" content="width=device-width, initial-scale=1">`, `srcset`, `sizes`, `loading="lazy"`.

### Contoh & Latihan
- Contoh: `contoh-kode/responsive-elements.html:1`
- Latihan: buat hero image responsif dan tabel yang dapat digeser.

---

## 🔗 8.9 Advanced Linking (Bookmark, Email, Phone)

### Definisi & Tujuan
Membuat tautan yang memicu aksi: lompat ke bagian (bookmark), kirim email, atau menelepon.

### Syntax Dasar
`href="#id"`, `mailto:osis@sekolah.id?subject=...`, `tel:+6221123456`.

### Contoh & Latihan
- Contoh: `contoh-kode/advanced-linking.html:1`
- Latihan: daftar isi dengan anchor + tombol email siap kirim.

---

## ♻️ 8.10 Deprecated vs Modern Elements

### Definisi & Tujuan
Kenali elemen lama (mis. `center`, `font`, `big`, `strike`) dan ganti dengan semantic + CSS.

### Contoh Refactor
Lihat: `contoh-kode/modernisasi-deprecated.html:1`

### Best Practices
- Hindari atribut presentasional lama; validasi dengan W3C Validator.

---

---

## 🏗️ Proyek Mini Bab 8
Bangun halaman “Kampanye Acara Sekolah” dengan:
- Layout semantic lengkap (header, nav, main, section, article, aside, footer)
- Video teaser (poster + subtitle), form pendaftaran valid
- Peta lokasi responsif (iframe + sandbox), head teroptimasi
- Aksesibilitas dasar (skip link, label jelas, fokus terlihat)
- Responsif (viewport + `srcset`)

Mulai dari: `proyek-mini/kampanye-acara-sekolah.html:1`

---

## 📝 Latihan Bab 8
- Latihan 1: sematkan audio & video dengan fallback — `latihan/latihan-bab-8-1.html:1`
- Latihan 2: refactor halaman jadi semantic + aksesibel — `latihan/latihan-bab-8-2.html:1`
- Latihan 3: gambar responsif dengan `srcset` + `sizes` — `latihan/latihan-bab-8-3.html:1`

---

## 📋 Rangkuman

### Yang Telah Dipelajari
1. Media (audio/video) dengan kontrol, format, dan subtitle
2. Form dan input types dengan validasi bawaan
3. Layout semantic HTML5 untuk struktur bermakna
4. Formatting teks lanjutan (`mark`, `time`, `small`, `abbr`, dll.)
5. Embedded content (iframe/object) yang aman dan responsif
6. Optimasi `<head>` untuk SEO dan social preview
7. Aksesibilitas dasar (ARIA seperlunya, fokus terlihat)
8. Responsif (viewport, `srcset`, tabel geser)
9. Advanced linking (bookmark, email, tel)
10. Migrasi dari elemen deprecated ke praktik modern

### Next Step
Lanjut ke **Bab 9: Atribut HTML (ID dan Class)** untuk dasar styling CSS dan interaksi JavaScript.

---

**💡 Tips Pro:**
- Uji media dan embed di beberapa perangkat/browser
- Tulis heading berurutan dan landmark yang jelas
- Pakai validator HTML dan alat cek aksesibilitas sederhana (keyboard-only)
- Kompres gambar/video, aktifkan lazy loading saat tepat
- Siapkan metadata head yang konsisten dan spesifik

**🔗 File Terkait:**
- `contoh-kode/audio-video-advanced.html:1`
- `contoh-kode/form-interaktif-advanced.html:1`
- `contoh-kode/layout-semantic-modern.html:1`
- `contoh-kode/text-formatting-advanced.html:1`
- `contoh-kode/embedded-iframe-object.html:1`
- `contoh-kode/head-optimization.html:1`
- `contoh-kode/aksesibilitas-aria.html:1`
- `contoh-kode/responsive-elements.html:1`
- `contoh-kode/advanced-linking.html:1`
- `contoh-kode/modernisasi-deprecated.html:1`
- `proyek-mini/kampanye-acara-sekolah.html:1`
