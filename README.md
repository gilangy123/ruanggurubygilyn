# Drill Soal TKA — Kirana Gilang (Android)

Aplikasi Android (WebView) yang membungkus web Drill Soal. Semua soal ada di
`app/src/main/assets/index.html`, jadi bisa dipakai tanpa internet
(hanya font Google yang butuh internet; tanpa itu dipakai font bawaan HP).

## Cara 1 — Tanpa Android Studio (paling mudah): build di GitHub
1. Buat repository baru di github.com (boleh private).
2. Upload SELURUH isi folder ini (termasuk folder `.github`).
3. Buka tab **Actions** → **Build APK** → **Run workflow**.
4. Tunggu ±3–5 menit, buka run yang selesai, unduh artifact **DrillSoalTKA-apk**
   → ekstrak → `app-debug.apk`.
5. Kirim ke HP, buka file APK, izinkan "Instal dari sumber tidak dikenal", lalu instal.

## Cara 2 — Android Studio
1. Install Android Studio, pilih **Open** → pilih folder ini.
2. Tunggu Gradle sync selesai.
3. Menu **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
4. APK ada di `app/build/outputs/apk/debug/app-debug.apk`.

## Cara 3 — Command line
Butuh JDK 17, Android SDK (platform 34), dan Gradle 8.5:
`gradle assembleDebug`

## Catatan
- APK ini bertanda tangan **debug** (cukup untuk dipasang sendiri). Untuk Play Store
  perlu dibuat keystore dan build release.
- Riwayat & poin tersimpan di dalam aplikasi; jika aplikasi di-uninstall, datanya hilang.
- Tombol Back Android sudah terhubung ke navigasi aplikasi.
- Minimal Android 8.0 (API 26). Disarankan Android System WebView / Chrome versi terbaru.
