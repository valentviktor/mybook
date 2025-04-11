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



# 📘 Studi Kasus Vue.js untuk Penguatan Dasar & Portfolio

Belajar Vue.js jadi lebih mantap dengan implementasi nyata. Berikut adalah daftar studi kasus mulai dari level dasar hingga menengah, yang bisa kamu jadikan sebagai latihan sekaligus proyek portfolio.

---

## 🔹 Studi Kasus Dasar (Cocok untuk Pemula)

### 1. To-Do List App
- **Fitur:** Tambah, hapus, edit, tandai selesai.
- **Fokus:** `v-model`, `v-for`, `v-bind`, `v-on`, `v-if`, `v-show`.
- **Bonus:** Simpan data ke `localStorage`.

### 2. Counter App
- **Fitur:** Tambah & kurang nilai counter.
- **Fokus:** Reactive data, event handling.
- **Bonus:** Multiple counter dengan komponen terpisah.

### 3. Weather App (menggunakan API)
- **Fitur:** Input nama kota → tampilkan cuaca.
- **Fokus:** Fetch API (`fetch()` / `axios`), binding data dari API.
- **API Referensi:** [OpenWeatherMap](https://openweathermap.org/)

### 4. Form Validation App
- **Fitur:** Form registrasi dengan validasi dasar.
- **Fokus:** `v-model`, form handling, validasi manual.
- **Bonus:** Validasi dengan package seperti Vuelidate.

---

## 🔹 Studi Kasus Menengah (Pakai Vue Router / Pinia)

### 5. Notes App
- **Fitur:** Tambah, edit, lihat, dan hapus catatan.
- **Fokus:** Vue Router, komponen dinamis, form handling.
- **Bonus:** Simpan ke `localStorage`.

### 6. CRUD Produk (Mini Admin Dashboard)
- **Fitur:** Tambah, lihat, edit, hapus produk.
- **Fokus:** Modular component, REST API integration.
- **API Dummy:** [JSONPlaceholder](https://jsonplaceholder.typicode.com) / [MockAPI](https://mockapi.io/)

### 7. Blog Viewer App
- **Fitur:** Ambil & tampilkan artikel, pagination.
- **Fokus:** Dynamic routing, fetch API, conditional rendering.
- **Bonus:** Viewer markdown untuk isi artikel.

### 8. Simple Authentication Flow
- **Fitur:** Login, logout, auth guard.
- **Fokus:** Vue Router guard, state management (Vuex/Pinia).
- **Bonus:** JWT token + dummy API.

---

## 🔹 Studi Kasus Portfolio Siap Tayang

### 9. Portfolio Website
- **Fitur:** Tentang saya, proyek, kontak.
- **Fokus:** Routing, component reuse, layouting.
- **Bonus:** Deploy ke Netlify / Vercel.

### 10. E-commerce Frontend Mockup
- **Fitur:** List produk, filter, keranjang, checkout dummy.
- **Fokus:** Vuex/Pinia untuk cart, komponen kompleks.
- **Bonus:** Simulasi pembayaran (Stripe / Midtrans).

### 11. Kanban Board (Seperti Trello)
- **Fitur:** Drag & drop task, kategorisasi.
- **Fokus:** Komunikasi antar komponen, lifecycle.
- **Bonus:** Gunakan `VueDraggable`.

### 12. Chat App (Realtime)
- **Fitur:** Chat antar user (realtime).
- **Fokus:** WebSocket / Firebase.
- **Bonus:** Gunakan Firebase untuk backend-nya.

---

## 🔧 Tips Implementasi ke Portfolio

- ✅ Tambahkan halaman "Tentang Proyek".
- ✅ Sertakan dokumentasi (README) di GitHub.
- ✅ Deploy ke Netlify / Vercel.
- ✅ Tampilkan di LinkedIn atau personal website.

---

> **Mau mulai dari yang mana dulu?** Bisa kita breakdown langkah-langkah pembuatannya bareng.


