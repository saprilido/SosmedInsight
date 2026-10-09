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

Belum punya data? Pakai `template-socmed-insight.csv` atau contoh `contoh-konten-sep2026.csv` dan `contoh-metrik-akun.csv`.
Detail format ada di [panduan-data.md](panduan-data.md).

## Membaca selisih di halaman Komparasi
Kolom kiri = periode aktif, kolom kanan = "Bandingkan dengan".
**Selisih = kanan dibanding kiri.** ▲ berarti periode kanan naik, ▼ berarti turun.

## API key Gemini (opsional)
Hanya diperlukan untuk membaca screenshot/PDF. Klik **API Key Gemini** di sidebar untuk membuka kolomnya.
- Key hanya disimpan di browser Anda, dan hanya jika kotak **Ingat key** dicentang.
- Untuk menghapus: klik **Hapus key** (menghapus dari kolom dan dari penyimpanan browser).
- Jangan pernah menaruh key di file di repo ini.

## Publikasi lewat GitHub Pages
1. Upload semua file di repo ini ke branch `main`.
2. Settings → Pages → Source: **Deploy from a branch**, Branch: `main`, folder `/ (root)`, lalu Save.
3. Tunggu 1–2 menit; alamat situs tampil di halaman Pages.

Repo publik berarti `index.html` dan contoh data terbuka untuk umum. Jangan upload data asli akun.

## Struktur
```
index.html                      dashboard (satu file)
template-socmed-insight.csv     template CSV satu file
contoh-konten-sep2026.csv       contoh data konten (fiktif)
contoh-metrik-akun.csv          contoh ringkasan akun (fiktif)
panduan-data.md                 format data yang dikenali
```

---
Made by [apink.web.id](https://apink.web.id/) with Claude | © copyright 2026 | ver. 1
Lisensi: MIT (lihat `LICENSE`).
