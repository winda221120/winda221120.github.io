---
---
Untuk menggunakan Jekyll untuk membuat situs web statis di GitHub, Anda dapat mengikuti langkah-langkah berikut:

### 1.Persiapkan Repositori GitHub:
-Buat repositori baru di GitHub untuk proyek situs web Anda.
-Pastikan untuk menyalakan opsi "GitHub Pages" di pengaturan repositori Anda. Ini akan memungkinkan GitHub untuk menyajikan situs web statis yang dibangun dengan Jekyll.

### 2.Instalasi Jekyll secara lokal (opsional):
-Anda dapat menginstal Jekyll secara lokal di komputer Anda untuk menguji situs web secara lokal sebelum mempublikasikannya di GitHub Pages.
-Instal Jekyll melalui perintah terminal atau command prompt dengan menggunakan RubyGems:

(gem install jekyll bundler)

### 3.Inisialisasi Proyek Jekyll:
-Di direktori kerja lokal Anda, inisialisasi proyek Jekyll dengan menggunakan perintah berikut:
arduino

(jekyll new nama_situs)
-Masuk ke direktori proyek:
bash

(cd nama_situs)

### 4.Edit Konten Situs Web:
-Edit file-file markdown di dalam direktori proyek untuk menyesuaikan konten situs web Anda.
-Atur layout, halaman, posting blog, dan konten lainnya sesuai kebutuhan Anda.

### 5.Jalankan Server Lokal (opsional):
-Jika Anda ingin melihat perubahan yang Anda buat secara lokal sebelum menerapkannya di GitHub Pages, Anda dapat menjalankan server lokal dengan perintah:
bash

(bundle exec jekyll serve)

-Situs web Anda akan tersedia di http://localhost:4000 secara default. Setiap perubahan yang Anda buat akan secara otomatis diperbarui di server lokal Anda.

### 6.Commit dan Push ke GitHub:
-Setelah Anda puas dengan situs web Anda, tambahkan semua perubahan ke repositori git Anda, lalu commit dan push ke repositori GitHub:
sql

(git add .
git commit -m "Menambahkan konten situs web"
git push origin master)

### 7.Tunggu Pembangunan di GitHub Pages:
-Setelah Anda melakukan push perubahan Anda, GitHub Pages akan membangun situs web Anda secara otomatis. Ini bisa memakan waktu beberapa saat.
-Setelah proses pembangunan selesai, situs web Anda akan tersedia di https://username.github.io/nama_situs.

Itulah langkah-langkah umum untuk menggunakan Jekyll untuk membuat situs web statis di GitHub. Pastikan untuk menyesuaikan konten dan konfigurasi sesuai dengan kebutuhan spesifik Anda.





