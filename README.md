---

# Praktikum 8: PHP dan Database MySQL

---

**Mata Kuliah:** Pemrograman Web1

**Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom.

**Nama:** Fajar Fawwaz Atallah

**NIM:** 312410357

**Kelas:** TI.2A.A.4

---

## Membuat Database di phpMyAdmin:
```
CREATE DATABASE latihan1;
```

## Membuat Tabel nya:
```
CREATE TABLE data_barang (
  id_barang int(10) auto_increment Primary Key,
  kategori varchar(30),
  nama varchar(30),
  gambar varchar(100),
  harga_beli decimal(10,0),
  harga_jual decimal(10,0),
  stok int(4)
);
```
---
<img width="678" height="310" alt="image" src="https://github.com/user-attachments/assets/e40d365c-1a27-4e4f-9fc6-668adaa2b3ec" />

---

## Menambahkan Data
```
INSERT INTO data_barang (kategori, nama, gambar, harga_beli, harga_jual, stok)
VALUES ('Elektronik', 'HP Samsung Android', 'hp_samsung.jpg', 2000000, 2400000, 5),
('Elektronik', 'HP Xiaomi Android', 'hp_xiaomi.jpg', 1000000, 1400000, 5),
('Elektronik', 'HP OPPO Android', 'hp_oppo.jpg', 1800000, 2300000, 5);
```

## Hasil tampilann Data Barang di phpMyAdmin nya:
---
<img width="829" height="191" alt="image" src="https://github.com/user-attachments/assets/67d51153-5784-46a5-b8d5-1a007864d354" />

---

## Membuat Program CRUD
**Buat dulu folder lab8_php_database pada root directory web server (d:\xampp\htdocs)**

---
<img width="661" height="317" alt="image" src="https://github.com/user-attachments/assets/c5435f78-a62a-408a-b9a6-408a0f4908d0" />

---

## Lalu buka browser dan ketik http://localhost/lab8_php_database/ untuk mengakses nya

---
<img width="500" height="245" alt="image" src="https://github.com/user-attachments/assets/bab37989-0a6d-4609-b324-1a2416d972f1" />

---

## Membuat file koneksi database
**Buat file baru dengan nama koneksi.php**

```
<?php
$host = "localhost";
$user = "root";
$pass = "";
$db = "latihan1";

$conn = mysqli_connect($host, $user, $pass, $db);
if ($conn == false)
{
    echo "Koneksi ke server gagal.";
    die();
} else echo "Koneksi berhasil";
?>
```
---
## Buka melalui browser untuk menguji koneksi database (untuk menyampilkan pesan
**koneksi berhasil, uncomment pada perintah echo “koneksi berhasil”;**

---
<img width="478" height="134" alt="image" src="https://github.com/user-attachments/assets/81dad071-6b0d-430e-bc50-b3d9ad996b41" />

---
