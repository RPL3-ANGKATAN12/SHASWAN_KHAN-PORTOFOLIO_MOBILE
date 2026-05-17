# Portofolio

## 1. Perkenalan

- **Vue**: library frontend untuk membuat antarmuka interaktif dengan komponen.
- **Vite**: build tool dan dev server yang sangat cepat untuk proyek modern (termasuk Vue).
- **Capacitor**: bridge yang mengubah aplikasi web menjadi aplikasi mobile (Android/iOS).

## 2. Progres Harian

1. Hari 1 — fokus
   - Instalasi Vue + Vite, lalu praktek bongkar-pasang komponen di `src/components`.

   ```sh
   npm create vue@latest
   cd <project-name>
   npm install
   npm run dev
   ```

2. Hari 2 — fokus
   - Perubahan `src/App.vue`, penggunaan `vue-router`, dan instalasi Tailwind.

   ```sh
   npm install tailwindcss @tailwindcss/vite
   ```

3. Hari 3 — fokus
   - Menggunakan tailwind
   - Menggunakan komponen dengan memanfaatkan props dan slot
   - Memanfaatkan asset di folder `/assets`
   - Melengkapi isi `src/views`

4. Hari 4 — fokus
   - Menginstall jdk26
   - Instalasi capacitor
   - Konfigurasi opsi pengembang lalu koneksi adb
   - Membangun Android app menggunakan capacitor

   ```sh
   # install cap
   npm install @capacitor/core @capacitor/android @capacitor/assets
   # inisialisasi cap
   npx cap init
   # menambahkan target os android ke project
   npx cap add android
   # menyinkronkan kode vite ke aplikasi
   npx cap sync android
   # menjalankan aplikasi
   npx cap run android
   ```

   **Mengganti ikon app**
   - Taruh file icon di: `/resources/icon.png`, lalu jalankan:

   ```sh
   npx capacitor-assets generate
   npx cap sync android
   npx cap run android
   ```

## 3. Catatan

- Jalankan `npm run dev` lalu buka alamat dev server di browser untuk melihat progres.

- Install Capacitor CLI sekali saja di laptop:

```sh
npm i -g @capacitor/cli
```

- Kalau pakai nirkabel pastikan berada di jaringan yang sama. Pastikan IP dan port tidak typo:

```sh
adb connect <IP_HP>:<PORT_HP>
adb devices
```

- Selalu jalankan `npx cap sync android` setiap kali melakukan build web sebelum `npx cap run android`.
