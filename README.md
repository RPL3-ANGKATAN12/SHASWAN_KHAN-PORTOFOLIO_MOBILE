# Portofolio — Day One

## 1. Perkenalan

- **Vue**: library frontend untuk membuat antarmuka interaktif dengan komponen.
- **Vite**: build tool dan dev server yang sangat cepat untuk proyek modern (termasuk Vue).
- **Capacitor**: bridge yang mengubah aplikasi web menjadi aplikasi mobile (Android/iOS).

## 2. Progres Harian

Hari 1 — fokus: instalasi Vue + Vite, lalu praktek bongkar-pasang komponen di `src/components`.

Perintah singkat untuk Day 1:

```sh
npm create vue@latest
cd <project-name>
npm install
npm run dev
```

Jalankan `npm run dev` lalu buka alamat dev server di browser untuk mencoba komponen.

## 3. Catatan

- Instalasi Capacitor (opsional untuk nanti):

```sh
# install Capacitor CLI sekali saja di laptop
npm i -g @capacitor/cli

# di dalam project (jika mau pakai Capacitor)
npm install @capacitor/core @capacitor/android
npx cap init
npx cap add android
npx cap sync android
npx cap run android
```

- Selalu jalankan `npx cap sync android` setiap kali melakukan build web sebelum `npx cap run android`.
