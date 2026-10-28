# huddle-tracker

Repo ini hanya untuk mencatat issue bug Huddle. Kode backend ada di repo `huddle-be`
dan kode frontend ada di repo `huddle-fe`; keduanya tidak diubah dari repo ini.

## Membuat issue

1. Buka tab **Issues** lalu klik **New issue**.
2. Pilih form **Bug Report** (issue kosong sengaja dimatikan).
3. Isi komponen, tingkat keparahan, langkah reproduksi, dan hasil yang diharapkan/aktual.
4. Kirim issue, lalu catat nomornya.

Jangan menempel password, token, atau data rahasia perusahaan di issue.

## Menutup issue otomatis dari PR

Di repo kode (`huddle-be` atau `huddle-fe`), tulis salah satu sintaks berikut di deskripsi PR
dengan owner/repo lengkap:

- `Fixes albertnanda19/huddle-tracker#123` — issue ditutup otomatis saat PR di-merge.
- `Refs albertnanda19/huddle-tracker#123` — hanya me-link, issue tetap terbuka. Pakai ini bila
  satu bug butuh lebih dari satu PR, misalnya PR backend dan PR frontend.

Syarat agar issue benar-benar tertutup otomatis:

- PR di-merge ke default branch repo kode tersebut.
- Orang yang melakukan merge punya akses write ke `albertnanda19/huddle-tracker`.

Setelah semua PR terkait selesai, tutup issue-nya manual bila masih memakai `Refs`.
