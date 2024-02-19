---
---
Sangat baik, mari kita jelajahi bagaimana membuat sebuah database terlebih dahulu sebelum membuat tabel. Database merupakan kumpulan dari tabel, yang digunakan untuk menyimpan data terkait dalam satu tempat. Berikut langkah-langkah untuk membuat database:

### 1. Membuat Database Baru:
Anda dapat menggunakan perintah CREATE DATABASE untuk membuat database baru. Misalnya, jika kita ingin membuat database dengan nama "sekolah":

sql
Copy code
CREATE DATABASE sekolah;
### 2. Memilih Database yang Dibuat:
Ketika Anda membuat atau ingin berinteraksi dengan database tertentu, Anda harus memilihnya terlebih dahulu. Anda dapat menggunakan perintah USE untuk memilih database yang ingin Anda gunakan:

sql
Copy code
USE sekolah;
### 3. Membuat Tabel dalam Database:
Setelah memilih database yang sesuai, Anda dapat membuat tabel di dalamnya menggunakan perintah CREATE TABLE. Misalnya, mari kita gunakan tabel "biodata_siswa" seperti yang telah kita buat sebelumnya:

sql
Copy code
CREATE TABLE biodata_siswa (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nama VARCHAR(100),
    usia INT,
    jenis_kelamin ENUM('Laki-laki', 'Perempuan'),
    alamat TEXT
);
### 4. Memasukkan Data ke dalam Tabel:
Setelah tabel dibuat, Anda dapat memasukkan data ke dalamnya menggunakan perintah INSERT INTO. Sebagai contoh:

sql
Copy code
INSERT INTO biodata_siswa (nama, usia, jenis_kelamin, alamat) VALUES 
('John Doe', 16, 'Laki-laki', '123 Main Street, Anytown'),
('Jane Smith', 15, 'Perempuan', '456 Elm Street, Othertown'),
('Michael Johnson', 17, 'Laki-laki', '789 Maple Avenue, Anycity');
Dengan langkah-langkah ini, Anda telah berhasil membuat sebuah database baru bernama "sekolah", membuat sebuah tabel "biodata_siswa" di dalamnya, serta memasukkan beberapa data contoh ke dalam tabel tersebut. Sekarang Anda bisa menjalankan berbagai operasi database dan tabel lainnya sesuai kebutuhan Anda.

User
---
---
![assets](/mariaDB.PNG)
