# Bab 7: Non-Semantic HTML (Div dan Span)

## 🎯 Tujuan Pembelajaran
Setelah menyelesaikan bab ini, kalian akan mampu:
- Memahami konsep dasar elemen non-semantic dalam HTML
- Menggunakan tag `<div>` untuk grouping dan layout
- Menggunakan tag `<span>` untuk styling inline
- Memahami perbedaan antara elemen block dan inline
- Menerapkan struktur dasar layout menggunakan div
- Memahami keterbatasan elemen non-semantic
- Mengetahui kapan harus menggunakan elemen semantic

## 📚 Konsep Dasar

### Apa Itu Elemen Non-Semantic?
**Elemen Non-Semantic** adalah elemen HTML yang tidak memiliki makna atau tujuan spesifik dalam konteks konten. Elemen ini digunakan terutama untuk keperluan styling dan layout tanpa memberikan informasi tambahan tentang isi konten.

**Analogi Sederhana:**
Elemen non-semantic seperti kotak-kotak kosong yang bisa digunakan untuk menyimpan berbagai macam barang. Kotak tersebut tidak memberitahu apa isinya, tetapi sangat berguna untuk mengatur dan mengelompokkan barang-barang tersebut.

### Elemen Non-Semantic Utama
1. **`<div>`** - Elemen block untuk grouping konten
2. **`<span>`** - Elemen inline untuk styling teks

### Kenapa Elemen Non-Semantic Penting?
1. **Layout dan Styling** - Membantu dalam mengatur tata letak halaman
2. **Grouping** - Mengelompokkan elemen untuk styling CSS
3. **Fleksibilitas** - Dapat digunakan untuk berbagai keperluan
4. **Kompatibilitas** - Didukung oleh semua browser

---

## 📦 Tag `<div>` - Elemen Block

### Definisi dan Tujuan
Tag `<div>` (division) adalah elemen block-level yang digunakan untuk mengelompokkan elemen-elemen HTML lainnya. Elemen ini tidak memiliki makna semantik spesifik tetapi sangat berguna untuk styling dan layout.

### Karakteristik `<div>`
- **Block-level element** - Dimulai dari baris baru
- **Full width** - Memenuhi lebar container
- **Bisa berisi elemen lain** - Termasuk block dan inline elements
- **Styling yang fleksibel** - Dapat diatur dengan CSS

### Syntax Dasar
```html
<div>
    <!-- Konten di sini -->
</div>
```

### Contoh Penggunaan
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contoh Div</title>
    <style>
        .container {
            background-color: #f0f0f0;
            padding: 20px;
            margin: 10px 0;
            border: 1px solid #ccc;
        }

        .header {
            background-color: #2196F3;
            color: white;
            padding: 15px;
            text-align: center;
        }

        .content {
            background-color: white;
            padding: 20px;
            margin: 10px 0;
        }

        .footer {
            background-color: #333;
            color: white;
            padding: 15px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Selamat Datang di Website Kami</h1>
        </div>

        <div class="content">
            <h2>Tentang Kami</h2>
            <p>Ini adalah contoh penggunaan div untuk membuat struktur halaman.</p>

            <div class="article">
                <h3>Artikel Terbaru</h3>
                <p>Isi artikel terbaru...</p>
            </div>
        </div>

        <div class="footer">
            <p>&copy; 2024 Hak Cipta Dilindungi</p>
        </div>
    </div>
</body>
</html>
```

### Atribut yang Sering Digunakan dengan `<div>`
| Atribut | Tujuan | Contoh Penggunaan |
|---------|--------|-------------------|
| `class` | Mengelompokkan div untuk styling | `<div class="header">` |
| `id` | Identifier unik untuk div | `<div id="main-content">` |
| `style` | Inline CSS styling | `<div style="color: red;">` |

---

## 🏷️ Tag `<span>` - Elemen Inline

### Definisi dan Tujuan
Tag `<span>` adalah elemen inline-level yang digunakan untuk mengelompokkan atau styling bagian dari teks tanpa mempengaruhi struktur dokumen.

### Karakteristik `<span>`
- **Inline-level element** - Tidak memulai baris baru
- **Hanya sepanjang konten** - Tidak memenuhi lebar container
- **Tidak bisa berisi block elements** - Hanya teks dan inline elements
- **Styling yang presisi** - Untuk bagian teks spesifik

### Syntax Dasar
```html
<span>Text yang akan di-styling</span>
```

### Contoh Penggunaan
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contoh Span</title>
    <style>
        .highlight {
            background-color: yellow;
            font-weight: bold;
        }

        .error {
            color: red;
            text-decoration: underline;
        }

        .success {
            color: green;
            font-style: italic;
        }
    </style>
</head>
<body>
    <h1>Contoh Penggunaan <span class="highlight">Span</span></h1>

    <p>Ini adalah paragraf dengan <span class="error">teks error</span>
       dan <span class="success">teks sukses</span> yang menggunakan span.</p>

    <p>Nama produk: <span class="highlight">Laptop Gaming Pro</span> -
       <span class="error">Stok habis</span></p>

    <p>Harga: <span class="success">Rp 15.000.000</span></p>
</body>
</html>
```

---

## ⚖️ Perbedaan Block vs Inline Elements

### Elemen Block
| Karakteristik | Deskripsi |
|---------------|-----------|
| **Baris baru** | Selalu dimulai dari baris baru |
| **Full width** | Memenuhi lebar container |
| **Padding/Margin** | Semua sisi bisa diberi padding/margin |
| **Konten** | Bisa berisi block dan inline elements |
| **Contoh** | `<div>`, `<p>`, `<h1>`, `<section>` |

### Elemen Inline
| Karakteristik | Deskripsi |
|---------------|-----------|
| **Tidak baris baru** | Tidak memulai baris baru |
| **Sesuai konten** | Lebar sesuai dengan konten |
| **Padding/Margin** | Hanya horizontal yang efektif |
| **Konten** | Hanya bisa berisi teks dan inline elements |
| **Contoh** | `<span>`, `<a>`, `<strong>`, `<em>` |

### Visualisasi Perbedaan
```html
<!-- Block Element -->
<div style="background: lightblue; margin: 10px 0;">
    Ini adalah div (block element)
    <div style="background: lightgreen;">
        Div di dalam div
    </div>
</div>

<!-- Inline Element -->
<p>Ini adalah paragraf dengan <span style="background: yellow;">span (inline element)</span> di dalamnya.</p>
```

---

## 🎨 Penggunaan untuk Styling dan Layout

### Layout Dasar dengan Div
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout dengan Div</title>
    <style>
        .wrapper {
            max-width: 1200px;
            margin: 0 auto;
            background: #f5f5f5;
        }

        .header {
            background: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .main-content {
            display: flex;
            min-height: 400px;
        }

        .sidebar {
            flex: 1;
            background: #ddd;
            padding: 20px;
        }

        .content {
            flex: 3;
            background: white;
            padding: 20px;
        }

        .footer {
            background: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="wrapper">
        <div class="header">
            <h1>Header Website</h1>
        </div>

        <div class="main-content">
            <div class="sidebar">
                <h3>Menu</h3>
                <ul>
                    <li>Beranda</li>
                    <li>Tentang</li>
                    <li>Kontak</li>
                </ul>
            </div>

            <div class="content">
                <h2>Konten Utama</h2>
                <p>Ini adalah konten utama website...</p>
            </div>
        </div>

        <div class="footer">
            <p>&copy; 2024 Footer Website</p>
        </div>
    </div>
</body>
</html>
```

### Styling Teks dengan Span
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Styling dengan Span</title>
    <style>
        .product-name {
            font-weight: bold;
            color: #2196F3;
        }

        .price {
            font-size: 1.2em;
            color: #4CAF50;
        }

        .discount {
            background: #FF5722;
            color: white;
            padding: 2px 6px;
            border-radius: 4px;
            font-size: 0.8em;
        }

        .old-price {
            text-decoration: line-through;
            color: #999;
        }
    </style>
</head>
<body>
    <div class="product-card">
        <h3>Produk Terbaru</h3>
        <p>Nama: <span class="product-name">Smartphone Pro Max</span></p>
        <p>Harga:
            <span class="old-price">Rp 12.000.000</span>
            <span class="price">Rp 10.000.000</span>
            <span class="discount">Hemat 16%</span>
        </p>
        <p>Deskripsi: <span class="product-name">Smartphone dengan kamera terbaik</span></p>
    </div>
</body>
</html>
```

---

## ⚠️ Keterbatasan Elemen Non-Semantic

### Masalah dengan Hanya Menggunakan Div/Span
1. **Aksesibilitas Buruk** - Pembaca layar tidak mengerti konten
2. **SEO Lemah** - Mesin pencari kurang memahami struktur
3. **Maintenance Sulit** - Kode sulit dipahami dan dimodifikasi
4. **Tidak Semantik** - Tidak menjelaskan makna konten

### Contoh Kode yang Kurang Baik
```html
<!-- ❌ Kurang Baik -->
<div class="bagian1">
    <div class="bagian2">
        <div class="bagian3">Judul Artikel</div>
        <div class="bagian4">Tanggal: 1 Januari 2024</div>
        <div class="bagian5">
            <div class="bagian6">Isi artikel...</div>
        </div>
    </div>
</div>
```

### Solusi dengan Elemen Semantic (Bab Selanjutnya)
```html
<!-- ✅ Lebih Baik -->
<article>
    <header>
        <h1>Judul Artikel</h1>
        <time datetime="2024-01-01">Tanggal: 1 Januari 2024</time>
    </header>
    <main>
        <p>Isi artikel...</p>
    </main>
</article>
```

---

## 🎯 Best Practices Penggunaan Div dan Span

### Kapan Menggunakan Div
1. **Grouping konten** untuk styling CSS
2. **Membuat layout** halaman
3. **Wrapper untuk komponen** kompleks
4. **Ketika tidak ada elemen semantic** yang cocok

### Kapan Menggunakan Span
1. **Styling bagian teks** spesifik
2. **Highlight kata atau frasa**
3. **Menambahkan atribut** ke bagian teks
4. **Inline styling** tanpa mempengaruhi layout

### Prinsip Penting
1. **Gunakan elemen semantic** jika tersedia
2. **Berikan class yang bermakna** (bukan generic seperti "div1", "div2")
3. **Hindari nesting terlalu dalam**
4. **Gunakan ID untuk elemen unik**
5. **Gunakan class untuk elemen yang berulang**

---

## 🚫 Kesalahan Umum dan Solusi

### 1. Menggunakan Div untuk Semua Hal
**❌ Kesalahan:**
```html
<div class="judul">Judul Artikel</div>
<div class="paragraf">Isi artikel...</div>
<div class="daftar">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
</div>
```

**✅ Perbaikan:**
```html
<h1>Judul Artikel</h1>
<p>Isi artikel...</p>
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
</ul>
```

### 2. Class yang Tidak Bermakna
**❌ Kesalahan:**
```html
<div class="div1">
    <div class="div2">
        <div class="div3">Konten</div>
    </div>
</div>
```

**✅ Perbaikan:**
```html
<div class="product-card">
    <div class="product-header">
        <div class="product-title">Nama Produk</div>
    </div>
</div>
```

### 3. Span dalam Block Element
**❌ Kesalahan:**
```html
<div>
    <span><h1>Judul</h1></span>
    <span><p>Paragraf</p></span>
</div>
```

**✅ Perbaikan:**
```html
<div>
    <h1>Judul</h1>
    <p>Paragraf</p>
</div>
```

---

## 🔧 Troubleshooting

### Masalah Umum dan Solusi

| Masalah | Penyebab | Solusi |
|---------|----------|---------|
| Layout tidak sesuai | CSS tidak diterapkan | Periksa class/id dan CSS |
| Span tidak terlihat | Tidak ada styling | Tambahkan warna/latar belakang |
| Div overlap | Positioning CSS | Periksa z-index dan position |
| Responsive tidak bekerja | Tidak ada media queries | Tambahkan CSS responsive |

---

## 📝 Latihan

### Latihan 1: Membuat Card Produk
Buat card produk menggunakan div dan span dengan:
- Container card menggunakan div
- Nama produk dengan span untuk styling
- Harga dengan span berbeda
- Tombol menggunakan div
- Styling CSS untuk tampilan menarik

### Latihan 2: Layout Halaman Sederhana
Buat layout halaman dengan:
- Header menggunakan div
- Sidebar menggunakan div
- Content area menggunakan div
- Footer menggunakan div
- Flexbox atau Grid untuk layout

### Latihan 3: Styling Teks dengan Span
Buat paragraf dengan:
- Highlight kata kunci menggunakan span
- Teks error menggunakan span
- Teks sukses menggunakan span
- Berbagai warna dan styling dengan CSS

---

## 📋 Rangkuman

### Yang Telah Dipelajari:
1. **Elemen Non-Semantic** - `<div>` dan `<span>` untuk layout dan styling
2. **Perbedaan Block vs Inline** - Karakteristik dan penggunaan
3. **Styling dengan CSS** - Menggunakan class dan id
4. **Layout dasar** - Membuat struktur halaman dengan div
5. **Best practices** - Penggunaan yang benar dan efektif

### Konsep Penting:
- Div untuk grouping dan layout block-level
- Span untuk styling inline-level
- Perbedaan block dan inline elements
- Keterbatasan non-semantic elements
- Pentingnya class dan id yang bermakna

### Next Step:
Lanjut ke **Bab 8: Semantic HTML** untuk mempelajari elemen-elemen HTML yang memiliki makna semantik dan lebih baik untuk aksesibilitas serta SEO.

---

**💡 Tips Pro:**
- Gunakan div/span hanya jika tidak ada elemen semantic yang cocok
- Berikan class yang bermakna untuk kemudahan maintenance
- Hindari nesting terlalu dalam untuk performa dan readability
- Gunakan CSS Grid/Flexbox untuk layout modern
- Selalu pertimbangkan aksesibilitas dan SEO

**🔗 File Terkait:**
- [`contoh-kode/div-span-demo.html`](contoh-kode/div-span-demo.html) - Demo lengkap div dan span
- [`contoh-kode/layout-dasar.html`](contoh-kode/layout-dasar.html) - Demo layout dengan div
- [`contoh-kode/styling-teks.html`](contoh-kode/styling-teks.html) - Demo styling dengan span
- [`proyek-mini/layout-halaman.html`](proyek-mini/layout-halaman.html) - Proyek layout halaman
