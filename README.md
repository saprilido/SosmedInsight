# SOCMED INSIGHT

Dashboard analitik media sosial (Instagram) untuk YMD: satu file HTML, tanpa server, tanpa instalasi.
Data CSV/XLSX diolah penuh **offline** di browser. Tidak ada data yang dikirim ke server mana pun,
kecuali jika Anda sendiri memakai API key Gemini untuk membaca gambar/PDF.

## Fitur
- **5 halaman**: Ringkasan organik, Komparasi periode, Top Performance, Giveaway & kuis, Rekomendasi.
- **Upload banyak file sekaligus**: CSV, XLSX, gambar, PDF.
- **Impor CSV bawaan Meta** apa adanya (bahasa Indonesia atau Inggris).
- **Kalender periode**: pilih "Periode aktif" dan "Bandingkan dengan"; muncul peringatan jika periode tidak ada di data.
- **Caption ringkas dan bisa diklik** ke postingan (butuh kolom `url`/`permalink`).
- Mode terang/gelap, ekspor PDF.

## Cara pakai
1. Buka `index.html` di browser (klik dua kali), atau buka lewat GitHub Pages.
2. Klik **Pilih File** dan pilih satu atau banyak file sekaligus.
3. Pilih periode lewat kalender di bagian atas.

Belum punya data? Pakai `template/template-socmed-insight.csv` atau contoh di `contoh-data/`.
Detail format ada di [docs/panduan-data.md](docs/panduan-data.md).

## Membaca selisih di halaman Komparasi
Kolom kiri = periode aktif, kolom kanan = "Bandingkan dengan".
**Selisih = kanan dibanding kiri.** ▲ berarti periode kanan naik, ▼ berarti turun.

## API key Gemini (opsional)
Hanya diperlukan untuk membaca screenshot/PDF. Klik **API Key Gemini** di sidebar untuk membuka kolomnya.
- Key hanya disimpan di browser Anda, dan hanya jika kotak **Ingat key** dicentang.
- Untuk menghapus: klik **Hapus key** (menghapus dari kolom dan dari penyimpanan browser).
- Jangan pernah menaruh key di file di repo ini.

## Publikasi lewat GitHub Pages
1. Buat repo baru, upload semua isi folder ini.
2. Settings → Pages → Source: **GitHub Actions** (workflow sudah ada di `.github/workflows/pages.yml`).
3. Tunggu workflow selesai; alamat situs tampil di halaman Pages.

Repo publik berarti `index.html` dan contoh data terbuka untuk umum. Jangan upload data asli akun
(folder `data-asli/` sudah diabaikan oleh `.gitignore`).

## Struktur
```
index.html                     dashboard (satu file)
template/                      template CSV satu file
contoh-data/                   contoh CSV (data dari screenshot, sebagian dibulatkan)
docs/panduan-data.md           format data yang dikenali
.github/workflows/pages.yml    deploy otomatis ke GitHub Pages
```

---
Made by [apink.web.id](https://apink.web.id/) with Claude | © copyright 2026 | ver. 1
Lisensi: MIT (lihat `LICENSE`).
