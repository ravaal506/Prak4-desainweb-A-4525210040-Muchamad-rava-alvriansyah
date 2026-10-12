# 🌿 Arunika Studio – Landing Page Responsif

| | |
|---|---|
| **Nama** | Muchamad Rava Alvriansyah |
| **NPM** | 4525210040 |
| **Mata Kuliah** | Desain Web |
| **Tugas** | Landing Page Responsif – Arunika Studio |

---

## 📖 Gambaran Umum

Proyek ini adalah landing page satu halaman untuk studio fiktif bernama **Arunika Studio**, yang menawarkan jasa desain web. Halaman dibuat hanya dengan **HTML dan CSS murni** (tanpa framework dan tanpa JavaScript). Tampilannya menyesuaikan ukuran layar, sehingga tetap nyaman dilihat di desktop maupun ponsel.

### 📁 Struktur Folder

```
.
├── index.html
├── css/
│   └── style.css
├── img/
│   ├── desktop.png
│   └── mobile.png
└── README.md
```

---

##  Hasil Tampilan

### Desktop

![Tampilan Desktop]  <img width="955" height="440" alt="ss web" src="https://github.com/user-attachments/assets/f9b2aa7f-f061-4de1-97f4-81b4145910ca" />


### Mobile

![Tampilan Mobile]  <img width="939" height="307" alt="ss mobile" src="https://github.com/user-attachments/assets/130b6850-1487-4a1b-b7d0-1e32a47ea07a" />


---

##  Penjelasan Kode

### 1. Struktur HTML (`index.html`)

- Semua isi halaman dibungkus dalam `<div class="page">`.
- Halaman terdiri dari tiga bagian utama: `<header>`, dua `<section>` (`#hero` dan `#layanan`), dan `<footer>` (`#kontak`).
- Menu navigasi memakai *anchor link* (`#hero`, `#layanan`, `#kontak`) yang mengarah ke `id` tiap bagian. Berkat `scroll-behavior: smooth`, halaman bergulir halus saat menu diklik.
- Tag `<meta name="viewport">` wajib ada agar layout responsif bekerja di ponsel.
- Atribut `lang="id"` menandakan isi halaman berbahasa Indonesia.
- File CSS dipanggil lewat `<link rel="stylesheet" href="css/style.css">`.

### 2. Reset dan Tampilan Dasar

- Selector `*` menghapus `margin` dan `padding` bawaan browser agar tampilan konsisten.
- `box-sizing: border-box` membuat lebar elemen sudah termasuk padding dan border.
- `body` memakai font **Arial**, `line-height: 1.6`, teks hijau tua `#20352a`, dan latar krem `#f7f5ef`.
- `.page` dibuat selebar layar (`width: 100%`), sedangkan jarak kiri-kanan tiap bagian diatur dengan padding `8%`.

### 3. Header dan Navigasi

- `header` memakai **Flexbox** dengan `justify-content: space-between`: logo di kiri, menu di kanan.
- `align-items: center` membuat logo dan menu sejajar secara vertikal.
- Kata "Studio" dibungkus `<span>` di dalam `.brand` agar bisa diberi warna emas `#b89658`.
- Link menu dibuat tanpa garis bawah (`text-decoration: none`) dan berubah menjadi emas saat `:hover`.
- Garis tipis `border-bottom` memisahkan header dari konten.

### 4. Hero

- Berisi logo bulat, judul, deskripsi singkat, dan tombol ajakan.
- `.logo-circle` berukuran `110px × 110px` dengan `border-radius: 50%`. Teks "RV" di dalamnya diletakkan di tengah memakai Flexbox.
- `.btn` adalah tag `<a>` dengan `display: inline-block` agar bisa diberi padding. Saat di-hover, warna latarnya berganti menjadi emas.

### 5. Layanan (Tiga Card)

- `.service-list` memakai Flexbox dengan `gap: 20px`, sehingga tiga card berjajar dengan jarak rata.
- `flex: 1` pada `.service-card` membuat ketiga card selebar sama.
- Tiap card punya angka kecil (`.number`), judul, dan deskripsi: **Web Design**, **Web Development**, dan **Branding**.
- Efek `:hover` + `transition: 0.3s` membuat card terangkat 5px (`translateY(-5px)`) dan border-nya menjadi emas.

### 6. Footer

- Latar hijau tua `#20352a` dengan teks putih dan rata tengah.
- Berisi email (`.contact`, berwarna emas) dan teks hak cipta.
- `id="kontak"` pada footer menjadi tujuan dari menu "Kontak".

### 7. Responsif (Media Query)

Aturan `@media (max-width: 650px)` aktif pada layar ponsel:

| Elemen | Perubahan |
|---|---|
| `header` | Menjadi satu kolom, rata tengah, dengan jarak 15px |
| `nav a` | Margin dan ukuran font diperkecil |
| `#hero` | Padding dikurangi, judul turun dari 32px ke 25px |
| `#layanan` | Padding dikurangi |
| `.service-list` | `flex-direction: column`, card tersusun ke bawah |
| `.service-card` | Lebar 100% |

>  **Cara mengetes:** buka `index.html` di browser, lalu perkecil lebar jendela atau gunakan mode responsive di Developer Tools (**F12**).

---

##  Palet Warna

| Warna | Kode | Dipakai untuk |
|---|---|---|
| Hijau tua | `#20352a` | Teks, logo bulat, tombol, footer |
| Emas | `#b89658` | Kata "Studio", angka card, hover, border hover |
| Krem | `#f7f5ef` | Latar halaman dan card |
| Putih | `#ffffff` | Latar section Layanan |
| Abu kehijauan | `#68756b` | Teks deskripsi |
| Krem tua | `#e4dfd2` | Garis header dan border card |

---

##  Properti CSS Utama

| Properti | Fungsi |
|---|---|
| `display: flex` | Menyusun elemen berjajar (header dan card layanan) |
| `justify-content` / `align-items` | Mengatur posisi horizontal dan vertikal di Flexbox |
| `gap` | Memberi jarak antar elemen dalam Flexbox |
| `box-sizing: border-box` | Lebar sudah termasuk padding dan border |
| `border-radius` | Membuat sudut membulat atau lingkaran |
| `transition` + `transform` | Efek card naik halus saat di-hover |
| `scroll-behavior: smooth` | Gulir halus saat klik menu |
| `@media (max-width: 650px)` | Mengubah layout untuk layar ponsel |
