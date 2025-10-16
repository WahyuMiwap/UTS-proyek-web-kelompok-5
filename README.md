# Project UTS Pemrograman Web - Website Brew & Co.

Proyek ini merupakan Ujian Tengah Semester (UTS) untuk matakuliah Pemrograman Web (Program Studi: Sarjana Terapan Manajemen Informatika / Semester 3). Proyek ini bertujuan untuk membuat halaman website interaktif untuk sebuah *coffee shop* fiktif bernama "Brew & Co." menggunakan HTML, CSS, dan JavaScript. Hasil akhir proyek di-hosting di server GitHub.

## Anggota Kelompok

| Nama Lengkap              | NIM         |
| :------------------------ | :---------- |
| Muhammad Wahyu Firmansyah | 24091397035 |
| Afta Wildana Zacky        | 24091397038 |
| Risda Sifa Hasna          | 24091397054 |

## Alamat Domain (Live Demo)

Website ini telah di-hosting menggunakan GitHub Pages dan dapat diakses melalui tautan berikut:

**[https://&lt;WahyuMiwap&gt;.github.io/&lt;UTS-proyek-web-kelompok-5&gt;/tugas%20web.html](https://<WahyuMiwap>.github.io/<UTS-proyek-web-kelompok-5>/tugas%20web.html)**

## Teknologi yang Digunakan

* **HTML5:** Untuk membangun struktur dan kerangka utama halaman web.
* **CSS3:** Untuk mendesain, menata letak, dan menambahkan animasi untuk mempercantik tampilan website.
* **JavaScript:** Untuk fungsionalitas dan interaktivitas, seperti event handling dan manipulasi DOM

---

## Penjelasan Kodingan Sesuai Kriteria Penilaian

Berikut adalah penjelasan implementasi kode pada proyek yang disesuaikan dengan kriteria penilaian pada dokumen `UTS Pemweb.pdf`.

### 1. Struktur HTML

File `tugas web.html` diorganisir menggunakan tag HTML semantik untuk meningkatkan aksesibilitas dan struktur yang jelas.

* **`<header>`:** Berisi elemen navigasi utama (`<nav>`) yang mencakup logo dan tautan ke bagian-bagian halaman.
* **`<main>`:** Membungkus seluruh konten utama halaman, yang dibagi lagi ke dalam beberapa bagian.
* **`<section>`:** Setiap bagian konten (seperti Home, Menu, About, Testimonials, Contact) dipisahkan menggunakan tag `<section>` dengan ID yang relevan untuk memfasilitasi navigasi internal.
* **`<footer>`:** Berisi informasi hak cipta di bagian paling bawah halaman.
* **Struktur Modal:** Terdapat dua `<div>` di akhir `<body>` dengan ID `memberModal` dan `menuModal`. Keduanya berfungsi sebagai kontainer pop-up yang awalnya disembunyikan dan akan ditampilkan menggunakan JavaScript.

### 2. Desain CSS 

File `style.css` bertanggung jawab atas seluruh aspek visual untuk menciptakan desain yang estetis dan menarik.

* **CSS Variables (`:root`):** Palet warna utama seperti `--bg-main` dan `--coffee-dark` didefinisikan sebagai variabel untuk menjaga konsistensi dan kemudahan dalam modifikasi desain.
* **Layouting:** Layout utama menggunakan **Flexbox** untuk mengatur elemen seperti navbar, konten hero, dan kartu testimoni, yang mempermudah implementasi desain yang responsif.
* **Desain Responsif:** Menggunakan **`@media queries`** untuk menyesuaikan tampilan pada berbagai ukuran layar, terutama di bawah 768px. Perubahan signifikan termasuk mengubah navigasi menjadi *hamburger menu* dan menata ulang layout beberapa bagian dari horizontal menjadi vertikal.
* **Animasi dan Transisi:** Efek visual seperti animasi `fadeUp` pada teks hero, transisi `transform` pada item menu saat di-hover, serta animasi `fadeIn` & `scaleUp` pada modal diimplementasikan untuk memberikan pengalaman pengguna yang lebih dinamis dan modern.

### 3. Fungsionalitas JavaScript 

File `Script.js` mengelola semua interaktivitas website. Seluruh kode dibungkus dalam event listener `DOMContentLoaded` untuk memastikan skrip berjalan setelah halaman dimuat sepenuhnya. Implementasi mencakup:

* **Event Handling:** Event `click` digunakan pada tombol menu, item menu, tombol *scroll*, dan tombol tutup modal untuk memicu fungsi tertentu. Event `keydown` pada `window` mendeteksi penekanan tombol 'Escape' sebagai cara alternatif untuk menutup modal.
* **DOM Manipulation:** Fungsi `openModal()` dan `openMemberModal()` secara dinamis membuat elemen HTML (`<li>`, `<div>`) berdasarkan data dari *array/object* JavaScript. Elemen-elemen ini kemudian disisipkan ke dalam DOM untuk menampilkan detail menu dan daftar anggota tim di dalam modal.
* **Style & Animation:** Fungsi `showCategory()` memanipulasi properti CSS seperti `style.opacity` dan `style.transform` untuk menciptakan animasi transisi yang halus saat beralih antara kategori menu 'Coffee' dan 'Snacks'. Kelas `.modal-open` ditambahkan ke `<body>` saat modal terbuka untuk menonaktifkan *scrolling* di latar belakang.

### 4. Dokumentasi dan SRS 

* **Dokumentasi Kode:** Komentar telah ditambahkan di dalam file `Script.js` dan `style.css` untuk menjelaskan bagian-bagian kode yang penting, seperti struktur data, fungsi utama, dan blok *styling*, agar mudah dipahami.
* **SRS (Software Requirements Specification) Sederhana:**
    * **a. Tujuan Proyek:** Tujuan utama proyek adalah merancang dan mengembangkan halaman website *front-end* yang fungsional dan estetis untuk "Brew & Co. Coffee Shop". Website ini bertujuan untuk memberikan informasi menu, profil perusahaan, dan testimoni pelanggan kepada pengunjung.
    * **b. Kebutuhan Fungsional:**
        * Pengguna dapat melihat navigasi utama (Home, About, Testimonials, Contact).
        * Pengguna dapat melihat daftar menu yang terbagi dalam kategori Coffee dan Snacks.
        * Pengguna dapat mengklik sebuah item menu untuk melihat detailnya (gambar, nama, deskripsi) dalam sebuah pop-up (modal).
        * Pengguna dapat mengklik tombol "Anggota Kami" untuk melihat daftar anggota tim pengembang dalam sebuah pop-up.
        * Pengguna dapat menutup jendela pop-up dengan mengklik tombol 'X', area di luar pop-up, atau menekan tombol 'Escape'.
        * Website dapat diakses dengan baik pada perangkat desktop maupun *mobile*.
    * **c. Kebutuhan Non-Fungsional:**
        * **Desain Estetis:** Tampilan website harus menarik, bersih, dan konsisten dengan tema *coffee shop* modern.
        * **Performa:** Halaman web harus dimuat dengan cepat.
        * **Keterbacaan:** Teks pada website harus mudah dibaca dengan kontras warna dan ukuran font yang baik.
        * **Validasi Kode:** Kode HTML dan CSS harus sesuai dengan standar.
