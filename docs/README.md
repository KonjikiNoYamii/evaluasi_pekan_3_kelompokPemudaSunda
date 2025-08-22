# Misi Perbaikan & Peluncuran Ulang Situs Toko Online "TechStore"

## Tipe: Ujian Praktik Berbasis Tim (2-3 orang per tim)

## Platform Pengumpulan: Tautan ke forked repository GitHub tim.

### Skenario & Problem Statement

Selamat! Tim Anda adalah sebuah agensi web profesional yang baru saja ditunjuk untuk mengambil alih proyek "TechStore". Proyek ini sebelumnya dikerjakan oleh seorang developer junior, dan hasilnya masih jauh dari standar profesional. Klien melaporkan bahwa websitenya jelek dan mereka khawatir tentang keamanan proyek.

Tugas utama tim Anda adalah melakukan audit total, memperbaiki semua masalah, merapikan repository agar sesuai standar industri, dan mempersiapkan situs ini untuk peluncuran resminya (Versi 1.0).

Setiap tim harus mem-fork repository "rusak" yang telah disediakan.

### Tugas Utama
#### Fase 1: Investigasi & Audit (CLI & Git Forensics)

Sebelum mengubah apapun, tim Anda harus berperan sebagai detektif digital untuk memahami kekacauan yang ada.

1. Analisis Struktur Aset: Gunakan perintah CLI untuk menavigasi dan memetakan struktur file. Identifikasi file mana saja yang lokasinya tidak standar (misalnya, gambar di root folder, bukan di dalam folder assets).

2. Perburuan Bug Visual: Terjadi bug styling css tidak ter-render dengan benar. Analisis dan temukan penyebabnya.

3. Audit Keamanan & Riwayat:
   - Gunakan perintah Git untuk menelusuri riwayat dan temukan commit spesifik di mana file debug.log pertama kali ditambahkan.

   - Di dalam file log tersebut, identifikasi baris pasti yang mengandung informasi sensitif (API Key).

4. Hasil: Buat sebuah file baru bernama AUDIT_REPORT.md di root directory. Di dalam file ini, jelaskan semua temuan Anda dari poin 1, 2, dan 3 dengan format Markdown yang rapi.

#### Fase 2: Perbaikan & Profesionalisasi (Clean-up & Hotfix)

Sekarang saatnya membersihkan kekacauan. Semua pekerjaan di fase ini harus dilakukan di dalam branch baru bernama hotfix-cleanup.

1. Refaktor Struktur Aset: Buat struktur direktori yang logis.Misalnya pindahkan semua file gambar (.png, .jpg) ke dalam folder assets untuk konsistensi. 

2. Perbaiki bug-bug yang anda temukan

3. Pembersihan Riwayat: Hapus total file debug.log dari seluruh riwayat Git. Hanya menghapusnya di commit baru tidaklah cukup; jejak file dan isinya harus benar-benar lenyap dari sejarah proyek.

4. Commit Profesional: Lakukan commit untuk setiap perubahan besar dengan menggunakan pesan commit yang konvensional dan deskriptif (misal: fix:, refactor:, docs:).

#### Fase 3: Pengembangan Fitur & Kolaborasi

Situs sudah stabil. Saatnya menambahkan fungsionalitas baru dengan alur kerja tim yang benar.

1. Buat Fondasi Baru: Merge branch hotfix-cleanup ke main. Setelah itu, buat branch baru bernama develop dari main. Semua pengembangan fitur baru harus dimulai dari sini.

2. Buat minimal 3 halaman baru lengkap dengan stylenya (minimal "Tentang Kami", "Produk", dan "Kontak"):
   - Buat branch baru untuk pembuat halaman" tersebut dari develop.
3. Simulasi Kolaborasi Tim:
   - Setelah semua anggota tim selesai dan melakukan push, salah satu dari mereka harus membuat Pull Request (PR) dari branch" tersebut ke develop.

   - Anggota tim lainnya harus melakukan Code Review di halaman PR GitHub.

   - Setelah disetujui, Merge PR tersebut.

#### Fase 4: Finalisasi & Peluncuran V1.0
Fitur baru sudah siap di develop. Sekarang saatnya mempersiapkan peluncuran resmi.

1. Resolusi Konflik: Merge branch about-us yang terbengkalai itu ke dalam branch develop Anda. Solve konfliknya jika ada.

2. Integrasi Final: Setelah konflik selesai dan fitur" yang dibuat terintegrasi, Merge branch develop yang sudah lengkap ke main.

3. Tagging Rilis: Buat sebuah tag bernama v1.0.0 pada commit terakhir di main untuk menandai peluncuran resmi landing page "TechStore".

