# AyoHadir

AyoHadir adalah aplikasi absensi berbasis QR yang akan dibangun dengan Flutter untuk Android. Backend utama direncanakan menggunakan Supabase.

## Status

Repository ini adalah fondasi project. Fitur produk akan ditambahkan bertahap setelah fondasi dan build tervalidasi.

## Struktur utama

```text
lib/
├── core/
│   ├── constants/
│   ├── models/
│   ├── routing/
│   ├── services/
│   ├── theme/
│   └── widgets/
├── features/
│   ├── auth/
│   ├── home/
│   ├── qr/
│   ├── attendance/
│   ├── history/
│   └── profile/
├── app.dart
└── main.dart
```

## Pengembangan dengan AI

Coding agent harus membaca `AGENTS.md` sebelum mengubah kode. Kerjakan fitur secara bertahap, jangan membuat ulang project tanpa alasan, dan jangan memasukkan secret ke repository.

Repository ini dapat digunakan sebagai sumber kode dari coding agent yang terhubung ke GitHub. Setiap perubahan penting harus tetap dapat dibangun dan diuji.

## Validasi

Pemeriksaan utama:

```text
flutter pub get
dart format --output=none --set-exit-if-changed .
flutter analyze
flutter test
flutter build apk --release
```

GitHub Actions menjalankan pemeriksaan dan build APK secara otomatis pada push ke `main` dan Pull Request.

## Keamanan

Jangan commit:

- Supabase service-role key
- access token
- password
- private API key
- credential signing Android

Gunakan GitHub Secrets atau mekanisme secret management yang sesuai saat konfigurasi deployment/build.
