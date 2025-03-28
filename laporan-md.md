# Laporan Proyek Website Personal

## Deskripsi Proyek

Proyek ini merupakan implementasi website personal/portfolio menggunakan HTML dan CSS saja, tanpa menggunakan JavaScript. Website ini dibuat untuk memenuhi tugas mata kuliah Pemrograman WEB dan berfungsi sebagai portfolio online yang menampilkan informasi pribadi, keahlian, proyek, dan kontak.

### Tujuan
- Membuat website personal yang responsif untuk berbagai ukuran perangkat
- Menerapkan konsep semantik HTML dan CSS modern
- Mengimplementasikan fitur interaktif menggunakan CSS saja
- Membuat desain yang menarik dan profesional

### Fitur Utama
1. **Navigasi Responsif**: Menu navigasi yang menyesuaikan dengan ukuran layar
2. **Mode Gelap (Dark Mode)**: Fitur untuk mengganti tema website menjadi gelap "sesuai tema sistem perangkat" menggunakan CSS (tanpa JavaScript)
3. **Halaman Beranda**: Menampilkan informasi utama dan foto profil
4. **Halaman Tentang**: Berisi informasi detail tentang diri
5. **Halaman Keahlian**: Menampilkan keahlian dengan visualisasi progress bar
6. **Halaman Portfolio**: Menampilkan beberapa pengalaman dengan fitur filter kategori menggunakan CSS
7. **Halaman Kontak**: Form kontak dan informasi kontak lainnya
8. **Animasi & Efek**: Berbagai efek hover dan animasi untuk meningkatkan UX

### Teknologi yang Digunakan
- **HTML5**: Struktur semantik website
- **CSS3**: Styling, layout (Flexbox, Grid, Media Queries), dan interaktivitas (menggunakan :checked pseudo-class dan sibling selectors)
- **Font Awesome**: Untuk ikon-ikon pada website
- **Google Fonts**: Untuk typography (Poppins)
- **CSS Variables**: Untuk implementasi tema terang/gelap
- **CSS Media Queries**: Untuk deteksi tema sistem dan responsivitas

## Struktur Folder dan File

```
├── index.html              # Halaman utama
├── about.html              # Halaman tentang
├── skills.html             # Halaman keahlian
├── portfolio.html          # Halaman portfolio
├── contact.html            # Halaman kontak
├── css/
│   └── style.css           # File CSS utama
└── images/                 # Folder untuk gambar
    ├── profile.jpg         # Foto profil
    ├── about.jpg           # Gambar halaman about
    ├── sertif1.png         # Gambar pengalaman 1
    ├── sertif2.png         # Gambar pengalaman 2
    ├── sertif3.png         # Gambar pengalaman 3
    ├── sertif4.png         # Gambar pengalaman 4
    ├── sertif5.png         # Gambar pengalaman 5
    └── sertif6.png         # Gambar pengalaman 6
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
    <!-- Checkbox tersembunyi untuk toggle dark mode -->
    <input type="checkbox" id="theme-toggle">
    
    <header>
        <!-- Logo dan navigasi -->
        <nav>
            <!-- Menu navigasi -->
            <li><label for="theme-toggle" class="theme-switch"></label></li>
        </nav>
    </header>

    <main>
        <!-- Konten spesifik halaman -->
    </main>

    <footer>
        <!-- Informasi copyright -->
    </footer>
</body>
</html>
```

### CSS
CSS dibuat dengan pendekatan modular, responsif, dan digunakan juga untuk menggantikan fungsionalitas yang umumnya menggunakan JavaScript:

1. **Variabel CSS**: Menggunakan variabel CSS untuk tema (light/dark) dan konsistensi warna
2. **Flexbox & Grid**: Untuk layout yang responsif dan modern
3. **Media Queries**: Untuk adaptasi ke berbagai ukuran layar dan deteksi preferensi tema sistem
4. **Transisi & Animasi**: Untuk efek visual yang menarik
5. **Responsivitas**: Website berfungsi dengan baik pada berbagai ukuran layar
6. **CSS Selectors Lanjutan**: Menggunakan selectors seperti `:checked`, `~`, dan attribute selectors untuk fungsionalitas interaktif

#### Implementasi Dark Mode dengan CSS
Dark mode diimplementasikan menggunakan kombinasi dari:
1. **Media Query** untuk mendeteksi preferensi tema sistem:
```css
@media (prefers-color-scheme: dark) {
    :root {
        /* Variabel dark mode */
    }
}
```

2. **Checkbox Tersembunyi** untuk toggle manual:
```css
#theme-toggle:checked ~ * {
    --background-color: #121212;
    /* Variabel dark mode lainnya */
}
```

#### Implementasi Filter Portfolio dengan CSS
Filter portfolio yang interaktif diimplementasikan menggunakan:
1. **Radio Button Tersembunyi** untuk pilihan filter
2. **CSS Selectors** untuk menyembunyikan item yang tidak sesuai kategori:
```css
#filter-web:checked ~ .portfolio-grid .portfolio-item:not([data-category="web"]) {
    display: none;
}
```

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
4. Implementasi fitur dark mode menggunakan CSS variables dan selectors lanjutan
5. Teknik untuk membuat website responsif pada berbagai perangkat
6. Optimasi pengalaman pengguna dengan animasi CSS
7. Pembuatan website interaktif tanpa menggunakan JavaScript
8. Penggunaan CSS secara kreatif untuk menggantikan fungsionalitas yang biasanya memerlukan JavaScript

## Tantangan dan Solusi

Beberapa tantangan dalam pengembangan proyek ini:

1. **Responsivitas**: Memastikan tampilan konsisten di berbagai ukuran layar
   - Solusi: Penggunaan media queries dan layout flexbox/grid
   
2. **Dark Mode Tanpa JavaScript**: Implementasi toggle tema tanpa menggunakan script
   - Solusi: Menggunakan checkbox tersembunyi, CSS selectors, dan variabel CSS

3. **Portfolio Filter Tanpa JavaScript**: Membuat filter kategori yang berfungsi dengan CSS saja
   - Solusi: Implementasi dengan radio button tersembunyi dan CSS selectors lanjutan

4. **Kompatibilitas Browser**: Memastikan selector CSS lanjutan bekerja di berbagai browser
   - Solusi: Penggunaan selector standar dan testing di berbagai browser

## Pengembangan Ke Depan

Untuk pengembangan selanjutnya, beberapa hal yang dapat ditambahkan:

1. Animasi yang lebih kompleks menggunakan CSS Animations
2. Peningkatan aksesibilitas untuk pengguna dengan berbagai keterbatasan
3. Optimasi CSS dengan teknik-teknik seperti CSS custom properties yang lebih efisien
4. Penggunaan CSS preprocessor seperti SASS untuk pengelolaan style yang lebih terstruktur
5. Implementasi CSS Houdini untuk efek visual yang lebih canggih
6. Penggunaan sistem CSS Grid yang lebih kompleks untuk layout yang lebih dinamis

## Link Website setelah Hosting

https://faiqzdhn.github.io/web_porto/

---

*Website ini dibuat oleh FAIQ ZAIDHAN (L200230149) untuk memenuhi Tugas #1 Membangun Website Personal dengan HTML & CSS tanpa JavaScript.*
