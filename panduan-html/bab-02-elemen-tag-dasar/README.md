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

### ⚓ Anchor Links (Jump to Section)

Link ke bagian tertentu dalam halaman yang sama:

```html
<!-- Link anchor -->
<a href="#section1">Pergi ke Bagian 1</a>
<a href="#section2">Pergi ke Bagian 2</a>

<!-- Target sections -->
<h2 id="section1">Bagian 1</h2>
<p>Konten bagian 1...</p>

<h2 id="section2">Bagian 2</h2>
<p>Konten bagian 2...</p>
```

### 🎨 Link Styling dengan Atribut

```html
<!-- Link dengan title (tooltip) -->
<a href="https://www.google.com" title="Kunjungi Google Search">Google</a>

<!-- Link dengan download attribute -->
<a href="file.pdf" download="panduan-html.pdf">Download PDF</a>

<!-- Link dengan rel attribute -->
<a href="https://external-site.com" rel="noopener noreferrer" target="_blank">
    External Site
</a>
```

### 💡 Best Practices Link

```html
<!-- ✅ Good: Descriptive link text -->
<a href="tutorial.html">Baca tutorial HTML lengkap</a>

<!-- ❌ Bad: Generic link text -->
<a href="tutorial.html">Klik di sini</a>

<!-- ✅ Good: External link with security -->
<a href="https://external-site.com" target="_blank" rel="noopener noreferrer">
    External Website
</a>

<!-- ✅ Good: Email with subject -->
<a href="mailto:support@example.com?subject=Butuh%20bantuan">
    Hubungi Support
</a>
```

---

## 📋 2.8 Menampilkan Daftar HTML

### 📝 Unordered List `<ul>` dan `<li>`

Daftar dengan bullet points:

```html
<ul>
    <li>Item pertama</li>
    <li>Item kedua</li>
    <li>Item ketiga</li>
</ul>
```

**Output:**
- Item pertama
- Item kedua
- Item ketiga

### 🔢 Ordered List `<ol>` dan `<li>`

Daftar dengan numbering:

```html
<ol>
    <li>Langkah pertama</li>
    <li>Langkah kedua</li>
    <li>Langkah ketiga</li>
</ol>
```

**Output:**
1. Langkah pertama
2. Langkah kedua
3. Langkah ketiga

### 🗂️ Nested Lists (Daftar Bersarang)

```html
<ul>
    <li>Frontend Development
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
        </ul>
    </li>
    <li>Backend Development
        <ul>
            <li>PHP</li>
            <li>Python</li>
            <li>Node.js</li>
        </ul>
    </li>
</ul>
```

### 🎨 Styling List dengan Atribut

#### Ordered List dengan Custom Numbering
```html
<!-- Start from number 5 -->
<ol start="5">
    <li>Item kelima</li>
    <li>Item keenam</li>
</ol>

<!-- Roman numerals -->
<ol type="I">
    <li>Item I</li>
    <li>Item II</li>
</ol>

<!-- Alphabetical -->
<ol type="A">
    <li>Item A</li>
    <li>Item B</li>
</ol>
```

#### Unordered List dengan Custom Bullets
```html
<!-- No bullets -->
<ul style="list-style-type: none;">
    <li>Item tanpa bullet</li>
    <li>Item tanpa bullet</li>
</ul>
```

### 📚 Definition List `<dl>`, `<dt>`, `<dd>`

Untuk daftar definisi:

```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>

    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>

    <dt>JS</dt>
    <dd>JavaScript programming language</dd>
</dl>
```

### 💼 Use Cases Praktis

#### Navigation Menu
```html
<ul>
    <li><a href="home.html">Beranda</a></li>
    <li><a href="about.html">Tentang</a></li>
    <li><a href="services.html">Layanan</a></li>
    <li><a href="contact.html">Kontak</a></li>
</ul>
```

#### Tutorial Steps
```html
<ol>
    <li>Buka VS Code</li>
    <li>Buat file baru dengan ekstensi .html</li>
    <li>Tulis struktur HTML dasar</li>
    <li>Save file dan buka di browser</li>
</ol>
```

#### Feature List
```html
<ul>
    <li>✅ Responsive design</li>
    <li>✅ Mobile friendly</li>
    <li>✅ SEO optimized</li>
    <li>✅ Fast loading</li>
</ul>
```

---

## 📊 2.9 Membuat Tabel di HTML

### 🏗️ Struktur Dasar Tabel

Tabel HTML menggunakan kombinasi tag:
- [`<table>`](panduan-html/bab-02-elemen-tag-dasar/contoh-kode/tabel-demo.html:1): Container utama
- [`<tr>`](panduan-html/bab-02-elemen-tag-dasar/contoh-kode/tabel-demo.html:3): Table row (baris)
- [`<td>`](panduan-html/bab-02-elemen-tag-dasar/contoh-kode/tabel-demo.html:4): Table data (cell)

```html
<table>
    <tr>
        <td>Baris 1, Kolom 1</td>
        <td>Baris 1, Kolom 2</td>
    </tr>
    <tr>
        <td>Baris 2, Kolom 1</td>
        <td>Baris 2, Kolom 2</td>
    </tr>
</table>
```

### 🎯 Table Headers `<th>`

Untuk header kolom/baris:

```html
<table>
    <tr>
        <th>Nama</th>
        <th>Umur</th>
        <th>Kelas</th>
    </tr>
    <tr>
        <td>John</td>
        <td>16</td>
        <td>XI IPA</td>
    </tr>
    <tr>
        <td>Jane</td>
        <td>17</td>
        <td>XI IPS</td>
    </tr>
</table>
```

### 🏢 Table Sections

Struktur tabel yang lebih semantic:

```html
<table>
    <thead>
        <tr>
            <th>Mata Pelajaran</th>
            <th>Nilai</th>
            <th>Grade</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Matematika</td>
            <td>85</td>
            <td>A</td>
        </tr>
        <tr>
            <td>Bahasa Indonesia</td>
            <td>90</td>
            <td>A</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td><strong>Rata-rata</strong></td>
            <td><strong>87.5</strong></td>
            <td><strong>A</strong></td>
        </tr>
    </tfoot>
</table>
```

### 📏 Colspan dan Rowspan

#### Colspan (Merge Columns)
```html
<table>
    <tr>
        <th>Nama</th>
        <th colspan="2">Nilai</th>
    </tr>
    <tr>
        <td>John</td>
        <td>UTS: 85</td>
        <td>UAS: 90</td>
    </tr>
</table>
```

#### Rowspan (Merge Rows)
```html
<table>
    <tr>
        <td rowspan="2">XI IPA</td>
        <td>John</td>
        <td>85</td>
    </tr>
    <tr>
        <td>Jane</td>
        <td>90</td>
    </tr>
</table>
```

### 📝 Caption dan Summary

```html
<table>
    <caption>Daftar Nilai Siswa Kelas XI IPA</caption>
    <thead>
        <tr>
            <th>No</th>
            <th>Nama</th>
            <th>Nilai</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>John Doe</td>
            <td>85</td>
        </tr>
    </tbody>
</table>
```

### 📊 Contoh Tabel Kompleks

```html
<table border="1" style="border-collapse: collapse;">
    <caption>Jadwal Pelajaran Kelas XI IPA 1</caption>
    <thead>
        <tr>
            <th>Waktu</th>
            <th>Senin</th>
            <th>Selasa</th>
            <th>Rabu</th>
            <th>Kamis</th>
            <th>Jumat</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>07:00 - 08:30</td>
            <td>Matematika</td>
            <td>Bahasa Indonesia</td>
            <td>Fisika</td>
            <td>Kimia</td>
            <td>Biologi</td>
        </tr>
        <tr>
            <td>08:30 - 10:00</td>
            <td>Bahasa Inggris</td>
            <td>Matematika</td>
            <td>Bahasa Indonesia</td>
            <td>Fisika</td>
            <td>Kimia</td>
        </tr>
        <tr>
            <td>10:15 - 11:45</td>
            <td colspan="5" style="text-align: center;">ISTIRAHAT</td>
        </tr>
        <tr>
            <td>11:45 - 13:15</td>
            <td>Sejarah</td>
            <td>PKn</td>
            <td>Olahraga</td>
            <td>Seni</td>
            <td>Agama</td>
        </tr>
    </tbody>
</table>
```

---

## 💬 2.10 Menampilkan Quote di HTML

### 📖 Blockquote `<blockquote>`

Untuk quote yang panjang atau standalone:

```html
<blockquote>
    <p>HTML adalah bahasa markup yang digunakan untuk membuat struktur halaman web. Dengan HTML, kita dapat menampilkan teks, gambar, link, dan berbagai elemen multimedia lainnya.</p>
    <cite>- Panduan Belajar HTML</cite>
</blockquote>
```

### 💭 Inline Quote `<q>`

Untuk quote pendek di dalam paragraf:

```html
<p>
    Seperti yang dikatakan Albert Einstein:
    <q>Imagination is more important than knowledge.</q>
</p>
```

### 📚 Citation `<cite>`

Untuk mereferensikan sumber:

```html
<p>
    Menurut buku <cite>HTML dan CSS untuk Pemula</cite>,
    tag semantic sangat penting untuk SEO.
</p>

<blockquote>
    <p>The best way to learn HTML is by practicing.</p>
    <cite>John Doe, Web Developer</cite>
</blockquote>
```

### 🏠 Address `<address>`

Untuk informasi kontak:

```html
<address>
    <strong>SMA Negeri 1 Jakarta</strong><br>
    Jl. Merdeka No. 123<br>
    Jakarta Pusat, 10110<br>
    Email: <a href="mailto:info@sma1jkt.sch.id">info@sma1jkt.sch.id</a><br>
    Telepon: <a href="tel:+62211234567">(021) 123-4567</a>
</address>
```

### 🎨 Kombinasi Quote Elements

```html
<article>
    <h2>Pentingnya Belajar HTML</h2>
    <p>HTML adalah fondasi dari semua website.</p>

    <blockquote>
        <p>
            <q>HTML bukanlah bahasa pemrograman,</q> kata ahli web development,
            <q>tetapi bahasa markup yang sangat penting untuk dipahami.</q>
        </p>
        <cite>- Jane Smith, Frontend Developer</cite>
    </blockquote>

    <p>
        Untuk mempelajari lebih lanjut, baca buku
        <cite>Mastering HTML and CSS</cite> karya John Doe.
    </p>

    <address>
        Artikel ini ditulis oleh:<br>
        <strong>Tim Pengajar SMA</strong><br>
        Email: <a href="mailto:guru@sma.sch.id">guru@sma.sch.id</a>
    </address>
</article>
```

---

## 💻 2.11 Menampilkan Code di HTML

### 🔤 Inline Code `<code>`

Untuk kode pendek di dalam teks:

```html
<p>
    Untuk membuat paragraf HTML, gunakan tag <code>&lt;p&gt;</code>
    dan tutup dengan <code>&lt;/p&gt;</code>.
</p>
```

### 📄 Code Block `<pre>`

Untuk blok kode dengan format tetap:

```html
<pre>
<code>
function helloWorld() {
    console.log("Hello, World!");
}

helloWorld();
</code>
</pre>
```

### ⌨️ Keyboard Input `<kbd>`

Untuk menunjukkan input keyboard:

```html
<p>
    Untuk save file, tekan <kbd>Ctrl</kbd> + <kbd>S</kbd>.
    Untuk copy teks, tekan <kbd>Ctrl</kbd> + <kbd>C</kbd>.
</p>
```

### 📺 Sample Output `<samp>`

Untuk menunjukkan output program:

```html
<p>Ketika program dijalankan, output yang dihasilkan adalah:</p>
<samp>
Hello, World!<br>
Program selesai dieksekusi.
</samp>
```

### 🔢 Variable `<var>`

Untuk menunjukkan variable atau nilai matematik:

```html
<p>
    Rumus luas lingkaran adalah π <var>r</var><sup>2</sup>,
    dimana <var>r</var> adalah jari-jari lingkaran.
</p>

<p>
    Dalam persamaan <var>y</var> = <var>mx</var> + <var>c</var>,
    <var>m</var> adalah gradien dan <var>c</var> adalah konstanta.
</p>
```

### 🎯 Kombinasi Code Elements

```html
<article>
    <h2>Tutorial JavaScript Dasar</h2>

    <p>
        Untuk membuat fungsi JavaScript, gunakan keyword
        <code>function</code> diikuti nama fungsi.
    </p>

    <pre>
<code>
function calculateArea(radius) {
    const pi = 3.14159;
    return pi * radius * radius;
}

let result = calculateArea(5);
console.log(result);
</code>
    </pre>

    <p>
        Untuk menjalankan kode di atas, simpan dalam file
        <code>script.js</code> dan tekan <kbd>F5</kbd> di browser.
    </p>

    <p>Output yang dihasilkan:</p>
    <samp>78.53975</samp>

    <p>
        Variabel <var>pi</var> menyimpan nilai konstanta,
        sedangkan <var>radius</var> adalah parameter fungsi.
    </p>
</article>
```

### 💡 Tips Menampilkan HTML Code

Untuk menampilkan kode HTML di dalam HTML:

```html
<p>Contoh tag paragraf:</p>
<pre>
<code>
&lt;p&gt;Ini adalah paragraf HTML.&lt;/p&gt;
&lt;h1&gt;Ini adalah heading.&lt;/h1&gt;
&lt;a href="link.html"&gt;Ini adalah link.&lt;/a&gt;
</code>
</pre>
```

**HTML Entities untuk Code:**
- `&lt;` untuk `<`
- `&gt;` untuk `>`
- `&amp;` untuk `&`
- `&quot;` untuk `"`

---

## ⏰ 2.12 Menampilkan Waktu di HTML

### 📅 Tag `<time>` untuk Datetime

Tag [`<time>`](panduan-html/bab-02-elemen-tag-dasar/contoh-kode/time-demo.html:1) menandai waktu atau tanggal:

```html
<time>2024-01-15</time>
<time>14:30</time>
<time datetime="2024-01-15T14:30:00">15 Januari 2024, 14:30</time>
```

### 🕐 Format Datetime

#### Tanggal (YYYY-MM-DD)
```html
<time datetime="2024-01-15">15 Januari 2024</time>
<time datetime="2024-12-31">Akhir tahun 2024</time>
```

#### Waktu (HH:MM atau HH:MM:SS)
```html
<time datetime="14:30">Jam 2 siang</time>
<time datetime="09:00:00">Pukul 9 pagi</time>
```

#### Datetime Lengkap (YYYY-MM-DDTHH:MM:SS)
```html
<time datetime="2024-01-15T14:30:00">
    15 Januari 2024 pukul 14:30
</time>
```

#### Dengan Timezone
```html
<time datetime="2024-01-15T14:30:00+07:00">
    15 Januari 2024, 14:30 WIB
</time>
```

### 📆 Use Cases Praktis

#### Artikel Blog
```html
<article>
    <h2>Tips Belajar HTML</h2>
    <p>
        Published on
        <time datetime="2024-01-15">January 15, 2024</time>
    </p>
    <p>
        Last updated:
        <time datetime="2024-01-20">January 20, 2024</time>
    </p>
</article>
```

#### Event Schedule
```html
<div>
    <h3>Workshop HTML untuk Pemula</h3>
    <p>
        Tanggal: <time datetime="2024-02-10">10 Februari 2024</time><br>
        Waktu: <time datetime="09:00">09:00</time> -
               <time datetime="12:00">12:00</time><br>
        Durasi: <time datetime="PT3H">3 jam</time>
    </p>
</div>
```

#### Deadline Assignment
```html
<div>
    <h4>Tugas HTML Dasar</h4>
    <p>
        Deadline:
        <time datetime="2024-01-30T23:59:59">
            30 Januari 2024, 23:59
        </time>
    </p>
</div>
```

### 🌍 Durasi dan Periode

```html
<!-- Durasi 2 jam 30 menit -->
<time datetime="PT2H30M">2 jam 30 menit</time>

<!-- Periode 1 minggu -->
<time datetime="P7D">1 minggu</time>

<!-- Periode 1 bulan -->
<time datetime="P1M">1 bulan</time>
```

### 💡 Benefits Tag `<time>`

1. **SEO**: Search engines memahami waktu/tanggal
2. **Accessibility**: Screen readers bisa membaca dengan benar
3. **Microdata**: Dapat digunakan untuk structured data
4. **JavaScript**: Mudah diakses untuk manipulasi waktu

---

## 📋 2.13 Menampilkan Detail di HTML

### 🔽 Tag `<details>` dan `<summary>`

Tag [`<details>`](panduan-html/bab-02-elemen-tag-dasar/contoh-kode/details-demo.html:1) membuat konten yang dapat dibuka/tutup:

```html
<details>
    <summary>Klik untuk melihat detail</summary>
    <p>Ini adalah konten detail yang tersembunyi secara default.</p>
</details>
```

### 📖 Basic Usage

```html
<details>
    <summary>Apa itu HTML?</summary>
    <p>
        HTML (HyperText Markup Language) adalah bahasa markup
        yang digunakan untuk membuat struktur halaman web.
    </p>
</details>

<details>
    <summary>Apa itu CSS?</summary>
    <p>
        CSS (Cascading Style Sheets) adalah bahasa stylesheet
        yang digunakan untuk mengatur tampilan halaman web.
    </p>
</details>
```

### 🎯 Advanced Usage

#### Detail dengan List
```html
<details>
    <summary>Langkah-langkah Belajar HTML</summary>
    <ol>
        <li>Pahami konsep dasar HTML</li>
        <li>Praktik membuat file HTML sederhana</li>
        <li>Pelajari berbagai tag HTML</li>
        <li>Buat proyek website pertama</li>
    </ol>
</details>
```

#### Detail dengan Tabel
```html
<details>
    <summary>Daftar Tag HTML Dasar</summary>
    <table border="1">
        <tr>
            <th>Tag</th>
            <th>Fungsi</th>
        </tr>
        <tr>
            <td>&lt;h1&gt;</td>
            <td>Heading utama</td>
        </tr>
        <tr>
            <td>&lt;p&gt;</td>
            <td>Paragraf</td>
        </tr>
        <tr>
            <td>&lt;a&gt;</td>
            <td>Link</td>
        </tr>
    </table>
</details>
```

#### Detail dengan Code
```html
<details>
    <summary>Contoh Kode HTML Sederhana</summary>
    <pre>
<code>
&lt;!DOCTYPE html&gt;
&lt;html lang="id"&gt;
&lt;head&gt;
    &lt;title&gt;Hello World&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Hello World!&lt;/h1&gt;
&lt;/body&gt;
&lt;/html&gt;
</code>
    </pre>
</details>
```

### 🎨 Detail dengan Attribute `open`

Detail terbuka secara default:

```html
<details open>
    <summary>Informasi Penting (Terbuka Default)</summary>
    <p>Konten ini terlihat secara default karena ada atribut 'open'.</p>
</details>
```

### 📚 Use Cases Praktis

#### FAQ Section
```html
<h2>Frequently Asked Questions</h2>

<details>
    <summary>Bagaimana cara belajar HTML dengan efektif?</summary>
    <p>
        Cara terbaik belajar HTML adalah dengan praktek langsung.
        Mulai dari struktur dasar, lalu pelajari berbagai tag secara bertahap.
    </p>
</details>

<details>
    <summary>Apakah HTML sulit dipelajari?</summary>
    <p>
        HTML relatif mudah dipelajari karena sintaksnya sederhana dan logis.
        Dengan praktek rutin, Anda bisa menguasainya dalam beberapa minggu.
    </p>
</details>

<details>
    <summary>Tools apa saja yang diperlukan untuk HTML?</summary>
    <p>
        Anda hanya memerlukan text editor (seperti VS Code) dan web browser.
        Tidak perlu software khusus yang mahal.
    </p>
</details>
```

#### Course Outline
```html
<h2>Materi Pelajaran HTML</h2>

<details>
    <summary>Bab 1: Pengenalan HTML</summary>
    <ul>
        <li>Apa itu HTML?</li>
        <li>Sejarah HTML</li>
        <li>Setup environment</li>
        <li>HTML pertama Anda</li>
    </ul>
</details>

<details>
    <summary>Bab 2: Elemen HTML Dasar</summary>
    <ul>
        <li>Tag dan elemen</li>
        <li>Heading dan paragraf</li>
        <li>Link dan navigasi</li>
        <li>List dan tabel</li>
    </ul>
</details>
```

### ♿ Accessibility Considerations

```html
<details>
    <summary role="button" aria-expanded="false">
        Detail dengan accessibility
    </summary>
    <p>
        Konten ini dapat diakses dengan baik oleh screen readers
        dan teknologi assistive lainnya.
    </p>
</details>
```

### 🌐 Browser Support

- ✅ Chrome 12+
- ✅ Firefox 49+
- ✅ Safari 6+
- ✅ Edge 79+
- ❌ Internet Explorer (not supported)

---

## 💭 2.14 Komentar di HTML

### 📝 Sintaks Komentar `<!-- -->`

Komentar HTML tidak ditampilkan di browser:

```html
<!-- Ini adalah komentar HTML -->
<h1>Judul yang terlihat</h1>
<!-- Komentar ini juga tidak terlihat -->
```

### 🎯 Kapan Menggunakan Komentar

#### 1. Dokumentasi Kode
```html
<!-- Header Section -->
<header>
    <h1>Judul Website</h1>
    <nav>
        <!-- Navigation menu -->
        <ul>
            <li><a href="home.html">Home</a></li>
            <li><a href="about.html">About</a></li>
        </ul>
    </nav>
</header>

<!-- Main Content -->
<main>
    <h2>Konten Utama</h2>
    <p>Paragraf konten...</p>
</main>
```

#### 2. Temporary Disable Code
```html
<p>Paragraf yang aktif</p>
<!--
<p>Paragraf yang di-comment sementara</p>
<p>Untuk testing atau development</p>
-->
<p>Paragraf yang aktif lagi</p>
```

#### 3. Development Notes
```html
<!-- TODO: Tambahkan gambar di sini -->
<div>
    <h3>Galeri</h3>
    <!-- FIXME: Link gambar belum benar -->
    <!-- <img src="image.jpg" alt="Gambar"> -->
</div>
```

### 📋 Best Practices Komentar

#### ✅ Good Comments
```html
<!-- Hero Section - Main banner area -->
<section class="hero">
    <h1>Welcome to Our Website</h1>
</section>

<!-- Contact Form - Updated 2024-01-15 -->
<form action="contact.php" method="post">
    <!-- User input fields -->
    <input type="text" name="name" required>
    <input type="email" name="email" required>
</form>

<!-- Footer Section -->
<footer>
    <!-- Copyright notice -->
    <p>&copy; 2024 Company Name</p>
</footer>
```

#### ❌ Poor Comments
```html
<!-- h1 tag -->
<h1>Title</h1>  <!-- This comment doesn't add value -->

<!-- div -->
<div>  <!-- Obvious comment -->
    <p>Content</p>  <!-- p tag -->
</div>  <!-- end div -->
```

### 📝 Multi-line Comments

```html
<!--
    Ini adalah komentar multi-line
    yang dapat mencakup beberapa baris
    untuk menjelaskan kode yang kompleks

    Author: John Doe
    Date: 2024-01-15
    Purpose: Contact form section
-->
<form>
    <!-- Form content here -->
</form>
```

### 🔧 Conditional Comments (Legacy IE)

```html
<!-- [if IE]>
    <p>Anda menggunakan Internet Explorer</p>
<![endif] -->

<!--[if IE 8]>
    <link rel="stylesheet" type="text/css" href="ie8.css">
<![endif]-->
```

### 💡 Tips Menggunakan Komentar

1. **Be Descriptive**: Jelaskan "mengapa" bukan "apa"
2. **Keep Updated**: Hapus komentar yang sudah tidak relevan
3. **Team Communication**: Gunakan untuk komunikasi tim
4. **Version Control**: Catat perubahan penting

```html
<!--
    Version 2.1 - Added responsive navigation
    Changed: 2024-01-15
    By: Jane Smith

    Next updates:
    - Add dark mode toggle
    - Optimize images
-->
<nav class="responsive-nav">
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
    </ul>
</nav>
```

### 🚫 Security Note

**Jangan letakkan informasi sensitif dalam komentar:**

```html
<!-- ❌ JANGAN LAKUKAN INI -->
<!-- Database password: secret123 -->
<!-- API key: abc123xyz -->

<!-- ✅ AMAN -->
<!-- Contact form uses reCAPTCHA for spam protection -->
```

---

## 🏗️ Proyek Mini Bab 2

### 🎯 Membuat Halaman Profil Siswa Lengkap

**Objective:** Membuat halaman profil yang menggunakan semua elemen HTML yang telah dipelajari

#### 📋 Requirements:
1. Struktur HTML yang benar dengan semua meta tags
2. Heading hierarchy yang logis (h1-h3)
3. Paragraf dengan format text (strong, em, mark)
4. Link internal dan eksternal dengan target yang sesuai
5. Daftar hobi (unordered) dan prestasi (ordered)
6. Tabel jadwal atau nilai
7. Quote dari tokoh inspiratif
8. Code snippet sederhana (jika ada skill programming)
9. Waktu/tanggal menggunakan tag time
10. FAQ section dengan details/summary
11. Komentar HTML untuk dokumentasi

#### 🎨 Template Proyek:

Buat file [`proyek-profil-lengkap.html`](panduan-html/bab-02-elemen-tag-dasar/proyek-mini/proyek-profil-lengkap.html):

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Profil lengkap siswa dengan berbagai elemen HTML">
    <meta name="author" content="[Nama Anda]">
    <title>Profil Lengkap - [Nama Anda]</title>
</head>
<body>
    <!-- Header Section -->
    <header>
        <h1>Profil Lengkap: [Nama Anda]</h1>
        <p><em>Siswa SMA yang passionate dengan teknologi</em></p>
    </header>

    <!-- Navigation -->
    <nav>
        <ul>
            <li><a href="#tentang">Tentang</a></li>
            <li><a href="#hobi">Hobi</a></li>
            <li><a href="#prestasi">Prestasi</a></li>
            <li><a href="#jadwal">Jadwal</a></li>
            <li><a href="#faq">FAQ</a></li>
        </ul>
    </nav>

    <!-- About Section -->
    <section id="tentang">
        <h2>Tentang Saya</h2>
        <p>Halo! Saya <strong>[Nama Anda]</strong>, siswa kelas <strong>[Kelas]</strong>
        di <em>[Nama Sekolah]</em>. Saya sangat <mark>tertarik dengan teknologi</mark>
        dan sedang belajar web development.</p>

        <p>Saya percaya seperti yang dikatakan <q>Steve Jobs: Innovation distinguishes
        between a leader and a follower.</q></p>
    </section>

    <!-- Quote Section -->
    <section>
        <h2>Quote Inspiratif</h2>
        <blockquote>
            <p>The best time to plant a tree was 20 years ago. The second best time is now.</p>
            <cite>- Chinese Proverb</cite>
        </blockquote>
    </section>

    <!-- Hobbies -->
    <section id="hobi">
        <h2>Hobi dan Minat</h2>
        <h3>Hobi Utama:</h3>
        <ul>
            <li>💻 <strong>Programming</strong> - HTML, CSS, JavaScript</li>
            <li>📚 <strong>Membaca</strong> - Novel fiksi dan non-fiksi</li>
            <li>🎮 <strong>Gaming</strong> - Strategy dan puzzle games</li>
            <li>🎵 <strong>Musik</strong> - Mendengarkan dan belajar gitar</li>
        </ul>

        <!-- Programming Skills -->
        <h3>Skill Programming:</h3>
        <p>Saya baru belajar HTML dan sudah bisa membuat struktur dasar:</p>
        <pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="id"&gt;
&lt;head&gt;
    &lt;title&gt;My Website&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Hello World!&lt;/h1&gt;
&lt;/body&gt;
&lt;/html&gt;</code></pre>

        <p>Untuk menjalankan kode HTML, saya menggunakan shortcut <kbd>Ctrl</kbd> + <kbd>O</kbd>
        di browser.</p>
    </section>

    <!-- Achievements -->
    <section id="prestasi">
        <h2>Prestasi dan Pencapaian</h2>
        <h3>Prestasi Akademik:</h3>
        <ol>
            <li><strong>Juara 2</strong> - Olimpiade Matematika Tingkat Sekolah <time datetime="2023-05">Mei 2023</time></li>
            <li><strong>Peringkat 5 Besar</strong> - Ulangan Harian Fisika <time datetime="2023-09">September 2023</time></li>
            <li><strong>Sertifikat</strong> - Workshop HTML untuk Pemula <time datetime="2024-01">Januari 2024</time></li>
        </ol>

        <h3>Aktivitas Ekstrakurikuler:</h3>
        <ol>
            <li>Anggota <strong>Klub Komputer</strong> sejak <time datetime="2023-08">Agustus 2023</time></li>
            <li>Volunteer <strong>Event Sekolah</strong> <time datetime="2023-12">Desember 2023</time></li>
        </ol>
    </section>

    <!-- Schedule -->
    <section id="jadwal">
        <h2>Jadwal Belajar Mingguan</h2>
        <table border="1" style="border-collapse: collapse;">
            <caption>Jadwal Belajar Mandiri di Rumah</caption>
            <thead>
                <tr>
                    <th>Waktu</th>
                    <th>Senin</th>
                    <th>Selasa</th>
                    <th>Rabu</th>
                    <th>Kamis</th>
                    <th>Jumat</th>
                    <th>Weekend</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><time datetime="19:00">19:00-20:00</time></td>
                    <td>Matematika</td>
                    <td>Fisika</td>
                    <td>Kimia</td>
                    <td>B. Indonesia</td>
                    <td>B. Inggris</td>
                    <td rowspan="2">Proyek HTML</td>
                </tr>
                <tr>
                    <td><time datetime="20:00">20:00-21:00</time></td>
                    <td>HTML/CSS</td>
                    <td>Membaca</td>
                    <td>HTML/CSS</td>
                    <td>Membaca</td>
                    <td>Review</td>
                </tr>
            </tbody>
        </table>
    </section>

    <!-- Time and Dates -->
    <section>
        <h2>Timeline Belajar HTML</h2>
        <ul>
            <li><time datetime="2024-01-01">1 Januari 2024</time> - Mulai belajar HTML dasar</li>
            <li><time datetime="2024-01-15">15 Januari 2024</time> - Menguasai tag-tag dasar</li>
            <li><time datetime="2024-02-01">1 Februari 2024</time> - Target: Buat website pertama</li>
            <li><time datetime="2024-03-01">1 Maret 2024</time> - Target: Mulai belajar CSS</li>
        </ul>
    </section>

    <!-- FAQ Section -->
    <section id="faq">
        <h2>Frequently Asked Questions</h2>

        <details>
            <summary>Mengapa saya tertarik dengan web development?</summary>
            <p>Saya tertarik dengan web development karena ingin bisa <strong>membuat website</strong>
            sendiri dan berkarya di bidang teknologi. Web development juga memiliki prospek
            karir yang bagus di era digital ini.</p>
        </details>

        <details>
            <summary>Bagaimana cara saya belajar HTML?</summary>
            <p>Saya belajar HTML melalui:</p>
            <ul>
                <li>Tutorial online dan video YouTube</li>
                <li>Praktek langsung dengan VS Code</li>
                <li>Bergabung dengan komunitas developer</li>
                <li>Membaca dokumentasi resmi</li>
            </ul>
        </details>

        <details>
            <summary>Apa target saya ke depan?</summary>
            <p>Target jangka pendek saya adalah menguasai <em>HTML dan CSS</em> dengan baik.
            Jangka panjang, saya ingin menjadi <strong>full-stack developer</strong> dan
            bisa membuat aplikasi web yang kompleks.</p>
        </details>

        <details>
            <summary>Bagaimana teman-teman bisa menghubungi saya?</summary>
            <address>
                <strong>[Nama Anda]</strong><br>
                Email: <a href="mailto:nama@email.com">nama@email.com</a><br>
                Instagram: <a href="https://instagram.com/username" target="_blank">@username</a><br>
                GitHub: <a href="https://github.com/username" target="_blank">github.com/username</a>
            </address>
        </details>
    </section>

    <!-- Footer -->
    <footer>
        <hr>
        <p>
            <small>
                Halaman ini dibuat dengan ❤️ menggunakan HTML.<br>
                Last updated: <time datetime="2024-01-15">15 Januari 2024</time>
            </small>
        </p>
    </footer>

    <!--
    TODO untuk pengembangan selanjutnya:
    - Tambahkan CSS untuk styling
    - Optimasi untuk mobile device
    - Tambahkan JavaScript untuk interaksi
    - Upload gambar profil
    -->

</body>
</html>
```

#### ✅ Checklist Penyelesaian:
- [ ] Struktur HTML lengkap dengan meta tags
- [ ] Heading hierarchy logis (h1, h2, h3)
- [ ] Paragraf dengan format text (strong, em, mark)
- [ ] Link dengan target="_blank" untuk external
- [ ] Anchor links untuk navigasi internal
- [ ] Unordered list untuk hobi
- [ ] Ordered list untuk prestasi
- [ ] Tabel dengan thead, tbody, caption
- [ ] Blockquote dan inline quote
- [ ] Code snippet dengan pre dan code
- [ ] Tag time untuk tanggal/waktu
- [
