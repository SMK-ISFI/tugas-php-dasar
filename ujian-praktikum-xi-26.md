# Ujian Praktikum: Sistem CRUD Inventaris Barang Laboratorium

### **Skenario**

SMK Nusantara memiliki laboratorium komputer yang berisi berbagai perangkat seperti komputer, monitor, keyboard, mouse, proyektor, kabel LAN, dan perangkat pendukung lainnya. Selama ini, pencatatan barang masih dilakukan menggunakan buku tulis sehingga sering terjadi kesalahan data, barang sulit dilacak, dan laporan inventaris tidak rapi.

Pihak sekolah meminta siswa membuat **aplikasi web sederhana** untuk mengelola data inventaris barang laboratorium. Aplikasi harus memiliki fitur **register, login, logout**, serta fitur **CRUD data barang**.

Aplikasi boleh dibuat menggunakan:

- PHP Native
- Laravel

---

Buatlah aplikasi web sederhana dengan tema:

## “Sistem Informasi Inventaris Barang Laboratorium”

Aplikasi wajib memiliki fitur berikut.

## Fitur Autentikasi

### 1\. Register

Buat halaman register untuk mendaftarkan pengguna baru.

Data yang harus diinput:

- Nama lengkap
- Username atau email
- Password

Ketentuan:

- Semua input wajib diisi.
- Username/email tidak boleh sama dengan yang sudah terdaftar.
- Password harus disimpan dalam bentuk hash.

### 2\. Login

Buat halaman login.

Data yang harus diinput:

- Username/email
- Password

Ketentuan:

- Pengguna hanya dapat masuk jika data login benar.
- Jika login gagal, tampilkan pesan kesalahan.
- Setelah login berhasil, pengguna diarahkan ke halaman dashboard.

### 3\. Logout

Buat fitur logout.

Ketentuan:

- Setelah logout, pengguna tidak boleh bisa mengakses halaman dashboard atau CRUD.
- Halaman CRUD hanya dapat diakses oleh pengguna yang sudah login.

---

## Fitur Dashboard

Setelah login, pengguna masuk ke halaman dashboard.

Dashboard minimal menampilkan:

- Nama aplikasi
- Nama pengguna yang sedang login

---

## Fitur CRUD Data Barang

Buat modul pengelolaan data barang laboratorium.

### 1\. Tampil Data Barang

Tampilkan daftar barang dalam bentuk tabel.

Kolom minimal:

- No
- Kode barang
- Nama barang
- Kategori
- Jumlah
- Kondisi
- Tanggal masuk
- Aksi

Pada kolom aksi terdapat tombol:

- Detail
- Edit
- Hapus

### 2\. Tambah Data Barang

Buat form tambah barang.

Input yang wajib ada:

- Kode barang
- Nama barang
- Kategori
- Jumlah
- Kondisi
- Tanggal masuk
- Keterangan

Ketentuan:

- Semua field wajib diisi kecuali keterangan.
- Kode barang tidak boleh duplikat.
- Jumlah harus berupa angka dan minimal 1.
- Kondisi menggunakan pilihan:
  - Baik
  - Rusak ringan
  - Rusak berat

### 3\. Detail Data Barang

Buat halaman detail untuk melihat informasi lengkap satu barang.

Data yang ditampilkan:

- Kode barang
- Nama barang
- Kategori
- Jumlah
- Kondisi
- Tanggal masuk
- Keterangan

### 4\. Edit Data Barang

Buat form edit barang.

Ketentuan:

- Data lama harus tampil di form.
- Pengguna dapat mengubah semua data barang.
- Kode barang tetap tidak boleh sama dengan kode barang lain.
- Setelah data berhasil diubah, pengguna diarahkan kembali ke halaman daftar barang.

### 5\. Hapus Data Barang

Buat fitur hapus barang.

Ketentuan:

- Sebelum menghapus, tampilkan konfirmasi.
- Setelah data dihapus, pengguna diarahkan kembali ke halaman daftar barang.
- Tampilkan pesan berhasil setelah data dihapus.

---

## Struktur Database

Minimal memiliki 2 tabel.

### 1\. Tabel users

Kolom minimal:

<table><tbody><tr><td><strong>Kolom</strong></td><td><strong>Tipe</strong></td></tr><tr><td>id</td><td>INT, Primary Key, Auto Increment</td></tr><tr><td>name</td><td>VARCHAR</td></tr><tr><td>email</td><td>VARCHAR</td></tr><tr><td>password</td><td>VARCHAR</td></tr></tbody></table>

### 2\. Tabel barang

Kolom minimal:

<table><tbody><tr><td>Kolom</td><td>Tipe</td></tr><tr><td>id</td><td>INT, Primary Key, Auto Increment</td></tr><tr><td>kode_barang</td><td>VARCHAR</td></tr><tr><td>nama_barang</td><td>VARCHAR</td></tr><tr><td>kategori</td><td>VARCHAR</td></tr><tr><td>jumlah</td><td>INT</td></tr><tr><td>kondisi</td><td>VARCHAR</td></tr><tr><td>tanggal_masuk</td><td>DATE</td></tr><tr><td>keterangan</td><td>TEXT</td></tr></tbody></table>

---

## Ketentuan Tampilan

Tampilan boleh menggunakan:

- HTML dan CSS biasa
- Bootstrap
- Tailwind CSS
- Template admin sederhana

Minimal halaman yang dibuat:

- Halaman register
- Halaman login
- Halaman dashboard
- Halaman daftar barang
- Halaman tambah barang
- Halaman detail barang
- Halaman edit barang

---

## Nilai Tambahan

Siswa akan mendapat nilai tambahan jika menambahkan salah satu fitur berikut:

- Pencarian data barang
- Filter berdasarkan kategori atau kondisi
- Pagination
- Upload foto barang

---

## Catatan

Gunakan nama database:

```
db_inventaris_lab
```

Nama aplikasi yang disarankan:

```
SILAB - Sistem Inventaris Laboratorium
```
