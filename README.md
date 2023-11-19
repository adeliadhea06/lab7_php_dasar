# lab7_php_dasar

Nama : Dhea Dwi Adelia

NIM : 312210116

Kelas : TI.22.A.1

### Instruksi Praktikum
1. Persiapkan text editor misalnya Sublime Text.
   
2. Buat folder baru dengan nama lab7_php_dasar pada docroot webserver (htdocs)
   
3. Ikuti langkah-langkah praktikum yang akan dijelaskan berikutnya.

### Langkah - Langkah Praktikum

#### 1. Persiapan
   
Untuk memulai membuat kode php, perlu disiapkan web server dan interpreter PHP terlebih dahulu. Web server yang sering kita gunakan adalah Apache 2 dan interpreter PHP 7. Untuk memudahkan proses praktikum, kita gunakan aplikasi bundle web server yaitu XAMPP.


#### 2. Install XAMPP

Unduh XAMPP dari https://www.apachefriends.org/download.html dan pilih versi portable untuk memudahkan proses installasi. Kemudian extract file tersebut, seusikan direktorinya (misal: c:\xampp).

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/ee719547-aede-4c7b-9d2c-6fcfc156c730)


#### 3. Konfigurasi Web Server

• Konfigurasi Apache

Untuk konfigurasi HTTP server, seperti port yang digunakan akses HTTP, modul yang diaktifkan, lokasi document root, dll. Lokasi file: \xampp\apache\conf\httpd.conf

• Konfigrasi PHP

Untuk konfigurasi perilaku engine PHP yang berefek pada keamanan dan performa. Seperti batas maksimal waktu eksekusi script, batas file yang dapat diupload, error reporting, dll. Lokasi file: \xampp\php\php.ini

• Konfigrasi MySql

Konfigurasi server MySQL, seperti administrator user, port, timezone, dll. Lokasi file: \xampp\mysql\bin\my.ini


#### 4. Menjalankan Web Server

Untuk menjalankan Web server dari menu XAMPP Control.

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/f9e4bb30-d839-4b02-8d85-e207b9cac7ab)

• Uji coba apakah server sudah berkerja dengan baik

http://127.0.0.1 atau http://localhost

Tampil halaman utama XAMPP jika server sudah berkerja dengan baik.

• Dokumen Website

Semua file website tempatkan di direktori: \xampp\htdocs\

• Database MySQL

Direktori: \xampp\mysql\

Manajemen database: http://localhost/phpmyadmin


#### 5. Memulai PHP

• Buat folder lab7_php_dasar pada root directory web server (c:\xampp\htdocs)

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/7c010b2b-4882-4bd5-9e2d-b076efd28dba)

• Kemudian untuk mengakses direktory tersebut pada web server dengan mengakses URL: http://localhost/lab7_php_dasar/

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/d8ab2e2d-371f-4bab-b006-fafa7b338593)


### PHP Dasar

• Buat file baru dengan nama php_dasar.php pada directory tersebut. Kemudian buat kode seperti berikut.

       <!DOCTYPE html>
       <html lang="en">
       <head>
           <meta charset="UTF-8">
           <title>PHP Dasar</title>
       </head>
       <body>
           <h1>Belajar PHP Dasar</h1>
           <?php
               echo "Hello World";
           ?>
       </body>
       </html>

• Kemudian untuk mengakses hasilnya melalui URL: http://localhost/lab7_php_dasar/php_dasar.php

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/8508bc80-65c2-460b-874f-0e724e3d280b)


### Variable PHP

Menambahkan variable pada program

      <?php
      $nim = "0411500400";
      $nama = 'Abdullah';
      echo "NIM : " . $nim . "<br>";
      echo "Nama : $nama";
      ?>

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/2e2d8e8c-ec64-4e2b-8d1d-fbf02664649f)


### Predefine Variable $_GET

      <?php
      echo 'Selamat Datang ' . $_GET['nama'];
      ?>

Untuk mengaksesnya gunakan URL: http://localhost/lab7_php_dasar/latihan2.php?nama=Dhea

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/b4b77c4f-642c-4db8-85b4-8b5e1c028ab6)


### Membuat Form Input

        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <title>PHP Dasar</title>
        </head>
        <body>
        <h2>Form Input</h2>
        <form method="post">
            <label>Nama: </label>
            <input type="text" name="nama">
            <input type="submit" value="Kirim">
        </form>
        <?php
        echo 'Selamat Datang ' . $_POST['nama'];
        ?>
        </body>
        </html>

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/7dd8d8c9-7046-4872-a425-a11a1ba7be86)


### Operator

       <?php
       $gaji = 1000000;
       $pajak = 0.1;
       $thp = $gaji - ($gaji*$pajak);
       echo "Gaji sebelum pajak = Rp. $gaji <br>";
       echo "Gaji yang dibawa pulang = Rp. $thp";
       ?>

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/0e9bdcc4-86f6-428c-8944-8e10ef2fb213)


### Kondisi IF

       <?php
       $nama_hari = date("l");
       if ($nama_hari == "Sunday") {
           echo "Minggu";
       } elseif ($nama_hari == "Monday") {
           echo "Senin";
       } else {
           echo "Selasa";
       }
       ?>

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/4ec4701e-4c6e-48b2-9794-d1a41fee7996)


### Kondisi Switch

       <?php
       $nama_hari = date("l");
       switch ($nama_hari) {
           case "Sunday":
               echo "Minggu";
               break;
           case "Monday":
               echo "Senin";
               break;
           case "Tuesday":
               echo "Selasa";
               break;
           default:
               echo "Sabtu";
            }
       ?>

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/4ec4701e-4c6e-48b2-9794-d1a41fee7996)


### Perulangan For

       <?php
       echo "Perulangan 1 sampai 10 <br />";
       for ($i=1; $i<=10; $i++) {
           echo "Perulangan ke: " . $i . '<br />';
       }
       echo "Perulangan Menurun dari 10 ke 1 <br />";
       for ($i=10; $i>=1; $i--) {
           echo "Perulangan ke: " . $i . '<br />';
       }
       ?>

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/b8fcf487-ffc2-4a41-9dff-a54763abc3c6)


### Perulangan While

       <?php
       echo "Perulangan 1 sampai 10 <br />";
       $i=1;
       while ($i<=10) {
           echo "Perulangan ke: " . $i . '<br />';
           $i++;
       }
       ?>

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/e878934e-e47b-4f7c-9252-0f454bdf1c41)


### Perulangan Dowhile

       <?php
       echo "Perulangan 1 sampai 10 <br />";
       $i=1;
       do {
           echo "Perulangan ke: " . $i . '<br />';
           $i++;
       } while ($i<=10);
       ?>

![image](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/7b2159d9-d602-4c77-8cee-3bfe2fbd6c57)


### Pertanyaan dan Tugas

Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.

         <!DOCTYPE html>
         <html>
         <head>
             <title>Form Input PHP</title>
         </head>
         <body>
         
         <?php
         // Fungsi untuk menghitung umur berdasarkan tanggal lahir
         function hitungUmur($tanggal_lahir) {
             $today = new DateTime('today');
             $tanggal_lahir = new DateTime($tanggal_lahir);
             $umur = $today->diff($tanggal_lahir);
             return $umur->y;
         }
         
         // Daftar pekerjaan dan gaji
         $pekerjaan_list = [
             'Programmer' => 5000000,
             'Designer' => 4500000,
             'Marketing' => 4000000
         ];
         
         // Inisialisasi variabel
         $nama = $tanggal_lahir = $pekerjaan = $gaji = '';
         
         // Memproses form jika sudah disubmit
         if ($_SERVER['REQUEST_METHOD'] === 'POST') {
             $nama = $_POST['nama'];
             $tanggal_lahir = $_POST['tanggal_lahir'];
             $pekerjaan = $_POST['pekerjaan'];
         
             // Validasi input
             if (empty($nama) || empty($tanggal_lahir) || empty($pekerjaan)) {
                 echo "Semua field harus diisi!";
             } else {
                 // Hitung umur
                 $umur = hitungUmur($tanggal_lahir);
         
                 // Ambil gaji berdasarkan pekerjaan
                 $gaji = isset($pekerjaan_list[$pekerjaan]) ? $pekerjaan_list[$pekerjaan] : 'Pekerjaan tidak valid';
             }
         }
         ?>
         
         <h2>Form Input PHP</h2>
         <form method="post" action="<?php echo $_SERVER['PHP_SELF']; ?>">
             Nama: <input type="text" name="nama" value="<?php echo $nama; ?>"><br>
             Tanggal Lahir: <input type="date" name="tanggal_lahir" value="<?php echo $tanggal_lahir; ?>"><br>
             Pekerjaan:
             <select name="pekerjaan">
                 <option value="Programmer">Programmer</option>
                 <option value="Designer">Designer</option>
                 <option value="Marketing">Marketing</option>
             </select><br>
             <input type="submit" value="Submit">
         </form>
         
         <?php
         // Menampilkan output jika sudah diproses
         if ($_SERVER['REQUEST_METHOD'] === 'POST' && !empty($gaji)) {
             echo "<h2>Output:</h2>";
             echo "Nama: $nama<br>";
             echo "Umur: $umur tahun<br>";
             echo "Pekerjaan: $pekerjaan<br>";
             echo "Gaji: Rp. " . number_format($gaji, 0, ',', '.') . "<br>";
         }
         ?>
         
         </body>
         </html>

![Screenshot (514)](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/5974eff1-851c-4ba7-b82a-4c6525c2af72)

![Screenshot (516)](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/a36567f5-8e46-44a9-9fac-776cdbf290fa)

![Screenshot (517)](https://github.com/adeliadhea06/lab7_php_dasar/assets/115794875/aabff9ee-f943-4bf7-b363-11b9f8103dc7)


### Sekian, Terima Kasih.
