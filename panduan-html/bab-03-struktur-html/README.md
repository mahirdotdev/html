# 📚 BAB 3: STRUKTUR DASAR DOKUMEN HTML

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan bab ini, siswa akan mampu:
- Memahami anatomi lengkap dokumen HTML
- Menggunakan tag head dengan berbagai meta informasi
- Mengoptimalkan tag body untuk konten yang accessible
- Menambahkan favicon untuk branding website
- Menggunakan meta tags untuk SEO dan user experience
- Memahami pentingnya viewport dan character encoding
- Membuat template HTML yang professional dan standard

---

## 📖 3.1 Struktur Dasar File HTML

### 🏗️ Anatomi Dokumen HTML

Setiap dokumen HTML memiliki struktur dasar yang **wajib** ada. Mari kita pahami setiap komponennya:

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <!-- Meta informasi dan pengaturan -->
</head>
<body>
    <!-- Konten yang terlihat -->
</body>
</html>
```

### 🧩 Analogi Sederhana: HTML sebagai Rumah

Bayangkan dokumen HTML seperti **rumah**:

```
🏠 RUMAH (DOKUMEN HTML)
┌─────────────────────────────────────────┐
│ 📋 DOKUMEN IZIN BANGUNAN (DOCTYPE)      │
├─────────────────────────────────────────┤
│ 🏠 STRUKTUR RUMAH (html lang)          │
│ ┌─────────────────────────────────────┐ │
│ │ 🧠 RUANG TEKNIS (head)             │ │
│ │   - Instalasi listrik              │ │
│ │   - Sistem air                     │ │
│ │   - Sertifikat & dokumen           │ │
│ └─────────────────────────────────────┘ │
│ ┌─────────────────────────────────────┐ │
│ │ 🏡 RUANG TAMU (body)               │ │
│ │   - Furniture & dekorasi           │ │
│ │   - Ruang yang terlihat tamu       │ │
│ │   - Aktivitas sehari-hari          │ │
│ └─────────────────────────────────────┘ │
└─────────────────────────────────────────┘
```

### 🔍 Penjelasan Setiap Komponen

#### 1. **DOCTYPE Declaration**
```html
<!DOCTYPE html>
```
- **Fungsi**: Memberitahu browser bahwa ini adalah dokumen HTML5
- **Posisi**: **Harus** di baris pertama
- **Case**: Tidak case-sensitive, tapi konvensi menggunakan uppercase
- **Wajib**: Ya, tanpa DOCTYPE browser akan masuk "quirks mode"

#### 2. **HTML Root Element**
```html
<html lang="id">
```
- **Fungsi**: Container utama untuk semua elemen HTML
- **Atribut lang**: Menentukan bahasa dokumen
  - `"id"` untuk Bahasa Indonesia
  - `"en"` untuk English
  - `"ja"` untuk Japanese
- **SEO Impact**: Search engines menggunakan ini untuk indexing
- **Accessibility**: Screen readers menggunakan untuk pronunciation

#### 3. **Head Section**
```html
<head>
    <!-- Meta informasi tidak terlihat user -->
</head>
```
- **Fungsi**: Metadata dan pengaturan dokumen
- **Tidak terlihat**: Konten head tidak muncul di browser
- **Penting untuk**: SEO, performance, user experience

#### 4. **Body Section**
```html
<body>
    <!-- Konten yang terlihat user -->
</body>
```
- **Fungsi**: Konten yang akan ditampilkan browser
- **Terlihat**: Semua konten body akan muncul di browser
- **Interactive**: Tempat semua elemen interaktif

### 📝 Template Dasar HTML5

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Judul Halaman</title>
</head>
<body>
    <h1>Hello World!</h1>
    <p>Ini adalah halaman HTML dasar.</p>
</body>
</html>
```

### 🔧 Validasi Struktur HTML

#### Tools untuk Validasi:
1. **W3C Markup Validator** - https://validator.w3.org
2. **VS Code Extensions** - HTMLHint, HTML CSS Support
3. **Browser DevTools** - Console untuk error checking

#### Error Umum:
```html
<!-- ❌ Missing DOCTYPE -->
<html>
<head>...

<!-- ❌ Missing lang attribute -->
<html>

<!-- ❌ Missing meta charset -->
<head>
    <title>Website</title>
</head>

<!-- ❌ Content outside body -->
<html>
<head>...</head>
<h1>This should be in body</h1>
<body>...</body>
</html>
```

---

## 🧠 3.2 Tag Head pada HTML

### 🔍 Apa itu Tag Head?

Tag [`<head>`](panduan-html/bab-03-struktur-html/contoh-kode/head-demo.html:5) berisi **metadata** - informasi tentang dokumen yang tidak ditampilkan langsung ke user tetapi sangat penting untuk:
- Browser (cara render halaman)
- Search engines (SEO)
- Social media (preview cards)
- Performance (loading optimization)

### 📋 Elemen-elemen dalam Head

#### 1. **Title Tag**
```html
<title>Judul yang Muncul di Tab Browser</title>
```
- **Wajib**: Ya, setiap halaman harus punya title
- **SEO**: Judul utama untuk search results
- **Length**: Ideal 50-60 karakter
- **Unique**: Setiap halaman harus punya title unik

**Contoh yang baik:**
```html
<title>Panduan HTML untuk SMA - Belajar Web Development</title>
<title>Resep Nasi Goreng Sederhana - Blog Masakan</title>
<title>Contact Us - Toko Online Fashion</title>
```

#### 2. **Meta Tags**
```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Deskripsi halaman untuk SEO">
<meta name="keywords" content="html, css, web development">
<meta name="author" content="Nama Penulis">
```

#### 3. **Link Tags**
```html
<link rel="stylesheet" href="style.css">
<link rel="icon" href="favicon.ico">
<link rel="preconnect" href="https://fonts.googleapis.com">
```

#### 4. **Script Tags**
```html
<script src="script.js"></script>
<script>
    // Inline JavaScript
    console.log("Hello from head!");
</script>
```

### 🎯 Contoh Head Section Lengkap

```html
<head>
    <!-- Basic Meta Tags -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- SEO Meta Tags -->
    <title>Belajar HTML - Panduan Lengkap untuk SMA</title>
    <meta name="description" content="Panduan lengkap belajar HTML untuk siswa SMA. Tutorial step-by-step dari dasar hingga mahir membuat website.">
    <meta name="keywords" content="HTML, CSS, JavaScript, Web Development, Tutorial, SMA">
    <meta name="author" content="Tim Pengajar Coding">

    <!-- Open Graph Meta Tags (Social Media) -->
    <meta property="og:title" content="Belajar HTML - Panduan Lengkap">
    <meta property="og:description" content="Tutorial HTML terlengkap untuk pemula">
    <meta property="og:image" content="https://example.com/preview.jpg">
    <meta property="og:url" content="https://example.com/html-guide">

    <!-- Twitter Card Meta Tags -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Belajar HTML - Panduan Lengkap">
    <meta name="twitter:description" content="Tutorial HTML terlengkap untuk pemula">

    <!-- Favicon -->
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    <link rel="apple-touch-icon" sizes="180x180" href="apple-touch-icon.png">

    <!-- External Resources -->
    <link rel="stylesheet" href="css/style.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap">

    <!-- Performance Hints -->
    <link rel="preload" href="hero-image.jpg" as="image">
    <link rel="dns-prefetch" href="//analytics.google.com">

    <!-- PWA Meta Tags -->
    <meta name="theme-color" content="#2563eb">
    <link rel="manifest" href="manifest.json">
</head>
```

### 💡 Best Practices Head Section

#### ✅ Do:
- Selalu sertakan charset dan viewport meta tags
- Buat title yang descriptive dan unique
- Gunakan meta description untuk SEO
- Tambahkan Open Graph tags untuk social sharing
- Load critical CSS di head, defer non-critical scripts

#### ❌ Don't:
- Jangan taruh content yang terlihat di head
- Jangan lupa close tag yang memerlukan closing
- Jangan duplikasi meta tags yang sama
- Jangan load semua JavaScript di head (performance issue)

---

## 🏡 3.3 Tag Body pada HTML

### 🔍 Apa itu Tag Body?

Tag [`<body>`](panduan-html/bab-03-struktur-html/contoh-kode/body-demo.html:15) adalah container untuk semua konten yang **terlihat** dan **interaktif** di halaman web:

```html
<body>
    <!-- Semua yang user lihat dan bisa interact -->
    <h1>Judul Utama</h1>
    <p>Paragraf konten</p>
    <button onclick="alert('Hello!')">Klik Saya</button>
</body>
```

### 📐 Struktur Body yang Baik

#### 1. **Semantic HTML Structure**
```html
<body>
    <header>
        <!-- Header website: logo, navigation -->
    </header>

    <nav>
        <!-- Menu navigasi utama -->
    </nav>

    <main>
        <!-- Konten utama halaman -->
        <article>
            <!-- Artikel/konten specific -->
        </article>

        <section>
            <!-- Bagian-bagian konten -->
        </section>
    </main>

    <aside>
        <!-- Sidebar, widget, konten sampingan -->
    </aside>

    <footer>
        <!-- Footer: copyright, links, contact -->
    </footer>
</body>
```

#### 2. **Body Attributes (Historical)**
```html
<!-- ❌ DEPRECATED - Jangan gunakan -->
<body bgcolor="white" text="black" link="blue">

<!-- ✅ MODERN - Gunakan CSS -->
<body>
<style>
body {
    background-color: white;
    color: black;
}
a { color: blue; }
</style>
```

### 🎯 Contoh Body Structure untuk Website Sekolah

```html
<body>
    <!-- Skip to main content untuk accessibility -->
    <a href="#main-content" class="skip-link">Skip to main content</a>

    <!-- Header -->
    <header>
        <div class="logo">
            <img src="logo-sekolah.png" alt="Logo SMA Negeri 1">
            <h1>SMA Negeri 1 Jakarta</h1>
        </div>

        <nav>
            <ul>
                <li><a href="#beranda">Beranda</a></li>
                <li><a href="#tentang">Tentang</a></li>
                <li><a href="#akademik">Akademik</a></li>
                <li><a href="#fasilitas">Fasilitas</a></li>
                <li><a href="#kontak">Kontak</a></li>
            </ul>
        </nav>
    </header>

    <!-- Main Content -->
    <main id="main-content">
        <!-- Hero Section -->
        <section id="beranda" class="hero">
            <h2>Selamat Datang di SMA Negeri 1 Jakarta</h2>
            <p>Membentuk Generasi Unggul dan Berkarakter</p>
            <a href="#akademik" class="cta-button">Lihat Program Kami</a>
        </section>

        <!-- About Section -->
        <section id="tentang">
            <h2>Tentang Kami</h2>
            <article>
                <h3>Visi Misi</h3>
                <p>Menjadi sekolah unggulan yang menghasilkan lulusan berkualitas...</p>
            </article>
        </section>

        <!-- Academic Programs -->
        <section id="akademik">
            <h2>Program Akademik</h2>
            <div class="programs">
                <article>
                    <h3>IPA (Ilmu Pengetahuan Alam)</h3>
                    <p>Program untuk siswa yang tertarik di bidang sains dan teknologi.</p>
                </article>

                <article>
                    <h3>IPS (Ilmu Pengetahuan Sosial)</h3>
                    <p>Program untuk siswa yang tertarik di bidang sosial dan humaniora.</p>
                </article>
            </div>
        </section>
    </main>

    <!-- Sidebar -->
    <aside>
        <section>
            <h3>Pengumuman Terbaru</h3>
            <ul>
                <li><a href="#">Pendaftaran Siswa Baru 2024</a></li>
                <li><a href="#">Ujian Akhir Semester</a></li>
                <li><a href="#">Event Tech Fair</a></li>
            </ul>
        </section>

        <section>
            <h3>Quick Links</h3>
            <ul>
                <li><a href="#">E-Learning Portal</a></li>
                <li><a href="#">Library System</a></li>
                <li><a href="#">Student Portal</a></li>
            </ul>
        </section>
    </aside>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <section>
                <h4>Kontak Kami</h4>
                <address>
                    <p>Jl. Merdeka No. 123<br>
                    Jakarta Pusat, 10110</p>
                    <p>Telp: <a href="tel:+62211234567">(021) 123-4567</a></p>
                    <p>Email: <a href="mailto:info@sma1jakarta.sch.id">info@sma1jakarta.sch.id</a></p>
                </address>
            </section>

            <section>
                <h4>Follow Us</h4>
                <nav aria-label="Social Media">
                    <ul>
                        <li><a href="#" target="_blank" rel="noopener">Facebook</a></li>
                        <li><a href="#" target="_blank" rel="noopener">Instagram</a></li>
                        <li><a href="#" target="_blank" rel="noopener">YouTube</a></li>
                    </ul>
                </nav>
            </section>
        </div>

        <div class="copyright">
            <p>&copy; 2024 SMA Negeri 1 Jakarta. All rights reserved.</p>
        </div>
    </footer>

    <!-- Scripts - di akhir body untuk performance -->
    <script src="js/main.js"></script>
    <script>
        // Analytics atau script lainnya
        console.log('Website loaded successfully!');
    </script>
</body>
```

### 🎨 Body Event Handlers (JavaScript)

```html
<body onload="initializePage()" onresize="handleResize()">
    <!-- Content -->

    <script>
        function initializePage() {
            console.log('Page loaded!');
            // Inisialisasi website
        }

        function handleResize() {
            console.log('Window resized');
            // Handle responsive behavior
        }

        // Modern event handling (recommended)
        document.addEventListener('DOMContentLoaded', function() {
            console.log('DOM ready!');
        });

        window.addEventListener('resize', function() {
            console.log('Window resized');
        });
    </script>
</body>
```

### 💡 Best Practices Body Section

#### ✅ Do:
- Gunakan semantic HTML elements (header, nav, main, aside, footer)
- Letakkan scripts di akhir body untuk performance
- Struktur konten secara logical dan hierarchical
- Sertakan skip links untuk accessibility
- Gunakan proper heading hierarchy (h1 → h2 → h3)

#### ❌ Don't:
- Jangan gunakan deprecated attributes (bgcolor, text, dll)
- Jangan letakkan semua JavaScript di head
- Jangan lupa struktur semantic
- Jangan skip heading levels (h1 → h3)

---

## 🎨 3.4 Menampilkan Favicon pada HTML

### 🔍 Apa itu Favicon?

**Favicon** (favorite icon) adalah icon kecil yang muncul di:
- Tab browser 🔖
- Bookmark bar ⭐
- History list 📜
- Desktop shortcuts 🖥️
- Mobile home screen 📱

### 📏 Format dan Ukuran Favicon

#### Format File yang Didukung:
| Format | Support | Use Case |
|--------|---------|----------|
| `.ico` | ✅ Universal | Classic favicon |
| `.png` | ✅ Modern | High quality, transparency |
| `.svg` | ✅ Modern | Vector, scalable |
| `.jpg` | ❌ Limited | Tidak recommended |
| `.gif` | ⚠️ Limited | Animated favicons |

#### Ukuran Standard:
| Ukuran | Penggunaan |
|--------|------------|
| 16x16 | Tab browser |
| 32x32 | Desktop shortcut |
| 48x48 | Windows taskbar |
| 96x96 | Desktop |
| 144x144 | Microsoft tiles |
| 180x180 | Apple touch icon |
| 192x192 | Android chrome |
| 512x512 | PWA apps |

### 🔗 Cara Menambahkan Favicon

#### 1. **Favicon Sederhana (ICO)**
```html
<head>
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
</head>
```

#### 2. **Favicon Modern (PNG)**
```html
<head>
    <link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png">
</head>
```

#### 3. **Favicon Lengkap (Multiple Devices)**
```html
<head>
    <!-- Standard favicon -->
    <link rel="icon" type="image/x-icon" href="favicon.ico">

    <!-- PNG favicons untuk modern browsers -->
    <link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png">
    <link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="96x96" href="favicon-96x96.png">

    <!-- Apple Touch Icons untuk iOS -->
    <link rel="apple-touch-icon" sizes="180x180" href="apple-touch-icon.png">
    <link rel="apple-touch-icon" sizes="152x152" href="apple-touch-icon-152x152.png">
    <link rel="apple-touch-icon" sizes="144x144" href="apple-touch-icon-144x144.png">

    <!-- Android Chrome Icons -->
    <link rel="icon" type="image/png" sizes="192x192" href="android-chrome-192x192.png">
    <link rel="icon" type="image/png" sizes="512x512" href="android-chrome-512x512.png">

    <!-- Microsoft Tiles -->
    <meta name="msapplication-TileColor" content="#2563eb">
    <meta name="msapplication-TileImage" content="mstile-144x144.png">

    <!-- Safari Pinned Tab -->
    <link rel="mask-icon" href="safari-pinned-tab.svg" color="#2563eb">

    <!-- Theme color for mobile browsers -->
    <meta name="theme-color" content="#2563eb">
</head>
```

### 🎨 Membuat Favicon

#### Tools Online:
1. **Favicon.io** - https://favicon.io
2. **RealFaviconGenerator** - https://realfavicongenerator.net
3. **Favicon Generator** - https://www.favicon-generator.org

#### Design Tips:
- ✅ Simpel dan mudah dikenali
- ✅ Kontras yang baik
- ✅ Readable di ukuran kecil
- ✅ Konsisten dengan brand
- ❌ Terlalu detail
- ❌ Text yang terlalu kecil

### 📁 Struktur File Favicon

```
website-root/
├── favicon.ico (root directory)
├── favicon-16x16.png
├── favicon-32x32.png
├── apple-touch-icon.png
├── android-chrome-192x192.png
├── android-chrome-512x512.png
└── safari-pinned-tab.svg
```

### 💻 Contoh Implementasi Favicon untuk Website Sekolah

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SMA Negeri 1 Jakarta - Beranda</title>

    <!-- Favicon Package -->
    <link rel="icon" type="image/x-icon" href="favicon.ico">
    <link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png">
    <link rel="apple-touch-icon" sizes="180x180" href="apple-touch-icon.png">
    <link rel="icon" type="image/png" sizes="192x192" href="android-chrome-192x192.png">
    <link rel="manifest" href="site.webmanifest">
    <meta name="theme-color" content="#1e40af">
</head>
<body>
    <h1>🎓 SMA Negeri 1 Jakarta</h1>
    <p>Lihat favicon di tab browser! 👆</p>
</body>
</html>
```

### 🔍 Testing Favicon

#### Browser Testing:
1. **Chrome**: F12 → Network → Refresh → Cek favicon request
2. **Firefox**: Right-click tab → View Page Info → Media
3. **Safari**: Develop → Web Inspector → Network

#### Online Tools:
- **Favicon Checker** - https://realfavicongenerator.net/favicon_checker
- **Google Search Console** - Cek apakah favicon muncul di search results

### ⚠️ Troubleshooting Favicon

#### Masalah Umum:
1. **Favicon tidak muncul**
   - Clear browser cache
   - Check file path
   - Validate HTML

2. **Wrong icon**
   - Browser cache issue
   - Force refresh (Ctrl+F5)

3. **Different icon di mobile**
   - Add Apple touch icon
   - Check manifest.json

4. **Performance issue**
   - Optimize file size
   - Use appropriate format

---

## 📊 3.5 Meta Tag pada HTML

### 🔍 Apa itu Meta Tags?

**Meta tags** adalah elemen HTML yang memberikan **metadata** tentang halaman web. Meta tags tidak terlihat di halaman tetapi dibaca oleh:
- 🔍 Search engines (Google, Bing)
- 📱 Social media platforms (Facebook, Twitter)
- 🤖 Web crawlers dan bots
- 🌐 Browsers untuk rendering

### 📋 Jenis-jenis Meta Tags

#### 1. **Character Encoding**
```html
<meta charset="UTF-8">
```
- **Wajib**: Ya, harus ada
- **Fungsi**: Menentukan character encoding
- **UTF-8**: Support semua karakter international
- **Posisi**: Harus dalam 1024 byte pertama HTML

#### 2. **Viewport Meta (Mobile)**
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- **Wajib**: Ya, untuk mobile responsiveness
- **Fungsi**: Mengatur tampilan di mobile device
- **Parameters**:
  - `width=device-width`: Lebar = lebar device
  - `initial-scale=1.0`: Zoom awal 100%
  - `user-scalable=no`: Disable zoom (hati-hati accessibility)

#### 3. **SEO Meta Tags**
```html
<!-- Title (wajib, muncul di search results) -->
<title>Judul Halaman - Max 60 Karakter</title>

<!-- Description (sangat penting untuk SEO) -->
<meta name="description" content="Deskripsi halaman 150-160 karakter. Muncul di Google search results sebagai snippet.">

<!-- Keywords (deprecated, tidak berpengaruh SEO) -->
<meta name="keywords" content="html, css, web development, tutorial">

<!-- Author -->
<meta name="author" content="Nama Penulis">

<!-- Robots (instruksi untuk search engine crawler) -->
<meta name="robots" content="index, follow">
<meta name="robots" content="noindex, nofollow">
```

#### 4. **Open Graph Meta (Social Media)**
```html
<!-- Facebook, LinkedIn, WhatsApp -->
<meta property="og:title" content="Judul untuk Social Media">
<meta property="og:description" content="Deskripsi untuk social media preview">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:url" content="https://example.com/page">
<meta property="og:type" content="website">
<meta property="og:site_name" content="Nama Website">
```

#### 5. **Twitter Card Meta**
```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:site" content="@username">
<meta name="twitter:creator" content="@username">
<meta name="twitter:title" content="Judul untuk Twitter">
<meta name="twitter:description" content="Deskripsi untuk Twitter">
<meta name="twitter:image" content="https://example.com/twitter-image.jpg">
```

#### 6. **Technical Meta Tags**
```html
<!-- Refresh/Redirect -->
<meta http-equiv="refresh" content="30">
<meta http-equiv="refresh" content="0; url=https://example.com">

<!-- Content Type (biasanya tidak perlu dengan HTML5) -->
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">

<!-- Cache Control -->
<meta http-equiv="Cache-Control" content="no-cache, no-store, must-revalidate">
<meta http-equiv="Pragma" content="no-cache">
<meta http-equiv="Expires" content="0">

<!-- X-UA-Compatible (untuk IE) -->
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

### 🎯 Template Meta Tags Lengkap

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <!-- ========================================= -->
    <!-- BASIC META TAGS (WAJIB) -->
    <!-- ========================================= -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <!-- ========================================= -->
    <!-- SEO META TAGS -->
    <!-- ========================================= -->
    <title>Belajar HTML untuk SMA - Tutorial Lengkap Web Development</title>
    <meta name="description" content="Panduan lengkap belajar HTML untuk siswa SMA. Tutorial step-by-step dari dasar hingga mahir membuat website professional.">
    <meta name="keywords" content="HTML, CSS, JavaScript, Web Development, Tutorial SMA, Programming">
    <meta name="author" content="Tim Pengajar Coding Indonesia">
    <meta name="robots" content="index, follow">
    <meta name="language" content="Indonesian">
    <meta name="revisit-after" content="7 days">

    <!-- ========================================= -->
    <!-- OPEN GRAPH META (FACEBOOK, WHATSAPP) -->
    <!-- ========================================= -->
    <meta property="og:type" content="website">
    <meta property="og:title" content="Belajar HTML untuk SMA - Tutorial Lengkap">
    <meta property="og:description" content="Panduan lengkap belajar HTML untuk siswa SMA dengan contoh praktis dan project nyata.">
    <meta property="og:image" content="https://example.com/images/html-tutorial-preview.jpg">
    <meta property="og:image:alt" content="Preview gambar tutorial HTML untuk SMA">
    <meta property="og:url" content="https://example.com/html-tutorial">
    <meta property="og:site_name" content="Coding untuk SMA">
    <meta property="og:locale" content="id_ID">

    <!-- ========================================= -->
    <!-- TWITTER CARD META -->
    <!-- ========================================= -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:site" content="@codinguntuksma">
    <meta name="twitter:creator" content="@codinguntuksma">
    <meta name="twitter:title" content="Belajar HTML untuk SMA - Tutorial Lengkap">
    <meta name="twitter:description" content="Panduan lengkap belajar HTML untuk siswa SMA dengan contoh praktis.">
    <meta name="twitter:image" content="https://example.com/images/twitter-html-tutorial.jpg">
    <meta name="twitter:image:alt" content="Tutorial HTML untuk siswa SMA">

    <!-- ========================================= -->
    <!-- MOBILE & PWA META -->
    <!-- ========================================= -->
    <meta name="theme-color" content="#2563eb">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="default">
    <meta name="apple-mobile-web-app-title" content="HTML Tutorial">

    <!-- ========================================= -->
    <!-- SECURITY & PERFORMANCE -->
    <!-- ========================================= -->
    <meta http-equiv="Content-Security-Policy" content="default-src 'self'">
    <meta name="referrer" content="strict-origin-when-cross-origin">

    <!-- ========================================= -->
    <!-- FAVICON & ICONS -->
    <!-- ========================================= -->
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    <link rel="apple-touch-icon" sizes="180x180" href="apple-touch-icon.png">
    <link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png">
    <link rel="manifest" href="site.webmanifest">

    <!-- ========================================= -->
    <!-- PRELOAD & PERFORMANCE HINTS -->
    <!-- ========================================= -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link rel="dns-prefetch" href="//www.google-analytics.com">
    <link rel="preload" href="css/critical.css" as="style">

    <!-- ========================================= -->
    <!-- EXTERNAL RESOURCES -->
    <!-- ========================================= -->
    <link rel="stylesheet" href="css/style.css">
    <link rel="canonical" href="https://example.com/html-tutorial">

</head>
<body>
    <h1>Tutorial HTML untuk SMA</h1>
    <p>Meta tags sudah dioptimasi untuk SEO dan social sharing! 🚀</p>
</body>
</html>
```

### 🔍 Testing Meta Tags

#### Tools untuk Testing:
1. **Facebook Debugger** - https://developers.facebook.com/tools/debug
2. **Twitter Card Validator** - https://cards-dev.twitter.com/validator
3. **Google Rich Results Test** - https://search.google.com/test/rich-results
4. **LinkedIn Post Inspector** - https://www.linkedin.com/post-inspector

#### Browser Testing:
```html
<!-- View page source dan cari meta tags -->
<!-- DevTools → Elements → Head section -->
<!-- Network tab untuk cek resource loading -->
```

### 💡 Best Practices Meta Tags

#### ✅ Do:
- Selalu include charset dan viewport meta
- Buat title dan description yang unique per halaman
- Gunakan Open Graph untuk social sharing
- Test meta tags dengan validator tools
- Keep description 150-160 characters
- Optimize images untuk social media (1200x630px)

#### ❌ Don't:
- Jangan duplikasi meta tags yang sama
- Jangan gunakan keyword stuffing
- Jangan lupa test di berbagai platform
- Jangan gunakan meta refresh untuk redirect (gunakan 301)
- Jangan exceed character limits

#### 📊 SEO Impact Meta Tags:
| Meta Tag | SEO Impact | Social Impact |
|----------|------------|---------------|
| Title | 🔥 Very High | 🔥 High |
| Description | 🔥 Very High | 🔥 High |
| Keywords | ❌ None | ❌ None |
| OG Tags | ⚠️ Indirect | 🔥 Very High |
| Twitter Cards | ⚠️ Indirect | 🔥 Very High |
| Robots | 🔥 Very High | ❌ None |

---

## 📱 3.6 Meta Viewport pada HTML

### 🔍 Apa itu Meta Viewport?

**Meta viewport** adalah meta tag yang **sangat penting** untuk membuat website responsive di mobile device. Tanpa meta viewport, website akan tampak "kecil" dan tidak user-friendly di smartphone.

### 📏 Analogi Sederhana: Viewport sebagai Jendela

Bayangkan viewport sebagai **jendela** untuk melihat website:

```
📱 SMARTPHONE TANPA META VIEWPORT
┌─────────────────────────────────────────────────┐
│ [Tiny website that's hard to read]             │
│ Users need to pinch-zoom to read content       │
│ Navigation is difficult                         │
│ Poor user experience                            │
└─────────────────────────────────────────────────┘

📱 SMARTPHONE DENGAN META VIEWPORT
┌─────────────────────────────────────────────────┐
│ [Content fits perfectly]                        │
│ Easy to read text                               │
│ Touch-friendly navigation                       │
│ Great user experience                           │
└─────────────────────────────────────────────────┘
```

### 📝 Sintaks Meta Viewport

#### Basic Viewport (Most Common):
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

#### Advanced Viewport dengan Multiple Properties:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, minimum-scale=1.0, user-scalable=yes">
```

### 🔧 Properties Meta Viewport

| Property | Value | Deskripsi |
|----------|-------|-----------|
| `width` | `device-width` atau number | Lebar viewport |
| `height` | `device-height` atau number | Tinggi viewport |
| `initial-scale` | 0.1 - 10.0 | Zoom level awal |
| `minimum-scale` | 0.1 - 10.0 | Zoom minimum |
| `maximum-scale` | 0.1 - 10.0 | Zoom maximum |
| `user-scalable` | `yes` atau `no` | User bisa zoom atau tidak |

### 📱 Contoh Berbagai Viewport Settings

#### 1. **Standard Responsive (Recommended)**
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- ✅ Website responsive
- ✅ User bisa zoom
- ✅ Accessibility friendly

#### 2. **Fixed Width**
```html
<meta name="viewport" content="width=320">
```
- ⚠️ Fixed 320px width
- ❌ Tidak responsive
- ❌ Tidak recommended

#### 3. **No Zoom (Be Careful!)**
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
```
- ✅ Website responsive
- ❌ User tidak bisa zoom
- ⚠️ Accessibility issue

#### 4. **Limited Zoom**
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=3.0, minimum-scale=1.0">
```
- ✅ Website responsive
- ✅ User bisa zoom tapi terbatas
- ✅ Balance antara UX dan control

### 🎯 Viewport untuk Berbagai Use Case

#### Website Umum / Blog:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

#### Web App / Dashboard:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
```

#### Game atau Interactive App:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no, shrink-to-fit=no">
```

#### PWA (Progressive Web App):
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
```

### 📊 Testing Viewport di Berbagai Device

#### Chrome DevTools:
1. F12 → Toggle Device Toolbar
2. Test di berbagai device sizes:
   - iPhone SE (375x667)
   - iPhone 12 Pro (390x844)
   - Samsung Galaxy S20 (360x800)
   - iPad (768x1024)
   - iPad Pro (1024x1366)

#### Online Testing Tools:
- **BrowserStack** - https://www.browserstack.com
- **Responsive Design Checker** - https://responsivedesignchecker.com
- **Mobile-Friendly Test** - https://search.google.com/test/mobile-friendly

### 🚨 Common Viewport Mistakes

#### ❌ Missing Viewport Meta:
```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
    <!-- Missing viewport meta! -->
</head>

```
**Result**: Website akan tampak kecil di mobile, user harus pinch-zoom.

#### ❌ Wrong Width Value:
```html
<meta name="viewport" content="width=320">
```
**Problem**: Fixed width, tidak responsive.

#### ❌ Disable Zoom (Accessibility Issue):
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
```
**Problem**: User dengan visual impairment tidak bisa zoom.

### 💡 Best Practices Viewport

#### ✅ Do:
- Selalu include viewport meta di setiap halaman
- Test di berbagai device sizes
- Allow user scaling untuk accessibility
- Gunakan `device-width` untuk responsive design

#### ❌ Don't:
- Jangan disable user scaling kecuali benar-benar perlu
- Jangan gunakan fixed width
- Jangan lupa test di mobile device
- Jangan ignore accessibility guidelines

---

## 🔤 3.7 Meta Charset UTF-8 pada HTML

### 🔍 Apa itu Character Encoding?

**Character encoding** menentukan bagaimana browser menginterpretasikan dan menampilkan karakter text. Tanpa charset yang benar, website bisa menampilkan karakter aneh seperti: `Ã¢â‚¬â„¢` instead of `'`.

### 🌍 Mengapa UTF-8?

**UTF-8** (Unicode Transformation Format - 8-bit) adalah standard encoding yang:
- ✅ Support semua karakter di dunia (200+ bahasa)
- ✅ Backward compatible dengan ASCII
- ✅ Efficient untuk text Latin
- ✅ Standard web modern
- ✅ Support emoji 😊🚀🎉

### 📝 Sintaks Meta Charset

#### HTML5 (Modern - Recommended):
```html
<meta charset="UTF-8">
```

#### HTML4 (Legacy):
```html
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
```

### 🔧 Posisi Meta Charset

**WAJIB**: Meta charset harus dalam **1024 byte pertama** HTML document.

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8"> <!-- HARUS DI ATAS! -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Saya</title>
</head>
```

### 🌐 Contoh Karakter yang Didukung UTF-8

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Test UTF-8 Characters</title>
</head>
<body>
    <h1>🌍 UTF-8 Character Test</h1>

    <h2>Bahasa Indonesia:</h2>
    <p>Selamat datang! Kami menyediakan café terbaik di Indonesia.
    Nikmati suasana yang nyaman dan pelayanan yang ramah.</p>

    <h2>English:</h2>
    <p>Welcome! We provide the "best" coffee experience with 100% satisfaction guarantee.</p>

    <h2>Characters Khusus:</h2>
    <ul>
        <li>Mata uang: $ € £ ¥ ₹ Rp</li>
        <li>Matematika: ± × ÷ ∞ π √ ∑</li>
        <li>Panah: ← → ↑ ↓ ↔ ⇨</li>
        <li>Simbol: © ® ™ § ¶ • ◆</li>
    </ul>

    <h2>Emoji:</h2>
    <p>🚀 🎉 💻 📚 ⭐ ❤️ 👍 🔥 💡 🌟</p>

    <h2>Bahasa Asia:</h2>
    <ul>
        <li>中文: 你好世界</li>
        <li>日本語: こんにちは世界</li>
        <li>한국어: 안녕 세계</li>
        <li>العربية: مرحبا بالعالم</li>
        <li>Русский: Привет мир</li>
    </ul>

    <h2>Aksara Nusantara:</h2>
    <ul>
        <li>ꦱꦼꦭꦩꦠ꧀ ꦢꦠꦁ (Selamat datang - Jawa)</li>
        <li>ᮞᮨᮜᮙᮒ᮪ ᮓᮒᮀ (Selamat datang - Sunda)</li>
    </ul>
</body>
</html>
```

### 🚨 Masalah Tanpa UTF-8

#### Contoh Error Encoding:
```html
<!-- Tanpa meta charset atau charset salah -->
<!DOCTYPE html>
<html>
<head>
    <title>Website</title>
    <!-- Missing charset! -->
</head>
<body>
    <h1>Selamat datang di cafÃ© kami!</h1>
    <!-- Harusnya: Selamat datang di café kami! -->

    <p>Harga: Rp 25.000,-</p>
    <!-- Bisa jadi: HargaÂ : Rp 25.000Â ,- -->
</body>
</html>
```

### 🔧 Troubleshooting Encoding Issues

#### Problem 1: Karakter Aneh Muncul
**Gejala**: `Ã¢â‚¬â„¢` instead of `'`
**Solusi**:
```html
<head>
    <meta charset="UTF-8"> <!-- Tambahkan ini -->
</head>
```

#### Problem 2: Emoji Tidak Muncul
**Gejala**: Emoji tampil sebagai kotak kosong
**Solusi**:
```html
<head>
    <meta charset="UTF-8"> <!-- UTF-8 support emoji -->
</head>
```

#### Problem 3: Aksara Lokal Tidak Muncul
**Gejala**: Aksara Jawa/Sunda tampil sebagai kotak
**Solusi**:
```html
<head>
    <meta charset="UTF-8">
    <!-- + Font yang support aksara lokal -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Javanese&display=swap" rel="stylesheet">
</head>
```

### 🛠️ Testing Character Encoding

#### Manual Testing:
1. Buat file HTML dengan berbagai karakter
2. Save dengan encoding UTF-8
3. Test di berbagai browser
4. Cek apakah karakter tampil dengan benar

#### Tools:
- **W3C Validator**: https://validator.w3.org
- **Browser DevTools**: Network tab → Response Headers
- **Online Encoding Detector**: https://2cyr.com/decode

### 💡 Best Practices Character Encoding

#### ✅ Do:
- Selalu gunakan UTF-8 untuk website modern
- Letakkan meta charset di awal head section
- Pastikan text editor save file sebagai UTF-8
- Test dengan berbagai karakter special
- Konsisten gunakan UTF-8 di server dan database

#### ❌ Don't:
- Jangan gunakan encoding lama (ISO-8859-1, Windows-1252)
- Jangan lupa meta charset di setiap halaman
- Jangan mix encoding yang berbeda
- Jangan assume semua user pakai ASCII saja

### 📊 Encoding Comparison

| Encoding | Support | Use Case | Status |
|----------|---------|----------|---------|
| **UTF-8** | 🌍 All languages | ✅ Modern web | Recommended |
| ASCII | English only | Legacy systems | Deprecated |
| ISO-8859-1 | Western European | Old websites | Deprecated |
| Windows-1252 | Windows legacy | Microsoft docs | Avoid |

---

## 🎯 Rangkuman Bab 3

### ✅ Poin-Poin Penting

1. **Struktur HTML5 Wajib**
   ```html
   <!DOCTYPE html>
   <html lang="id">
   <head>...</head>
   <body>...</body>
   </html>
   ```

2. **Meta Tags Essential**
   - `charset="UTF-8"` untuk character support
   - `viewport` untuk mobile responsiveness
   - `description` untuk SEO snippet

3. **Head vs Body**
   - Head: Metadata, tidak terlihat user
   - Body: Content, terlihat dan interaktif

4. **Favicon Package**
   - Multiple sizes untuk berbagai device
   - Format ICO, PNG untuk compatibility

5. **Performance Hints**
   - Preconnect untuk external resources
   - Preload untuk critical assets
   - Defer/async untuk scripts

### 🚀 Next Steps

Setelah menguasai Bab 3, Anda siap untuk:
- **Bab 4**: Menambahkan multimedia (gambar, audio, video)
- **CSS Integration**: Styling template yang sudah dibuat
- **JavaScript Enhancement**: Menambahkan interactivity

### 💡 Tips Sukses

1. **Always Validate**: Gunakan W3C validator untuk cek struktur
2. **Test Responsiveness**: Cek di berbagai device sizes
3. **Performance First**: Optimize loading dengan proper meta tags
4. **Accessibility Matters**: Gunakan semantic HTML dan ARIA labels
5. **SEO Friendly**: Meta tags yang proper untuk search visibility

---

## 🎓 Self-Assessment Checklist

Sebelum melanjutkan ke Bab 4, pastikan Anda bisa:

- [ ] Menulis struktur HTML5 yang valid dan lengkap
- [ ] Menjelaskan fungsi setiap bagian dalam tag head
- [ ] Menggunakan meta tags untuk SEO dan social media
- [ ] Menambahkan favicon dengan berbagai format
- [ ] Mengimplementasikan viewport untuk mobile responsive
- [ ] Memahami pentingnya UTF-8 character encoding
- [ ] Membuat template HTML yang production-ready
- [ ] Mengatasi masalah encoding dan viewport
- [ ] Testing struktur HTML dengan validator tools

**Jika semua sudah ✅, Anda siap melanjutkan ke [Bab 4: Multimedia dalam HTML](../bab-04-multimedia/README.md)**

---

*Selamat! Anda telah menguasai struktur dasar HTML yang professional! 🎉*
