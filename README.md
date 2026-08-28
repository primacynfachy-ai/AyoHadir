# AyoHadir

Aplikasi absensi Android berbasis Flutter.

## Tujuan repository

Repository ini adalah sumber kode utama AyoHadir. Pengembangan dilakukan bertahap agar setiap fitur mudah diuji dan tidak saling merusak.

## Teknologi

- Flutter / Dart
- Material 3
- Target utama: Android
- Backend yang akan diintegrasikan: Supabase

## Struktur

```text
lib/
├── core/       # tema, konstanta, routing, service, model, widget bersama
└── features/   # modul fitur aplikasi
```

Fitur utama akan dibangun sebagai modul terpisah, antara lain autentikasi, QR, absensi, GPS, riwayat, dan profil.

## Aturan pengembangan

- Gunakan null safety dan penamaan Dart konvensional.
- Pertahankan pemisahan antar-feature.
- Jangan menaruh secret, password, atau Supabase service-role key di source code.
- Jangan menambahkan dependency tanpa alasan yang jelas.
- Jangan mengubah file yang tidak berkaitan dengan tugas.
- Perubahan besar harus dilakukan bertahap dan dapat diperiksa melalui Git.

## Validasi

Perubahan dianggap siap apabila pemeriksaan berikut lulus:

```text
flutter pub get
dart format --output=none --set-exit-if-changed .
flutter analyze
flutter test
flutter build apk --release
```

GitHub Actions digunakan untuk menjalankan validasi dan build APK secara otomatis.

## Pengembangan dengan AI

Coding agent harus membaca `AGENTS.md` sebelum mengubah kode. Kerjakan satu fitur atau satu perbaikan dalam satu perubahan yang jelas, kemudian validasi hasilnya.
