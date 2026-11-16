# POH3 – pembungkus WebView untuk https://app.poh3.my.id/

Aplikasi Android sederhana (WebView) yang membuka https://app.poh3.my.id/ layaknya aplikasi.

## Cara membuat APK

### Opsi A – GitHub Actions (tanpa Android Studio)
1. Buat repositori baru di GitHub, unggah seluruh isi folder ini (termasuk folder `.github`).
2. Buka tab **Actions** > **Build APK** > **Run workflow** (atau cukup push ke branch `main`).
3. Setelah selesai, unduh artifact **POH3-apk** – isinya `app-release.apk`.

### Opsi B – Android Studio
1. File > Open, pilih folder ini, tunggu Gradle sync.
2. Build > Build Bundle(s) / APK(s) > Build APK(s).
3. APK ada di `app/build/outputs/apk/`.

## Yang sudah ditangani
- Tombol Back kembali ke halaman sebelumnya
- Tautan ke domain lain dibuka di browser / aplikasi lain (tel:, mailto:, WhatsApp, dll.)
- Unggah berkas/foto dari form, izin kamera untuk halaman web
- Unduhan berkas, bilah progres, halaman "Tidak dapat terhubung" saat offline
- Sesi login/cookie tersimpan

## Kustomisasi
- Nama aplikasi: `app/src/main/res/values/strings.xml`
- ID paket: `applicationId` di `app/build.gradle`
- Ikon: tambahkan `android:icon` di `AndroidManifest.xml` (mis. buat lewat Android Studio: New > Image Asset)

Catatan: APK ditandatangani dengan kunci debug, cukup untuk dipasang manual. Untuk Play Store, buat keystore sendiri.
