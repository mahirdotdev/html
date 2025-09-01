# 📚 BAB 1: PERKENALAN HTML DAN PERSIAPAN ENVIRONMENT

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan bab ini, siswa akan mampu:
- Memahami konsep dasar HTML dan peranannya dalam web development
- Menjelaskan mengapa website penting di era digital
- Menyiapkan environment development yang tepat
- Membuat dan menjalankan file HTML pertama
- Memahami workflow dasar web development

---

## 📖 1.1 Apa itu HTML?

### 🔍 Definisi HTML

**HTML** adalah kepanjangan dari **HyperText Markup Language**. Mari kita pahami setiap kata ini:

- **HyperText**: Teks yang memiliki kemampuan untuk terhubung dengan teks lain melalui link
- **Markup**: Sistem penandaan untuk memberikan struktur dan format pada teks
- **Language**: Bahasa pemrograman yang memiliki aturan dan sintaks tertentu

### 🏠 Analogi Sederhana: HTML sebagai Kerangka Rumah

Bayangkan kamu sedang membangun rumah:

```
🏗️ MEMBANGUN RUMAH vs MEMBANGUN WEBSITE

Rumah Fisik           |  Website
---------------------|-------------------------
🏗️ Kerangka besi     → HTML (struktur)
🎨 Cat dan dekorasi   → CSS (styling)
⚡ Instalasi listrik  → JavaScript (interaktif)
🚪 Pintu dan jendela  → Link dan navigasi
📋 Denah rumah        → Layout halaman
🧱 Fondasi           → Server dan hosting
```

HTML adalah **kerangka** website yang menentukan:
- Dimana letak judul
- Dimana paragraph ditempatkan
- Dimana gambar dipasang
- Bagaimana struktur halaman disusun

### 🌐 Peran HTML dalam Pengembangan Web

HTML adalah **bahasa dasar web** yang:

1. **Memberikan Struktur**: Mengatur tata letak konten
2. **Menyediakan Makna**: Memberikan konteks pada informasi
3. **Menghubungkan Halaman**: Membuat link antar halaman
4. **Mendukung Multimedia**: Menampilkan gambar, video, audio
5. **Memungkinkan Interaksi**: Membuat form dan tombol

### 📜 Sejarah Singkat HTML

| Tahun | Versi | Fitur Utama |
|-------|-------|-------------|
| 1990 | HTML | Versi pertama oleh Tim Berners-Lee |
| 1995 | HTML 2.0 | Standard resmi pertama |
| 1997 | HTML 3.2 | Tabel dan applet |
| 1999 | HTML 4.01 | CSS support, multimedia |
| 2014 | HTML5 | Semantic tags, multimedia native |

### ⚡ Mengapa HTML Penting?

1. **Fondasi Web**: Semua website menggunakan HTML
2. **Universal**: Dapat dibaca oleh semua browser
3. **Mudah Dipelajari**: Sintaks sederhana dan logis
4. **Career Opportunities**: Dasar untuk web developer
5. **Kreativitas**: Media untuk mengekspresikan ide

---

## 🚀 1.2 Mengapa Membuat Website?

### 🌟 Keuntungan Memiliki Website

#### Untuk Siswa SMA:
- **Portfolio Digital**: Menampilkan karya dan prestasi
- **Blog Pribadi**: Berbagi hobi dan minat
- **Proyek Sekolah**: Presentasi yang interaktif
- **Skill Development**: Melatih kemampuan teknologi

#### Untuk Masa Depan:
- **Personal Branding**: Membangun identitas online
- **Business Opportunity**: Toko online, jasa
- **Communication**: Platform berbagi informasi
- **Career Advantage**: Skill yang dibutuhkan industri

### 🎯 Jenis-Jenis Website

| Jenis Website | Contoh | Tujuan |
|---------------|---------|---------|
| **Personal** | Blog pribadi, Portfolio | Ekspresi diri |
| **Bisnis** | Toko online, Company profile | Komersial |
| **Edukasi** | E-learning, Tutorial | Pembelajaran |
| **Entertainment** | Game online, Streaming | Hiburan |
| **Sosial** | Forum, Social media | Komunitas |

### 💼 Prospek Karir Web Development

**Posisi Karir:**
- 🎨 **Front-end Developer**: Fokus tampilan dan user experience
- ⚙️ **Back-end Developer**: Fokus server dan database
- 🔧 **Full-stack Developer**: Gabungan front-end dan back-end
- 🎯 **UI/UX Designer**: Desain antarmuka pengguna
- 📊 **Web Analyst**: Analisis performa website

**Gaji Rata-rata (Indonesia, 2024):**
- Junior Web Developer: Rp 5-8 juta/bulan
- Mid-level Web Developer: Rp 8-15 juta/bulan
- Senior Web Developer: Rp 15-30 juta/bulan

---

## 🛠️ 1.3 Persiapan Membuat Website

### 💻 Tools yang Diperlukan

#### 1. **Text Editor** (Pilih salah satu)

**🌟 Visual Studio Code (Recommended)**
- ✅ Gratis dan open source
- ✅ Extensions lengkap
- ✅ Syntax highlighting
- ✅ Auto-completion
- ✅ Integrated terminal

**Alternatif lain:**
- Sublime Text
- Atom
- Notepad++
- Brackets

#### 2. **Web Browser** (Install minimal 2)

**🌟 Google Chrome (Recommended)**
- ✅ Developer tools canggih
- ✅ Fast rendering
- ✅ Extension ecosystem

**Browser alternatif:**
- Firefox Developer Edition
- Microsoft Edge
- Safari (Mac only)

#### 3. **File Manager**
- Windows Explorer (Windows)
- Finder (Mac)
- Nautilus (Linux)

### 📥 Menginstall Visual Studio Code

#### Windows:
1. Kunjungi https://code.visualstudio.com
2. Download "Download for Windows"
3. Jalankan file installer
4. Ikuti panduan instalasi
5. Pilih "Add to PATH" saat instalasi

#### Mac:
1. Kunjungi https://code.visualstudio.com
2. Download "Download for Mac"
3. Extract file .zip
4. Drag VS Code ke Applications folder

#### Linux:
```bash
# Ubuntu/Debian
sudo snap install code --classic

# Atau download .deb file dari website
```

### 🔧 Extensions VS Code yang Berguna

Install extensions ini untuk pengalaman yang lebih baik:

| Extension | Fungsi | Command |
|-----------|--------|---------|
| **Live Server** | Preview real-time | Ctrl+Shift+P → "Live Server" |
| **HTML Snippets** | Auto-completion HTML | Otomatis |
| **Prettier** | Code formatter | Alt+Shift+F |
| **Auto Rename Tag** | Sync tag HTML | Otomatis |
| **HTML CSS Support** | CSS IntelliSense | Otomatis |

**Cara Install Extensions:**
1. Buka VS Code
2. Klik icon Extensions (Ctrl+Shift+X)
3. Search nama extension
4. Klik "Install"

### 📁 Membuat Folder Kerja

Buat struktur folder yang rapi untuk project HTML:

```
📁 html-projects/
  ├── 📁 bab-01/
  ├── 📁 bab-02/
  ├── 📁 latihan/
  ├── 📁 proyek-mini/
  └── 📁 assets/
      ├── 📁 images/
      ├── 📁 css/
      └── 📁 js/
```

**Langkah membuat folder:**
1. Buat folder `html-projects` di Desktop atau Documents
2. Buka folder tersebut di VS Code (File → Open Folder)

---

## ⚙️ 1.4 Environment Setup dan Testing

### 🎯 Membuat File HTML Pertama

Mari kita buat file HTML pertama dengan nama [`hello-world.html`](panduan-html/bab-01-perkenalan/contoh-kode/hello-world.html):

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Halo Dunia - HTML Pertamaku</title>
</head>
<body>
    <h1>Halo Dunia!</h1>
    <p>Ini adalah halaman HTML pertama saya.</p>
    <p>Saya sedang belajar HTML untuk siswa SMA.</p>
</body>
</html>
```

### 📝 Penjelasan Kode

Mari kita pahami setiap baris kode:

```html
<!DOCTYPE html>
```
- **DOCTYPE**: Memberitahu browser bahwa ini adalah dokumen HTML5
- Harus ditulis di baris pertama

```html
<html lang="id">
```
- **Tag `<html>`**: Tag pembungkus semua konten
- **`lang="id"`**: Bahasa Indonesia untuk SEO dan accessibility

```html
<head>
    <!-- Meta information dan settings -->
</head>
```
- **Tag `<head>`**: Informasi metadata (tidak terlihat di halaman)
- Berisi pengaturan dan informasi untuk browser

```html
<meta charset="UTF-8">
```
- **Charset**: Encoding karakter untuk huruf Indonesia (é, ñ, dll)

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- **Viewport**: Pengaturan tampilan di mobile device

```html
<title>Halo Dunia - HTML Pertamaku</title>
```
- **Title**: Judul yang muncul di tab browser

```html
<body>
    <!-- Konten yang terlihat di halaman -->
</body>
```
- **Tag `<body>`**: Konten yang akan terlihat pengunjung

### 🚀 Menjalankan File HTML di Browser

#### Metode 1: Double Click File
1. Save file dengan ekstensi `.html`
2. Double click file di Windows Explorer/Finder
3. File akan terbuka di browser default

#### Metode 2: Drag & Drop ke Browser
1. Buka browser (Chrome/Firefox)
2. Drag file HTML dari folder
3. Drop ke tab browser

#### Metode 3: Live Server (VS Code)
1. Install extension "Live Server"
2. Right click pada file HTML
3. Pilih "Open with Live Server"
4. Halaman akan terbuka dengan auto-refresh

#### Metode 4: File Path di Browser
1. Copy path file HTML
2. Paste di address bar browser
3. Tambahkan `file://` di depan path

### 🔍 Debugging Dasar

#### Menggunakan Developer Tools

**Chrome DevTools (F12):**

```
🔧 Developer Tools Panel:
├── 📋 Elements    → Lihat struktur HTML
├── 🎨 Styles      → Lihat CSS properties
├── 💾 Console     → Lihat error messages
├── 🔗 Network     → Monitor loading files
└── 📱 Device      → Test responsive design
```

**Cara menggunakan:**
1. Tekan F12 atau Right click → "Inspect"
2. Tab Elements: Lihat struktur HTML
3. Tab Console: Lihat error (jika ada)

#### Error Umum dan Solusi

| Error | Penyebab | Solusi |
|-------|----------|--------|
| Halaman tidak muncul | File path salah | Periksa lokasi file |
| Karakter aneh (Ã¢â‚¬) | Encoding salah | Tambahkan `<meta charset="UTF-8">` |
| Tag tidak berfungsi | Typo atau tidak ditutup | Periksa spelling dan closing tag |
| Gambar tidak muncul | Path gambar salah | Periksa path relative/absolute |

### 🔄 Workflow Development

**Workflow yang Recommended:**

```
1. 📝 WRITE     → Tulis kode HTML
2. 💾 SAVE      → Save file (Ctrl+S)
3. 🔄 REFRESH   → Refresh browser (F5)
4. 🔍 TEST      → Test fungsionalitas
5. 🐛 DEBUG     → Fix error jika ada
6. ♻️  REPEAT   → Ulangi proses
```

**Tips Workflow:**
- Save sering-sering (Ctrl+S)
- Test di multiple browser
- Gunakan Live Server untuk auto-refresh
- Backup code secara berkala

---

## 🏗️ Proyek Mini Bab 1

### 🎯 Membuat Halaman "Halo Dunia" Pertama

**Objective:** Membuat halaman HTML sederhana yang menampilkan informasi pribadi

#### 📋 Requirements:
1. Struktur HTML yang benar
2. Meta tags lengkap
3. Judul halaman yang descriptive
4. Minimal 3 paragraph konten
5. Testing di 2 browser berbeda

#### 🎨 Template Proyek:

Buat file [`proyek-halo-dunia.html`](panduan-html/bab-01-perkenalan/proyek-mini/proyek-halo-dunia.html):

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Halaman perkenalan diri untuk belajar HTML">
    <meta name="author" content="[Nama Anda]">
    <title>Perkenalan Diri - [Nama Anda]</title>
</head>
<body>
    <h1>Halo! Saya [Nama Anda]</h1>

    <h2>Tentang Saya</h2>
    <p>Saya adalah siswa SMA yang sedang belajar HTML. Saya bersekolah di [Nama Sekolah] dan berada di kelas [Kelas].</p>

    <h2>Hobi dan Minat</h2>
    <p>Hobi saya adalah <strong>[sebutkan hobi Anda]. Saya juga tertarik dengan teknologi dan ingin belajar web development.</p>

    <h2>Tujuan Belajar HTML</h2>
    <p>Tujuan saya belajar HTML</strong> adalah </em>[tuliskan tujuan Anda]. Saya berharap suatu hari nanti bisa membuat website yang keren!</p>

    <p><strong>Terima kasih telah mengunjungi halaman pertama saya!</strong></p>
</body>
</html>
```

#### ✅ Checklist Penyelesaian:
- [ ] File HTML dibuat dengan struktur lengkap
- [ ] Meta tags ditambahkan
- [ ] Konten personal diisi
- [ ] File berhasil dibuka di browser
- [ ] Testing di minimal 2 browser
- [ ] Developer tools dicoba untuk inspect element

#### 🎯 Challenge (Opsional):
- Tambahkan lebih banyak heading (h3, h4)
- Experiment dengan tag formatting (strong, em)
- Coba ubah title dan refresh browser untuk melihat perubahan tab

---

## 📝 Latihan Bab 1

### 📚 Quiz Konsep Dasar

#### Soal Pilihan Ganda

**1. HTML adalah kepanjangan dari:**
- a) HyperText Markup Language
- b) HyperText Machine Language
- c) High Tech Markup Language
- d) HyperText Modern Language

**2. Tag yang wajib ada di setiap dokumen HTML adalah:**
- a) `<title>`
- b) `<head>`
- c) `<html>`
- d) Semua benar

**3. Untuk menampilkan karakter Indonesia dengan benar, kita menggunakan:**
- a) `<meta charset="ISO-8859-1">`
- b) `<meta charset="UTF-8">`
- c) `<meta charset="ASCII">`
- d) Tidak perlu meta charset

**4. Extension file HTML yang benar adalah:**
- a) .htm
- b) .html
- c) .web
- d) a dan b benar

**5. Shortcut untuk membuka Developer Tools di browser adalah:**
- a) F11
- b) F12
- c) Ctrl+F12
- d) Alt+F12

#### Soal Essay

**1. Jelaskan perbedaan antara tag `<head>` dan `<body>` dalam HTML!**

**2. Mengapa meta viewport penting untuk website modern?**

**3. Sebutkan 3 keuntungan menggunakan Visual Studio Code untuk HTML development!**

**4. Bagaimana cara mengatasi jika website menampilkan karakter aneh (encoding error)?**

**5. Jelaskan workflow yang baik untuk HTML development!**

### 💻 Latihan Praktik Coding

#### Latihan 1: Perbaiki Kode Error

Kode HTML berikut memiliki beberapa error. Temukan dan perbaiki:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Website Saya
    <meta charset="UTF-8">
</head>
<body>
    <h1>Selamat Datang</h1>
    <p>Ini adalah paragraph pertama.
    <p>Ini adalah paragraph kedua.</p>
<body>
</html>
```

**Error yang ada:**
1. Tag title tidak ditutup
2. Tag p pertama tidak ditutup
3. Tag body tidak ditutup dengan benar
4. Missing lang attribute di html tag

#### Latihan 2: Buat Struktur HTML Lengkap

Buat file HTML dengan requirements:
- DOCTYPE HTML5
- Lang bahasa Indonesia
- Meta charset, viewport, description, author
- Title yang descriptive
- Struktur head dan body yang benar
- Minimal 1 heading dan 2 paragraph

#### Latihan 3: Testing Browser

1. Buat file HTML sederhana
2. Test di Chrome dan Firefox
3. Buka Developer Tools di kedua browser
4. Screenshot hasil testing

### 🔧 Troubleshooting Exercises

#### Problem 1: File HTML Tidak Terbuka
**Gejala:** Double click file HTML tidak membuka browser
**Possible Solutions:**
- Periksa file extension (.html)
- Right click → Open with → Browser
- Check default program untuk .html files

#### Problem 2: Karakter Indonesia Tidak Muncul
**Gejala:** Huruf "é", "ñ", dll muncul sebagai "?"
**Solution:**
- Tambahkan `<meta charset="UTF-8">`
- Save file dengan encoding UTF-8

#### Problem 3: Live Server Tidak Jalan
**Gejala:** Extension Live Server tidak bekerja
**Solutions:**
- Restart VS Code
- Check extension ter-install dengan benar
- Right click file HTML → "Open with Live Server"

---

## 🎯 Rangkuman Bab 1

### ✅ Poin-Poin Penting

1. **HTML = HyperText Markup Language**
   - Bahasa markup untuk struktur web
   - Foundation semua website
   - Easy to learn, powerful to use

2. **Website Development Tools**
   - Text Editor: Visual Studio Code
   - Browser: Chrome + Firefox
   - Extensions: Live Server, HTML Snippets

3. **Struktur HTML Dasar**
   ```html
   <!DOCTYPE html>
   <html lang="id">
   <head>
       <!-- Meta information -->
   </head>
   <body>
       <!-- Visible content -->
   </body>
   </html>
   ```

4. **Development Workflow**
   - Write → Save → Refresh → Test → Debug

5. **Developer Tools (F12)**
   - Elements: HTML structure
   - Console: Error messages
   - Essential for debugging

### 🚀 Next Steps

Setelah menguasai Bab 1, Anda siap untuk:
- **Bab 2**: Mempelajari elemen dan tag HTML dasar
- **Praktek**: Membuat halaman dengan berbagai elemen
- **Project**: Mulai membangun portfolio website

### 💡 Tips Sukses

1. **Practice Regularly**: Code setiap hari minimal 30 menit
2. **Experiment**: Jangan takut mencoba hal baru
3. **Debug Patiently**: Error adalah bagian dari learning
4. **Ask Questions**: Gunakan developer community
5. **Build Projects**: Apply what you learn immediately

---

## 🎓 Self-Assessment Checklist

Sebelum melanjutkan ke Bab 2, pastikan Anda bisa:

- [ ] Menjelaskan apa itu HTML dan fungsinya
- [ ] Menginstall dan menggunakan VS Code
- [ ] Membuat file HTML dengan struktur yang benar
- [ ] Menjalankan file HTML di browser
- [ ] Menggunakan Developer Tools untuk inspect element
- [ ] Mengatasi error encoding dan sintaks dasar
- [ ] Memahami workflow development HTML

**Jika semua sudah ✅, Anda siap melanjutkan ke [Bab 2: Elemen dan Tag HTML Dasar](../bab-02-elemen-tag-dasar/README.md)**

---

*Selamat! Anda telah menyelesaikan Bab 1. HTML journey Anda baru saja dimulai! 🚀*
