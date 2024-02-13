---
layout: post
title:  "menambahkan gambar"
date:   2024-01-29 13:39:33 +0800
categories: jekyll update
---
Untuk menambahkan gambar di Jekyll, Anda dapat mengikuti langkah-langkah berikut:

Tempatkan Gambar di Direktori Proyek:
Pastikan gambar yang ingin Anda tambahkan sudah berada di direktori proyek Jekyll Anda. Direktori umumnya disebut _assets atau assets, tetapi Anda dapat membuat direktori khusus untuk gambar jika diperlukan.

Edit atau Buat Posting/Page:
Jika Anda ingin menambahkan gambar ke posting, buka file posting yang ingin Anda edit. Jika Anda ingin menambahkannya ke halaman, buka file halaman yang sesuai.

Gunakan Markdown:
Jekyll umumnya menggunakan Markdown untuk format kontennya. Untuk menambahkan gambar, Anda dapat menggunakan sintaks Markdown berikut:

markdown
Copy code
![Deskripsi Gambar](assets/image/winda.jpg)
Gantilah /path/to/gambar.jpg dengan path relatif dari file Markdown ke gambar yang ingin Anda masukkan. Deskripsi gambar adalah teks yang akan muncul jika gambar tidak dapat dimuat.

Gunakan HTML (Opsional):
Jika Anda memerlukan kontrol lebih besar atas gambar, Anda juga dapat menggunakan elemen HTML <img>:

html
Copy code
<img src="/path/to/gambar.jpg" alt="Deskripsi Gambar">
Ini memungkinkan Anda menentukan atribut tambahan seperti lebar (width), tinggi (height), dan atribut lainnya.

Jalankan Proses Build:
Jekyll memerlukan proses build untuk menghasilkan situs statis. Jalankan perintah build di terminal:

bash
Copy code
bundle exec jekyll build
atau tanpa bundler:

bash
Copy code
jekyll build
Lihat Hasilnya:
Setelah proses build selesai, lihat situs Anda untuk memastikan bahwa gambar telah ditambahkan dengan benar.

Ingat bahwa langkah-langkah ini dapat sedikit bervariasi tergantung pada struktur proyek Jekyll Anda dan tema yang Anda gunakan. Pastikan untuk merujuk pada dokumentasi Jekyll dan tema yang Anda gunakan untuk informasi yang lebih spesifik.






