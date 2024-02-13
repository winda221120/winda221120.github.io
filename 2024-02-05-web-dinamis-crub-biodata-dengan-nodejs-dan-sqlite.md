Berikut adalah kode lengkap untuk aplikasi web dinamis biodata siswa dengan Node.js, SQLite, dan CRUD:

Buat file server.js:
javascript
Copy code
const express = require('express');
const bodyParser = require('body-parser');
const sqlite3 = require('sqlite3').verbose();

const app = express();
const PORT = process.env.PORT || 3000;

app.use(bodyParser.urlencoded({ extended: false }));
app.use(bodyParser.json());
app.set('view engine', 'ejs'); // Menggunakan EJS sebagai template engine

// Koneksi ke database
const db = new sqlite3.Database('./students.db', (err) => {
  if (err) {
    console.error('Error connecting to database:', err.message);
  } else {
    console.log('Connected to the database.');
  }
});

// Membuat tabel jika belum ada
db.run(`
  CREATE TABLE IF NOT EXISTS students (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT,
    age INTEGER,
    grade TEXT
  )
`);

// Route untuk menampilkan semua siswa
app.get('/students', (req, res) => {
  db.all('SELECT * FROM students', (err, rows) => {
    if (err) {
      console.error('Error getting students:', err.message);
      res.status(500).send('Internal server error');
    } else {
      res.render('students', { students: rows });
    }
  });
});

// Route untuk menambahkan siswa baru
app.post('/students/add', (req, res) => {
  const { name, age, grade } = req.body;
  db.run('INSERT INTO students (name, age, grade) VALUES (?, ?, ?)', [name, age, grade], function(err) {
    if (err) {
      console.error('Error adding student:', err.message);
      res.status(500).send('Internal server error');
    } else {
      res.redirect('/students');
    }
  });
});

// Route untuk menghapus siswa
app.post('/students/delete/:id', (req, res) => {
  const id = req.params.id;
  db.run('DELETE FROM students WHERE id = ?', [id], function(err) {
    if (err) {
      console.error('Error deleting student:', err.message);
      res.status(500).send('Internal server error');
    } else {
      res.redirect('/students');
    }
  });
});

// Server listening
app.listen(PORT, () => {
  console.log(`Server is running on http://localhost:${PORT}`);
});
Buat folder views dan buat file students.ejs di dalamnya:
html
Copy code
<!-- views/students.ejs -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Student List</title>
</head>
<body>
  <h1>Student List</h1>
  <ul>
    <% students.forEach(student => { %>
      <li><%= student.name %> - <%= student.age %> years old - Grade: <%= student.grade %></li>
    <% }); %>
  </ul>
  <form action="/students/add" method="post">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required><br>
    <label for="age">Age:</label>
    <input type="number" id="age" name="age" required><br>
    <label for="grade">Grade:</label>
    <input type="text" id="grade" name="grade" required><br>
    <button type="submit">Add Student</button>
  </form>
</body>
</html>
Jalankan npm install express sqlite3 body-parser ejs di terminal untuk menginstal dependensi yang diperlukan.

Jalankan node server.js untuk memulai server.

Dengan ini, Anda memiliki aplikasi CRUD sederhana yang berjalan menggunakan Node.js, SQLite, dan Express.js untuk mengelola biodata siswa. Anda dapat mengaksesnya melalui browser di http://localhost:3000/students.

User
hal yang salah harus di tambahkan kode yaitu 

Jika Anda mendapat pesan "Cannot GET /" ketika mencoba mengakses aplikasi Anda, itu berarti tidak ada rute yang ditentukan untuk menangani permintaan ke akar URL ("/").

Anda dapat menambahkan rute yang sesuai untuk menangani permintaan ke akar URL atau mengarahkannya ke rute yang sesuai.

Contoh:

javascript
Copy code
app.get('/', (req, res) => {
  res.redirect('/students'); // Mengarahkan ke halaman daftar siswa
});
Dengan menambahkan rute ini, ketika seseorang mengakses akar URL, mereka akan secara otomatis diarahkan ke halaman daftar siswa.

Setelah menambahkan kode di atas ke dalam server.js, restart server Anda, kemudian coba lagi mengakses aplikasi Anda. Jika Anda masih mengalami masalah, pastikan tidak ada kesalahan lain dalam kode Anda dan pastikan server berjalan tanpa masalah.






