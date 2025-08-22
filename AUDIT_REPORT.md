## step 1A - Aalisis Struktur folder & FILE 

AUDIT REPORT – TechStore

Step 1A – Analisis Struktur Folder & File

Temuan:

File gambar/media tersebar di root, folder images/, img/, photos/, pics/ → perlu dipindahkan ke assets/images/.

CSS tersebar di root (css/, styles/, assets/css/) → perlu dikonsolidasikan.

File HTML backup/duplikat: index-old.html, index_backup.html, temp.html → perlu dihapus.

File debug.log, error.log, access.log, application.log masih ada di repo → sebaiknya dihapus, jangan commit informasi sensitif.

Dokumentasi .md tersebar di root, docs/, documentation/ → perlu dikonsolidasikan.



---

Step 1B – Bug Visual (CSS Tidak Render)

Temuan:

1. Halaman index.html tidak muncul styling.

Penyebab: tag <link> salah path atau ekstensi file CSS.

Contoh yang salah:

<link rel="stylesheet" href="style.sss">



2. File CSS sebenarnya ada di folder assets/css/style.css.


3. Halaman lain yang perlu diperiksa juga: home.html, product.html.


4. Semua link CSS akan diperbaiki di Step 2.




---

Step 1C – Audit Keamanan & Riwayat

Temuan:

File debug.log muncul pertama kali di commit be72ca7 (“apa ya lupa”).

File berisi data sensitif (API key, konfigurasi internal).

Risiko: data sensitif terekspos publik.

