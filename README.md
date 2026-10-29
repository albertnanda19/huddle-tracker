# huddle-tracker

Repo ini hanya untuk mencatat issue bug Huddle. Kode backend ada di repo `huddle-be`
dan kode frontend ada di repo `huddle-fe`; keduanya tidak diubah dari repo ini.

## Membuat issue

1. Buka tab **Issues** lalu klik **New issue**.
2. Pilih form yang paling sesuai dengan jenis issue (issue kosong sengaja dimatikan).
3. Isi komponen, prioritas atau tingkat keparahan, dan bagian lain yang diminta form.
4. Kirim issue, lalu catat nomornya.

Jangan menempel password, token, atau data rahasia perusahaan di issue.

## Jenis issue

| Form | Kegunaan | Label jenis |
|------|----------|-------------|
| Bug Report | Melaporkan bug beserta langkah reproduksinya | `bug` |
| Feature Request | Mengusulkan kemampuan baru | `feature` |
| Improvement | Memperbaiki fitur yang sudah ada, termasuk performa | `improvement` |
| Refactor / Chore | Tech debt, refactor, CI, deploy, atau dokumentasi | `refactor` |

## Label

**Jenis**

- `bug` — bug yang dilaporkan lewat Bug Report.
- `feature` — fitur baru.
- `improvement` — perbaikan fitur yang sudah ada.
- `refactor` — refactor, tech debt, dan chore.

**Komponen**

- `backend` — Backend API.
- `frontend` — Frontend UI.
- `media-sfu` — Media plane dan SFU.
- `signaling` — Signaling dan WebSocket.
- `deploy` — Deploy dan infrastruktur.

**Tambahan**

- `performance` — performa dan skalabilitas.
- Label lain hanya dibuat atas permintaan pemilik repo.

Severity dan prioritas ditulis di body issue, bukan sebagai label. Form web hanya memasang
label jenis, jadi label komponen dan label tambahan ditambahkan manual atau oleh agent.

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
