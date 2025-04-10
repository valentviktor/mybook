# Roadmap Belajar Vue.js: Dari Dasar sampai Mahir

Roadmap ini dirancang bertahap, dengan fokus pembelajaran **materi + studi kasus nyata** agar kamu bisa paham konsep sekaligus praktik. Kamu tidak perlu terburu-buru—ikuti alurnya minggu demi minggu.

---

## Minggu 1: Pengenalan Vue & Dasar Template

### Materi:
1. Instalasi proyek dengan Vite
2. Struktur file Vue + penjelasan `main.js`, `App.vue`, dan komponen
3. Reactive Data: `data()`, `{{ variable }}`
4. Event: `@click`, `@input`, `@submit`
5. Directive dasar: `v-if`, `v-for`, `v-model`

### Studi Kasus:
**ToDo App Sederhana**
- Tambah, hapus, centang task
- Input dengan `v-model`
- List dengan `v-for`
- Tombol dengan `@click`

> **Tujuan:** Memahami interaktivitas dasar Vue

---

## Minggu 2: Komponen dan Komunikasi

### Materi:
1. Komponen dasar (`.vue` file)
2. Props & Emit (komunikasi antar komponen)
3. Slot
4. Ref & Reactive

### Studi Kasus:
**Aplikasi Komentar**
- Komponen form input
- Komponen daftar komentar
- Kirim komentar dari child ke parent via `emit`

> **Tujuan:** Pahami modularisasi dan komunikasi antar komponen

---

## Minggu 3: Vue Router

### Materi:
1. Instalasi & setup Vue Router
2. Routing halaman dasar: `Home`, `About`, `Products`
3. Navigasi dinamis: `/product/:id`
4. Navigasi programatik

### Studi Kasus:
**Aplikasi Produk**
- Halaman daftar produk
- Klik produk → ke detail halaman produk

> **Tujuan:** Paham navigasi antar halaman dalam SPA

---

## Minggu 4: State Management (Pinia)

### Materi:
1. Install Pinia & setup store
2. Reactive global state
3. Getter dan Actions
4. Integrasi store ke komponen

### Studi Kasus:
**Aplikasi Keranjang Belanja**
- Tambah produk ke cart
- Hapus produk dari cart
- Hitung total harga

> **Tujuan:** Paham konsep store global, interaksi multi-komponen

---

## Minggu 5: Integrasi dengan Backend Laravel API

### Materi:
1. Setup Laravel REST API (`GET`, `POST`, `PUT`, `DELETE`)
2. CORS, Sanctum (optional)
3. Ambil data dengan `axios`
4. Kirim data via form (POST)

### Studi Kasus:
**Aplikasi Manajemen Produk (CRUD)**
- Tampilkan daftar produk dari API
- Tambah, edit, hapus produk
- Tampilkan alert & validasi

> **Tujuan:** Paham integrasi Vue + Laravel API secara penuh

---

## Minggu 6: Laravel + Inertia (Alternatif tanpa REST API)

### Materi:
1. Install Laravel Jetstream + Inertia + Vue
2. Buat halaman SPA dengan Inertia
3. Form handling dengan Inertia
4. Passing data dari controller ke Vue

### Studi Kasus:
**Dashboard User**
- Tampilkan data user dari Laravel
- Update data profil dengan form Inertia
- Tampilkan notifikasi dan validasi

> **Tujuan:** Pahami pendekatan Inertia: SPA tanpa API

---

## Minggu 7: Lanjutan & Level Mahir

### Materi:
1. Upload file (gambar/dokumen)
2. Middleware dan Auth (role, login, protected route)
3. Optimasi performa komponen (Lazy load, Suspense)
4. Component Design System (Reusable UI)

### Studi Kasus:
**CMS Mini (Content Management System)**
- Admin login → dashboard → CRUD artikel dengan upload gambar
- Reusable komponen form + modal

> **Tujuan:** Menguasai skill Vue pada level profesional

---

## Bonus: Ekstra Studi Kasus Opsional

1. **Aplikasi Catatan Harian** (Vue + LocalStorage)
2. **Aplikasi Kasir Sederhana** (Vue + Laravel API + Pinia)
3. **Sistem Booking Ruangan** (Vue + Tailwind + Routing + Pinia)

---

Roadmap ini fleksibel. Jika kamu stuck di materi tertentu, **ulang dan perdalam studi kasusnya.** Jangan buru-buru ke tahap selanjutnya sampai kamu yakin udah ngerti dan bisa bikin minimal 1 proyek kecil dari materi itu.

Kalau kamu butuh versi interaktif (Notion/Trello), aku juga bisa bantu bikinin!

