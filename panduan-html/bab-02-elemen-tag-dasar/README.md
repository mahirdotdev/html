# 📚 BAB 2: ELEMEN DAN TAG HTML DASAR

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan bab ini, siswa akan mampu:
- Memahami konsep elemen HTML dan perbedaannya dengan tag
- Menggunakan berbagai tag HTML untuk format teks dan konten
- Membuat struktur halaman dengan heading, paragraf, dan list
- Menampilkan quote, code, dan konten khusus lainnya
- Membuat link dan navigasi antar halaman
- Membangun tabel sederhana untuk menampilkan data
- Menggunakan komentar HTML dengan tepat

---

## 📖 2.1 Memahami Elemen HTML

### 🔍 Definisi Elemen HTML

**Elemen HTML** adalah komponen dasar yang membangun halaman web. Setiap elemen terdiri dari:

1. **Opening Tag**: Menandai awal elemen `<tagname>`
2. **Content**: Isi/konten di dalam elemen
3. **Closing Tag**: Menandai akhir elemen `</tagname>`

### 🏗️ Analogi Sederhana: Elemen HTML sebagai Kotak

Bayangkan elemen HTML seperti **kotak penyimpanan**:

```
📦 KOTAK (ELEMEN HTML)
┌─────────────────────────────┐
│ 🏷️ LABEL (Opening Tag)      │
│                             │
│ 📄 ISI KOTAK (Content)      │
│                             │
│ 🏷️ LABEL PENUTUP           │
│    (Closing Tag)            │
└─────────────────────────────┘
```

**Contoh praktis:**
```html
<h1>Judul Halaman</h1>
│   │              │   │
│   │              │   └── Closing tag
│   │              └────── Content
│   └─────────────────────── Opening tag
└─────────────────────────── Elemen lengkap
```

### 🧩 Struktur Elemen HTML

```html
<tagname attribute="value">Content goes here</tagname>
```

**Penjelasan komponen:**
- **tagname**: Nama tag HTML (h1, p, div, dll)
- **attribute**: Properti tambahan untuk elemen
- **value**: Nilai dari attribute
- **Content**: Isi yang akan ditampilkan

### 🔄 Self-Closing Tags

Beberapa tag tidak memerlukan closing tag karena tidak memiliki konten:

```html
<br>      <!-- Line break -->
<hr>      <!-- Horizontal rule -->
<img>     <!-- Image -->
<input>   <!-- Form input -->
<meta>    <!-- Meta information -->
```

### 📚 Nesting (Tag Bersarang)

Elemen HTML dapat berisi elemen lain:

```html
<div>
    <h1>Judul Utama</h1>
    <p>Ini adalah <strong>paragraph</strong> dengan <em>format</em>.</p>
</div>
```

**Aturan Nesting:**
- Tag yang dibuka terakhir harus ditutup lebih dulu
- Jangan menyilangkan tag (incorrect nesting)
- Ikuti hirarki yang logis

---

## 🏷️ 2.2 Apa itu Tag HTML

### 🔍 Definisi Tag HTML

**Tag HTML** adalah penanda yang memberitahu browser bagaimana menampilkan atau memproses konten. Tag ditulis dalam kurung siku `< >`.

### 📝 Sintaks Tag HTML

#### Tag Dasar:
```html
<tagname>content</tagname>
```

#### Tag dengan Atribut:
```html
<tagname attribute1="value1" attribute2="value2">content</tagname>
```

#### Self-closing Tag:
```html
<tagname attribute="value">
```

### 🔤 Case Sensitivity

HTML **tidak case-sensitive**, tapi **best practice** adalah menggunakan **lowercase**:

```html
<!-- ✅ Recommended -->
<h1>Judul</h1>
<p>Paragraph</p>

<!-- ❌ Not recommended -->
<H1>Judul</H1>
<P>Paragraph</P>
```

### 📋 Aturan Penulisan Tag

1. **Selalu tutup tag** yang memerlukan closing tag
2. **Gunakan lowercase** untuk nama tag
3. **Quote attribute values** dengan tanda petik
4. **Proper nesting** - jangan menyilangkan tag
5. **Indentasi yang konsisten** untuk readability

```html
<!-- ✅ Good -->
<div>
    <h1>Judul</h1>
    <p>Paragraph dengan <strong>teks tebal</strong>.</p>
</div>

<!-- ❌ Bad -->
<div>
<h1>Judul</h1>
<p>Paragraph dengan <strong>teks tebal</p></strong>
</div>
```

---

## 📄 2.3 Menampilkan Paragraf HTML

### 🔍 Tag `<p>` untuk Paragraf

Tag [`<p>`](panduan-html/bab-02-elemen-tag-dasar/contoh-kode/paragraf-demo.html:1) digunakan untuk membuat paragraf teks:

```html
<p>Ini adalah paragraf pertama.</p>
<p>Ini adalah paragraf kedua.</p>
<p>Ini adalah paragraf ketiga.</p>
```

### 🎯 Karakteristik Tag `<p>`

1. **Block-level element**: Mengambil lebar penuh container
2. **Auto spacing**: Browser menambahkan margin otomatis
3. **Line wrapping**: Teks akan wrap otomatis jika panjang
4. **Multiple spaces collapsed**: Spasi berlebih akan dijadikan satu

### 📐 Whitespace dan Line Breaks

HTML mengabaikan **multiple spaces** dan **line breaks**:

```html
<!-- Input -->
<p>Teks    dengan    banyak    spasi
dan line break
akan ditampilkan normal.</p>

<!-- Output di browser -->
Teks dengan banyak spasi dan line break akan ditampilkan normal.
```

### 💡 Best Practices Paragraf

```html
<!-- ✅ Good: Paragraf terpisah -->
<p>Paragraf pertama tentang topik A.</p>
<p>Paragraf kedua tentang topik B.</p>

<!-- ❌ Bad: Menggunakan <br> berlebihan -->
<p>Paragraf pertama tentang topik A.<br><br>
Paragraf kedua tentang topik B.</p>
```

### 🎨 Variasi Penggunaan Paragraf

```html
<!-- Paragraf sederhana -->
<p>Paragraf biasa.</p>

<!-- Paragraf dengan formatting -->
<p>Paragraf dengan <strong>teks tebal</strong> dan <em>teks miring</em>.</p>

<!-- Paragraf panjang -->
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris.</p>
```

---

## 🚧 2.4 Memberi Jarak HTML

### 🔀 Tag `<br>` untuk Line Break

Tag [`<br>`](panduan-html/bab-02-elemen-tag-dasar/contoh-kode/spacing-demo.html:5) membuat line break (baris baru):

```html
<p>Baris pertama<br>
Baris kedua<br>
Baris ketiga</p>
```

**Output:**
```
Baris pertama
Baris kedua
Baris ketiga
```

### 📏 Tag `<hr>` untuk Horizontal Rule

Tag [`<hr>`](panduan-html/bab-02-elemen-tag-dasar/contoh-kode/spacing-demo.html:10) membuat garis horizontal pemisah:

```html
<p>Konten bagian pertama</p>
<hr>
<p>Konten bagian kedua</p>
```

### ⚖️ Kapan Menggunakan Spacing Tags

| Tag | Gunakan Untuk | Jangan Gunakan Untuk |
|-----|---------------|----------------------|
| `<br>` | Alamat, puisi, line break dalam teks | Spacing antar paragraf |
| `<hr>` | Pemisah topik, section breaks | Dekorasi visual semata |

### 📝 Contoh Penggunaan yang Benar

```html
<!-- ✅ Good: Alamat -->
<address>
John Doe<br>
123 Main Street<br>
City, State 12345<br>
Email: john@example.com
</address>

<!-- ✅ Good: Puisi -->
<p>
Roses are red<br>
Violets are blue<br>
HTML is awesome<br>
And so are you!
</p>

<!-- ✅ Good: Section separator -->
<p>Konten bagian pertama...</p>
<hr>
<p>Konten bagian kedua...</p>
```

### ❌ Alternatif untuk Spacing

Daripada menggunakan multiple `<br>` untuk spacing:

```html
<!-- ❌ Bad -->
<p>Paragraf 1</p>
<br><br><br>
<p>Paragraf 2</p>

<!-- ✅ Better -->
<p>Paragraf 1</p>
<p>Paragraf 2</p>
<!-- Use CSS for custom spacing -->
```

---

## ✨ 2.5 Format Text HTML

### 💪 Bold Text

#### Tag `<strong>` (Semantic)
```html
<p>Ini adalah <strong>teks penting</strong> yang perlu ditekankan.</p>
```
- **Semantic meaning**: Menunjukkan konten penting
- **SEO friendly**: Search engine memahami importance

#### Tag `<b>` (Visual)
```html
<p>Ini adalah <b>teks tebal</b> untuk tujuan visual.</p>
```
- **Visual only**: Hanya untuk styling visual
- **No semantic meaning**: Tidak ada makna khusus

### 📐 Italic Text

#### Tag `<em>` (Semantic)
```html
<p>Saya <em>sangat senang</em> belajar HTML!</p>
```
- **Emphasis**: Memberikan penekanan pada kata/frase
- **Screen reader friendly**: Dibaca dengan intonasi berbeda

#### Tag `<i>` (Visual)
```html
<p>Nama ilmiah: <i>Homo sapiens</i></p>
```
- **Visual styling**: Untuk nama asing, istilah teknis
- **No emphasis meaning**: Tidak menunjukkan penekanan

### 🔘 Format Text Lainnya

#### Underline `<u>`
```html
<p>Ini adalah <u>teks bergaris bawah</u>.</p>
```

#### Strikethrough `<s>`
```html
<p>Harga lama: <s>Rp 100.000</s> Harga baru: Rp 75.000</p>
```

#### Highlight `<mark>`
```html
<p>Jangan lupa bawa <mark>pulpen</mark> saat ujian.</p>
```

#### Small Text `<small>`
```html
<p>Harga sudah termasuk pajak <small>(PPN 11%)</small>.</p>
```

#### Subscript `<sub>` dan Superscript `<sup>`
```html
<p>Rumus kimia air: H<sub>2</sub>O</p>
<p>Luas persegi: a<sup>2</sup></p>
```

### 🎯 Kombinasi Format Text

```html
<p>
    Dalam matematika, kita sering menggunakan
    <strong>rumus <em>penting</em></strong> seperti
    E=mc<sup>2</sup> dan H<sub>2</sub>O + CO<sub>2</sub>.
    <mark>Ingat</mark> untuk selalu <u>mengecek</u>
    hasil perhitungan Anda!
</p>
```

### 📚 Best Practices Format Text

1. **Gunakan semantic tags** (`<strong>`, `<em>`) daripada visual tags
2. **Jangan overuse**: Terlalu banyak formatting mengganggu readability
3. **Konsisten**: Gunakan format yang sama untuk tujuan yang sama
4. **Accessibility**: Semantic tags lebih baik untuk screen readers

---

## 🎯 2.6 Menampilkan Judul HTML

### 📊 Hierarchy Heading `<h1>` sampai `<h6>`

HTML menyediakan 6 level heading:

```html
<h1>Judul Utama (Level 1)</h1>
<h2>Sub Judul (Level 2)</h2>
<h3>Sub-sub Judul (Level 3)</h3>
<h4>Judul Level 4</h4>
<h5>Judul Level 5</h5>
<h6>Judul Level 6</h6>
```

### 📏 Visual Size Hierarchy

```
H1 ████████████████████ (Terbesar)
H2 ███████████████
H3 ████████████
H4 ██████████
H5 ████████
H6 ██████ (Terkecil)
```

### 🗂️ Kapan Menggunakan Setiap Level

| Level | Penggunaan | Contoh |
|-------|------------|--------|
| `<h1>` | Judul halaman utama | "Panduan Belajar HTML" |
| `<h2>` | Judul bab/section utama | "Elemen HTML Dasar" |
| `<h3>` | Sub-section | "Format Text HTML" |
| `<h4>` | Sub-sub section | "Tag Strong dan Em" |
| `<h5>` | Detail kecil | "Contoh Penggunaan" |
| `<h6>` | Detail tersecil | "Catatan Tambahan" |

### 🔍 SEO dan Accessibility

**Untuk SEO:**
- **Satu `<h1>` per halaman**: Judul utama halaman
- **Hierarchy yang logis**: Jangan skip level (h1→h3)
- **Keywords relevant**: Masukkan kata kunci penting

**Untuk Accessibility:**
- **Screen readers** menggunakan heading untuk navigasi
- **Logical structure** membantu user understand content
- **Descriptive headings** memberikan context yang jelas

### 📝 Contoh Struktur Heading yang Baik

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <title>Panduan Belajar HTML</title>
</head>
<body>
    <h1>Panduan Belajar HTML untuk Pemula</h1>

    <h2>Dasar-dasar HTML</h2>
    <p>Pengenalan konsep HTML...</p>

    <h3>Apa itu Tag HTML?</h3>
    <p>Tag HTML adalah...</p>

    <h3>Struktur HTML Document</h3>
    <p>Setiap dokumen HTML memiliki...</p>

    <h2>Elemen HTML Dasar</h2>
    <p>Elemen-elemen penting yang perlu dipahami...</p>

    <h3>Heading dan Paragraf</h3>
    <p>Cara menggunakan heading...</p>

    <h4>Contoh Penggunaan H1-H6</h4>
    <p>Berikut adalah contoh...</p>
</body>
</html>
```

### ❌ Kesalahan Umum Heading

```html
<!-- ❌ Bad: Skip level -->
<h1>Judul Utama</h1>
<h3>Langsung ke level 3</h3>  <!-- Skip h2 -->

<!-- ❌ Bad: Multiple h1 -->
<h1>Judul Pertama</h1>
<h1>Judul Kedua</h1>  <!-- Sebaiknya h2 -->

<!-- ❌ Bad: Heading for styling only -->
<h1>Teks kecil yang saya buat besar</h1>  <!-- Use CSS instead -->

<!-- ✅ Good: Logical hierarchy -->
<h1>Judul Utama</h1>
<h2>Sub Judul</h2>
<h3>Sub-sub Judul</h3>
```

---

## 🔗 2.7 Membuat Link HTML

### 🌐 Tag `<a>` untuk Link

Tag [`<a>`](panduan-html/bab-02-elemen-tag-dasar/contoh-kode/link-demo.html:1) (anchor) digunakan untuk membuat link:

```html
<a href="https://www.google.com">Kunjungi Google</a>
```

### 🎯 Atribut `href`

**href** (hypertext reference) menentukan tujuan link:

```html
<!-- External link -->
<a href="https://www.wikipedia.org">Wikipedia</a>

<!-- Internal link (same website) -->
<a href="halaman-lain.html">Halaman Lain</a>

<!-- Relative path -->
<a href="../folder/file.html">File di Folder Lain</a>
```

### 🌍 Jenis-jenis Link

#### 1. Link Eksternal
```html
<a href="https://www.github.com">GitHub</a>
<a href="https://www.youtube.com">YouTube</a>
```

#### 2. Link Internal (Same Website)
```html
<a href="about.html">Tentang Kami</a>
<a href="contact.html">Kontak</a>
<a href="gallery.html">Galeri</a>
```

#### 3. Link ke Email
```html
<a href="mailto:someone@example.com">Kirim Email</a>
<a href="mailto:admin@example.com?subject=Pertanyaan">Email dengan Subject</a>
```

#### 4. Link ke Nomor Telepon
```html
<a href="tel:+628123456789">Hubungi Kami</a>
<a href="tel:+62-21-1234567">Telepon Kantor</a>
```

### 🎯 Target Link

#### `target="_blank"` (Buka di Tab Baru)
```html
<a href="https://www.google.com" target="_blank">Google (Tab Baru)</a>
```

#### `target="_self"` (Default - Buka di Tab Same)
```html
<a href="https://www.google.com" target="_self">Google (Tab Sama)</a>
```

