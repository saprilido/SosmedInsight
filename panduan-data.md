# Panduan data

Dashboard membaca tiga jenis data. Semua bisa diunggah bersamaan.

## 1. CSV bawaan Meta (tanpa diubah)
File ekspor Insight Instagram dengan format seperti:

```
sep=,
"Klik tautan Instagram"
"Tanggal","Primary"
"2026-09-01T00:00:00","0"
```

Judul metrik yang dikenali (Indonesia dan Inggris):

| Metrik di dashboard | Contoh judul di file Meta |
|---|---|
| Klik tautan bio | Klik tautan / Link clicks |
| Kunjungan profil | Kunjungan profil / Profile visits |
| Pengikut baru (follows) | Pengikut / Followers / Follows |
| Tayangan | Tayangan / Views |
| Interaksi | Interaksi / Interactions |

Catatan: file "Pengikut" dari Meta berisi pengikut baru kotor per hari, bukan pengikut bersih.

## 2. CSV data konten
Satu baris per konten. Kolom yang dikenali (nama kolom bebas huruf besar/kecil, Indonesia atau Inggris):

`tanggal, judul, url, platform, jenis, kategori, tayangan, likes, komentar, repost, share, simpan, pengikut_baru`

- `kategori`: organik, giveaway, quiz, game, winner. Jika kosong, ditebak dari judul.
- `url` / `permalink` / `tautan permanen`: membuat caption bisa diklik.
- Untuk periode bernama (bukan per tanggal), tambahkan kolom `periode`, misalnya `1–15 Sep 2026`.

## 3. Template satu file
`template/template-socmed-insight.csv` menggabungkan baris konten dan baris ringkasan akun
(audience, interaksi_akun, total_pengikut, pengikut_bersih, kunjungan_profil, klik_tautan_bio,
views_nonpengikut, tayangan_postingan/reel/story, er_postingan/reel/story).
Baris ringkasan akun: isi `periode` dan kolom akun, kosongkan `judul`.

## Gambar dan PDF
Dibaca lewat Gemini API (opsional) dan hanya berjalan jika `index.html` dibuka langsung di browser
atau lewat GitHub Pages. Di dalam claude.ai, fitur ini tidak tersedia.
