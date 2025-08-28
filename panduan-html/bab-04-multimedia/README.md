# Bab 4: Multimedia dalam HTML

## 🎯 Tujuan Pembelajaran
Setelah menyelesaikan bab ini, kalian akan mampu:
- Memahami konsep multimedia dalam web
- Menggunakan tag `<img>` untuk menampilkan gambar
- Menggunakan tag `<audio>` untuk audio
- Menggunakan tag `<video>` untuk video
- Menggunakan tag `<iframe>` untuk konten eksternal
- Mengoptimalkan multimedia untuk web
- Menerapkan prinsip aksesibilitas pada multimedia

## 📚 Konsep Dasar

### Apa itu Multimedia dalam Web?
**Multimedia** adalah kombinasi dari berbagai jenis konten seperti teks, gambar, audio, video, dan animasi dalam satu halaman web.

**Analogi Sederhana:**
Bayangkan halaman web seperti majalah digital. Seperti majalah yang memiliki foto, ilustrasi, dan kadang QR code untuk video, halaman web juga bisa memiliki berbagai jenis media untuk membuat konten lebih menarik dan informatif.

### Kenapa Multimedia Penting?
1. **Daya Tarik Visual** - Membuat halaman lebih menarik
2. **Komunikasi Efektif** - Gambar bisa menyampaikan informasi lebih cepat
3. **Pengalaman Pengguna** - Membuat interaksi lebih engaging
4. **Aksesibilitas** - Audio untuk yang sulit membaca, subtitle untuk yang sulit mendengar

---

## 🖼️ Tag `<img>` - Menampilkan Gambar

### Definisi dan Tujuan
Tag `<img>` digunakan untuk menampilkan gambar di halaman web. Tag ini adalah **self-closing tag** (tidak memerlukan tag penutup).

### Syntax Dasar
```html
<img src="path/gambar.jpg" alt="Deskripsi gambar">
```

### Atribut Wajib
| Atribut | Tujuan | Contoh |
|---------|--------|---------|
| `src` | Menentukan lokasi file gambar | `src="gambar/logo.png"` |
| `alt` | Teks alternatif untuk aksesibilitas | `alt="Logo perusahaan"` |

### Atribut Opsional
| Atribut | Tujuan | Contoh |
|---------|--------|---------|
| `width` | Lebar gambar (piksel) | `width="300"` |
| `height` | Tinggi gambar (piksel) | `height="200"` |
| `title` | Tooltip saat hover | `title="Klik untuk memperbesar"` |
| `loading` | Strategi loading gambar | `loading="lazy"` |

### Contoh Lengkap
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Demo Gambar</title>
</head>
<body>
    <h1>Galeri Foto Sekolah</h1>

    <!-- Gambar dengan semua atribut -->
    <img src="https://via.placeholder.com/400x300/4CAF50/white?text=Gedung+Sekolah"
         alt="Gedung utama sekolah dengan lapangan hijau di depannya"
         width="400"
         height="300"
         title="Gedung Utama SMA"
         loading="lazy">

    <h2>Kegiatan Ekstrakurikuler</h2>

    <!-- Gambar responsif -->
    <img src="https://via.placeholder.com/500x300/2196F3/white?text=Basket"
         alt="Siswa bermain basket di lapangan sekolah"
         style="max-width: 100%; height: auto;"
         loading="lazy">

    <!-- Gambar dengan link -->
    <a href="galeri-lengkap.html">
        <img src="https://via.placeholder.com/200x150/FF9800/white?text=Lihat+Semua"
             alt="Tombol untuk melihat galeri lengkap"
             width="200"
             height="150">
    </a>
</body>
</html>
```

### Format Gambar yang Didukung
| Format | Ekstensi | Terbaik Untuk |
|--------|----------|---------------|
| **JPEG/JPG** | .jpg, .jpeg | Foto dengan banyak warna |
| **PNG** | .png | Gambar dengan transparansi |
| **GIF** | .gif | Animasi sederhana |
| **SVG** | .svg | Logo dan ikon |
| **WebP** | .webp | Kompresi modern (ukuran kecil) |

---

## 🎵 Tag `<audio>` - Audio Player

### Definisi dan Tujuan
Tag `<audio>` digunakan untuk memutar file audio di halaman web dengan kontrol yang built-in.

### Syntax Dasar
```html
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    <source src="audio.ogg" type="audio/ogg">
    Peramban Anda tidak mendukung audio HTML5.
</audio>
```

### Atribut Audio
| Atribut | Tujuan | Nilai |
|---------|--------|-------|
| `controls` | Menampilkan kontrol pemutaran | (boolean) |
| `autoplay` | Otomatis putar | (boolean) |
| `loop` | Putar berulang | (boolean) |
| `muted` | Mulai dalam kondisi mute | (boolean) |
| `preload` | Strategi loading | `none`, `metadata`, `auto` |

### Contoh Lengkap
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Demo Audio</title>
</head>
<body>
    <h1>Musik Sekolah</h1>

    <!-- Audio dengan kontrol lengkap -->
    <h2>Mars Sekolah</h2>
    <audio controls preload="metadata">
        <source src="mars-sekolah.mp3" type="audio/mpeg">
        <source src="mars-sekolah.ogg" type="audio/ogg">
        <p>Peramban Anda tidak mendukung audio HTML5.
           <a href="mars-sekolah.mp3">Download audio</a>
        </p>
    </audio>

    <!-- Audio background (gunakan dengan hati-hati) -->
    <h2>Musik Latar</h2>
    <audio controls loop muted>
        <source src="background-music.mp3" type="audio/mpeg">
        Peramban tidak mendukung audio.
    </audio>

    <!-- Multiple audio sources -->
    <h2>Rekaman Pengumuman</h2>
    <audio controls>
        <source src="pengumuman.m4a" type="audio/mp4">
        <source src="pengumuman.mp3" type="audio/mpeg">
        <source src="pengumuman.wav" type="audio/wav">
        <p>Tidak dapat memutar audio. Silakan update peramban Anda.</p>
    </audio>
</body>
</html>
```

### Format Audio yang Didukung
| Format | Ekstensi | Kompatibilitas |
|--------|----------|----------------|
| **MP3** | .mp3 | Universal |
| **OGG** | .ogg | Firefox, Chrome |
| **WAV** | .wav | Kualitas tinggi |
| **M4A/AAC** | .m4a | Safari, Chrome |

---

## 🎥 Tag `<video>` - Video Player

### Definisi dan Tujuan
Tag `<video>` digunakan untuk memutar video di halaman web dengan kontrol built-in dan dukungan subtitle.

### Syntax Dasar
```html
<video controls width="640" height="360">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    <track src="subtitle.vtt" kind="subtitles" srclang="id" label="Bahasa Indonesia">
    Peramban Anda tidak mendukung video HTML5.
</video>
```

### Atribut Video
| Atribut | Tujuan | Contoh |
|---------|--------|---------|
| `controls` | Kontrol pemutaran | (boolean) |
| `width` | Lebar video | `width="640"` |
| `height` | Tinggi video | `height="360"` |
| `autoplay` | Otomatis putar | (boolean) |
| `loop` | Putar berulang | (boolean) |
| `muted` | Mulai muted | (boolean) |
| `poster` | Gambar preview | `poster="thumbnail.jpg"` |
| `preload` | Strategi loading | `none`, `metadata`, `auto` |

### Contoh Lengkap
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Demo Video</title>
    <style>
        .video-container {
            max-width: 100%;
            margin: 20px 0;
        }
        .video-container video {
            width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <h1>Video Pembelajaran</h1>

    <!-- Video dengan poster dan subtitle -->
    <div class="video-container">
        <h2>Orientasi Siswa Baru</h2>
        <video controls
               width="640"
               height="360"
               poster="https://via.placeholder.com/640x360/E91E63/white?text=Video+Orientasi"
               preload="metadata">
            <source src="orientasi.mp4" type="video/mp4">
            <source src="orientasi.webm" type="video/webm">
            <track src="subtitle-id.vtt"
                   kind="subtitles"
                   srclang="id"
                   label="Bahasa Indonesia"
                   default>
            <track src="subtitle-en.vtt"
                   kind="subtitles"
                   srclang="en"
                   label="English">
            <p>Peramban Anda tidak mendukung video HTML5.
               <a href="orientasi.mp4">Download video</a>
            </p>
        </video>
    </div>

    <!-- Video responsif -->
    <div class="video-container">
        <h2>Kegiatan Ekstrakurikuler</h2>
        <video controls muted>
            <source src="https://sample-videos.com/zip/10/mp4/480/SampleVideo_480x270_1mb.mp4" type="video/mp4">
            Video tidak dapat dimuat.
        </video>
    </div>

    <!-- Video autoplay (hati-hati dengan kebijakan browser) -->
    <div class="video-container">
        <h2>Video Pendek</h2>
        <video autoplay muted loop width="300" height="200">
            <source src="intro-short.mp4" type="video/mp4">
            Browser tidak mendukung video.
        </video>
    </div>
</body>
</html>
```

### Format Video yang Didukung
| Format | Ekstensi | Kompatibilitas |
|--------|----------|----------------|
| **MP4** | .mp4 | Universal |
| **WebM** | .webm | Chrome, Firefox |
| **OGV** | .ogv | Firefox, Chrome |

---

## 🌐 Tag `<iframe>` - Konten Eksternal

### Definisi dan Tujuan
Tag `<iframe>` (inline frame) digunakan untuk menampilkan halaman web lain di dalam halaman web kita.

**Analogi Sederhana:**
Iframe seperti jendela kecil di rumah yang memungkinkan kita melihat pemandangan luar tanpa harus keluar rumah.

### Syntax Dasar
```html
<iframe src="https://www.example.com"
        width="600"
        height="400"
        title="Deskripsi konten iframe">
</iframe>
```

### Atribut Iframe
| Atribut | Tujuan | Contoh |
|---------|--------|---------|
| `src` | URL konten yang dimuat | `src="https://maps.google.com"` |
| `width` | Lebar iframe | `width="600"` |
| `height` | Tinggi iframe | `height="400"` |
| `title` | Deskripsi untuk aksesibilitas | `title="Peta lokasi sekolah"` |
| `allowfullscreen` | Izinkan fullscreen | (boolean) |
| `loading` | Strategi loading | `loading="lazy"` |
| `sandbox` | Pembatasan keamanan | `sandbox="allow-scripts"` |

### Contoh Penggunaan Umum
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Demo Iframe</title>
    <style>
        .iframe-container {
            margin: 20px 0;
            border: 1px solid #ddd;
            border-radius: 8px;
            overflow: hidden;
        }

        .responsive-iframe {
            width: 100%;
            height: 300px;
            border: none;
        }
    </style>
</head>
<body>
    <h1>Konten Eksternal</h1>

    <!-- Google Maps -->
    <div class="iframe-container">
        <h2>Lokasi Sekolah</h2>
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3966.666!2d106.845!3d-6.208!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNsKwMTInMjguOCJTIDEwNsKwNTAnNDIuMCJF!5e0!3m2!1sen!2sid!4v1234567890"
                class="responsive-iframe"
                title="Lokasi SMA Negeri 1 Jakarta"
                loading="lazy"
                allowfullscreen>
        </iframe>
    </div>

    <!-- YouTube Video -->
    <div class="iframe-container">
        <h2>Video Pembelajaran</h2>
        <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ?rel=0&modestbranding=1"
                class="responsive-iframe"
                title="Video pembelajaran HTML"
                loading="lazy"
                allowfullscreen>
        </iframe>
    </div>

    <!-- Form Eksternal -->
    <div class="iframe-container">
        <h2>Formulir Pendaftaran</h2>
        <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSc_example/viewform?embedded=true"
                class="responsive-iframe"
                title="Form pendaftaran ekstrakurikuler"
                loading="lazy">
            Memuat...
        </iframe>
    </div>

    <!-- Konten Lokal -->
    <div class="iframe-container">
        <h2>Halaman Profil</h2>
        <iframe src="../bab-02-elemen-tag-dasar/proyek-mini/proyek-profil-lengkap.html"
                class="responsive-iframe"
                title="Halaman profil siswa"
                loading="lazy">
        </iframe>
    </div>
</body>
</html>
```

---

## ⚡ Optimasi Multimedia

### 1. Optimasi Gambar
```html
<!-- Lazy loading untuk performa -->
<img src="gambar-besar.jpg"
     alt="Deskripsi"
     loading="lazy"
     width="800"
     height="600">

<!-- Responsive images -->
<img src="gambar-small.jpg"
     srcset="gambar-small.jpg 300w,
             gambar-medium.jpg 600w,
             gambar-large.jpg 1200w"
     sizes="(max-width: 300px) 100vw,
            (max-width: 600px) 50vw,
            25vw"
     alt="Gambar responsif">
```

### 2. Optimasi Video
```html
<!-- Preload metadata saja -->
<video controls preload="metadata" poster="thumbnail.jpg">
    <source src="video-small.mp4" type="video/mp4" media="(max-width: 600px)">
    <source src="video-large.mp4" type="video/mp4">
</video>
```

### 3. Optimasi Iframe
```html
<!-- Lazy loading iframe -->
<iframe src="https://example.com"
        loading="lazy"
        width="600"
        height="400">
</iframe>
```

---

## ♿ Aksesibilitas Multimedia

### Prinsip Aksesibilitas
1. **Alt text yang deskriptif** untuk gambar
2. **Captions/subtitle** untuk video
3. **Transkrip** untuk audio
4. **Kontrol keyboard** yang dapat diakses

### Contoh Implementasi
```html
<!-- Gambar dengan alt text yang baik -->
<img src="grafik-nilai.png"
     alt="Grafik batang menunjukkan peningkatan nilai rata-rata dari 75 menjadi 85 dalam 3 bulan">

<!-- Video dengan subtitle -->
<video controls>
    <source src="pembelajaran.mp4" type="video/mp4">
    <track src="subtitle-id.vtt"
           kind="captions"
           srclang="id"
           label="Bahasa Indonesia"
           default>
    <track src="audio-description.vtt"
           kind="descriptions"
           srclang="id"
           label="Audio Description">
</video>

<!-- Audio dengan transkrip -->
<audio controls>
    <source src="ceramah.mp3" type="audio/mpeg">
</audio>
<details>
    <summary>Transkrip Audio</summary>
    <p>Selamat pagi siswa-siswi sekalian...</p>
</details>
```

---

## 🚫 Kesalahan Umum dan Solusi

### 1. Gambar Tidak Muncul
**❌ Kesalahan:**
```html
<img src="gambar.jpg">  <!-- Tidak ada alt -->
<img alt="Gambar">      <!-- Tidak ada src -->
```

**✅ Perbaikan:**
```html
<img src="gambar.jpg" alt="Deskripsi gambar">
```

### 2. Video Tidak Dapat Diputar
**❌ Kesalahan:**
```html
<video>
    <source src="video.avi" type="video/avi">  <!-- Format tidak didukung -->
</video>
```

**✅ Perbaikan:**
```html
<video controls>
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Browser tidak mendukung video HTML5.
</video>
```

### 3. Iframe Keamanan
**❌ Kesalahan:**
```html
<iframe src="http://untrusted-site.com"></iframe>  <!-- Tidak aman -->
```

**✅ Perbaikan:**
```html
<iframe src="https://trusted-site.com"
        title="Deskripsi konten"
        sandbox="allow-scripts allow-same-origin">
</iframe>
```

### 4. Multimedia Terlalu Besar
**❌ Kesalahan:**
```html
<img src="foto-10mb.jpg">  <!-- File terlalu besar -->
```

**✅ Perbaikan:**
```html
<img src="foto-optimized.jpg"
     loading="lazy"
     alt="Foto sekolah"
     width="800"
     height="600">
```

---

## 🔧 Troubleshooting

### Masalah Umum dan Solusi

| Masalah | Penyebab | Solusi |
|---------|----------|---------|
| Gambar tidak muncul | Path salah atau file tidak ada | Periksa path dan keberadaan file |
| Video lag/lambat | File terlalu besar | Kompres video atau gunakan format yang lebih efisien |
| Audio tidak terdengar | Browser di-mute atau file corrupt | Periksa volume browser dan integritas file |
| Iframe tidak muncul | X-Frame-Options blocking | Gunakan sumber yang mengizinkan embedding |
| Multimedia tidak responsif | Ukuran fixed | Gunakan CSS untuk membuat responsif |

---

## 📝 Latihan

### Latihan 1: Galeri Foto
Buat halaman galeri foto sekolah dengan:
- 6 gambar placeholder
- Alt text yang deskriptif
- Lazy loading
- Gambar dalam grid 3x2

### Latihan 2: Media Center
Buat halaman yang berisi:
- 1 video dengan kontrol
- 1 audio dengan kontrol
- Poster untuk video
- Fallback text untuk browser lama

### Latihan 3: Dashboard Konten
Buat dashboard yang menampilkan:
- Iframe Google Maps
- Iframe YouTube video
- Iframe form Google Forms
- Semua dengan lazy loading

---

## 📋 Rangkuman

### Yang Telah Dipelajari:
1. **Tag `<img>`** - Menampilkan gambar dengan berbagai format dan atribut
2. **Tag `<audio>`** - Memutar file audio dengan kontrol built-in
3. **Tag `<video>`** - Memutar video dengan dukungan subtitle dan poster
4. **Tag `<iframe>`** - Menampilkan konten eksternal dalam halaman
5. **Optimasi multimedia** - Teknik untuk meningkatkan performa
6. **Aksesibilitas** - Membuat multimedia dapat diakses semua pengguna

### Konsep Penting:
- Selalu gunakan alt text untuk gambar
- Sediakan multiple format untuk kompatibilitas
- Gunakan lazy loading untuk performa
- Perhatikan ukuran file untuk loading cepat
- Implementasikan aksesibilitas dengan subtitle dan transkrip

### Next Step:
Lanjut ke **Bab 5: Form dan Input HTML** untuk belajar membuat form interaktif yang memungkinkan pengguna memasukkan data.

---

**💡 Tips Pro:**
- Kompres gambar sebelum diupload (gunakan tools seperti TinyPNG)
- Gunakan CDN untuk loading multimedia yang lebih cepat
- Test multimedia di berbagai browser dan device
- Selalu sediakan fallback untuk browser lama
- Perhatikan hak cipta saat menggunakan multimedia

**🔗 File Terkait:**
- [`contoh-kode/gambar-demo.html`](contoh-kode/gambar-demo.html) - Demo lengkap tag img
- [`contoh-kode/audio-demo.html`](contoh-kode/audio-demo.html) - Demo audio player
- [`contoh-kode/video-demo.html`](contoh-kode/video-demo.html) - Demo video player
- [`contoh-kode/iframe-demo.html`](contoh-kode/iframe-demo.html) - Demo iframe
- [`proyek-mini/galeri-multimedia.html`](proyek-mini/galeri-multimedia.html) - Proyek mini galeri
