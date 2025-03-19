# Laporan Proyek Website Personal

## Deskripsi Proyek

Proyek ini merupakan implementasi website personal/portfolio menggunakan HTML dan CSS dengan tambahan JavaScript untuk fungsionalitas interaktif. Website ini dibuat untuk memenuhi tugas mata kuliah dan berfungsi sebagai portfolio online yang menampilkan informasi pribadi, keahlian, proyek, dan kontak.

### Tujuan
- Membuat website personal yang responsif untuk berbagai ukuran perangkat
- Menerapkan konsep semantik HTML dan CSS modern
- Mengimplementasikan fitur interaktif dengan JavaScript
- Membuat desain yang menarik dan profesional

### Fitur Utama
1. **Navigasi Responsif**: Menu navigasi yang menyesuaikan dengan ukuran layar
2. **Mode Gelap (Dark Mode)**: Fitur untuk mengganti tema website menjadi gelap
3. **Halaman Beranda**: Menampilkan informasi utama dan foto profil
4. **Halaman Tentang**: Berisi informasi detail tentang diri
5. **Halaman Keahlian**: Menampilkan keahlian dengan visualisasi progress bar
6. **Halaman Portfolio**: Menampilkan proyek-proyek dengan fitur filter kategori
7. **Halaman Kontak**: Form kontak dan informasi kontak lainnya
8. **Animasi & Efek**: Berbagai efek hover dan animasi untuk meningkatkan UX

### Teknologi yang Digunakan
- **HTML5**: Struktur semantik website
- **CSS3**: Styling dan layout (Flexbox, Grid, Media Queries)
- **JavaScript**: Interaktivitas dan fungsionalitas (Dark mode, filter portfolio)
- **Font Awesome**: Untuk ikon-ikon pada website
- **Google Fonts**: Untuk typography (Poppins)
- **LocalStorage API**: Menyimpan preferensi tema pengguna

## Struktur Folder dan File

```
├── index.html              # Halaman utama
├── about.html              # Halaman tentang
├── skills.html             # Halaman keahlian
├── portfolio.html          # Halaman portfolio
├── contact.html            # Halaman kontak
├── css/
│   └── style.css           # File CSS utama
├── js/
│   └── script.js           # File JavaScript
└── images/                 # Folder untuk gambar
    ├── profile.jpg         # Foto profil
    ├── about.jpg           # Gambar halaman about
    ├── project1.webp       # Gambar proyek 1
    ├── project2.webp       # Gambar proyek 2
    ├── project3.webp       # Gambar proyek 3
    ├── project4.webp       # Gambar proyek 4
    ├── project5.webp       # Gambar proyek 5
    └── project6.webp       # Gambar proyek 6
```

## Penjelasan Kode

### HTML
Website ini menggunakan struktur HTML5 semantik dengan tag seperti `<header>`, `<nav>`, `<main>`, `<section>`, dan `<footer>` untuk meningkatkan aksesibilitas dan SEO. Setiap halaman memiliki struktur dasar yang konsisten:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Meta tags, title, dan link stylesheet -->
</head>
<body>
    <header>
        <!-- Logo dan navigasi -->
    </header>

    <main>
        <!-- Konten spesifik halaman -->
    </main>

    <footer>
        <!-- Informasi copyright -->
    </footer>
    
    <!-- Script JavaScript -->
</body>
</html>
```

### CSS
CSS dibuat dengan pendekatan modular dan responsif:

1. **Variabel CSS**: Menggunakan variabel CSS untuk tema (light/dark) dan konsistensi warna
2. **Flexbox & Grid**: Untuk layout yang responsif dan modern
3. **Media Queries**: Untuk adaptasi ke berbagai ukuran layar
4. **Transisi & Animasi**: Untuk efek visual yang menarik
5. **Responsivitas**: Website berfungsi dengan baik pada berbagai ukuran layar

### JavaScript
JavaScript digunakan untuk menambahkan fungsionalitas interaktif:

1. **Dark Mode Toggle**: Perpindahan antara tema terang dan gelap
2. **Portfolio Filter**: Memfilter proyek berdasarkan kategori
3. **Form Validation**: Validasi formulir kontak
4. **Scroll Animation**: Efek muncul saat scrolling
5. **LocalStorage**: Menyimpan preferensi tema pengguna

## Responsive Design

Website dirancang dengan pendekatan mobile-first dan responsif pada berbagai ukuran layar:

1. **Mobile** (< 576px): Tata letak satu kolom, menu navigasi stack
2. **Tablet** (576px - 992px): Dua kolom untuk beberapa bagian
3. **Desktop** (> 992px): Multi-kolom layout dengan spacing optimal

Responsivitas dicapai melalui:
- Penggunaan unit relatif (%, rem, em)
- Media queries untuk breakpoint utama
- Flexbox dan Grid untuk layout adaptif
- Gambar responsif dengan `max-width: 100%`

## Kesimpulan dan Pembelajaran

Dalam pembuatan proyek ini, beberapa hal yang dipelajari:

1. Pentingnya perencanaan desain sebelum mulai coding
2. Manfaat penggunaan semantik HTML untuk struktur yang jelas
3. Kelebihan CSS modern (variabel, flexbox, grid) untuk layout yang kompleks
4. Implementasi fitur dark mode menggunakan CSS variables dan JavaScript
5. Teknik untuk membuat website responsif pada berbagai perangkat
6. Optimasi pengalaman pengguna dengan animasi CSS dan JavaScript

## Tantangan dan Solusi

Beberapa tantangan dalam pengembangan proyek ini:

1. **Responsivitas**: Memastikan tampilan konsisten di berbagai ukuran layar
   - Solusi: Penggunaan media queries dan layout flexbox/grid
   
2. **Dark Mode**: Implementasi toggle tema tanpa mengganggu UX
   - Solusi: Menggunakan CSS variables dan LocalStorage untuk menyimpan preferensi

3. **Portfolio Filter**: Membuat filter kategori yang smooth
   - Solusi: Kombinasi CSS transitions dan JavaScript untuk animasi smooth

## Pengembangan Ke Depan

Untuk pengembangan selanjutnya, beberapa hal yang dapat ditambahkan:

1. Animasi yang lebih kompleks menggunakan GSAP atau libraries lain
2. Integrasi dengan backend untuk form kontak yang berfungsi
3. Implementasi Progressive Web App (PWA)
4. Optimasi performa dan loading time
5. Penambahan blog section dengan dynamic content

---

*Website ini dibuat oleh FAIQ ZAIDHAN (L200230149) untuk memenuhi Tugas #1 Membangun Website Personal dengan HTML & CSS.*