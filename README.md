# Awesome Project Build with TypeORM

Steps to run this project:

1. Menggunakan relation mapping ORM bertujuan agar memudahkan dalam pembuatan standar struktur folder.
2. Menambahkan beberapa dependency yang diperlukan untuk enkripsi yaitu bcrypt, jsonwebtoken.
3. Membuat file .env untuk mengarahkan ketika debug ke database dan koneksi yang sudah di srtting.
4. Pada file index dipisahkan parent pathnya berdasarkan service api untuk movie dan auth untuk service yang berkaitan degan user.
5. Mendefinisikan variabel yang digunakan pada .env di data-source.
6. Membuat entity untuk user dan movie dengan id yg didapatkan dari PrimaryGeneratedColumn berbentuk string, dan auto generated date createdAt dan upadateAt.
7. Membuat middleware untuk menghandle kondisi jik request tidak sesuai, contoh untuk menghapus user diperlukan validasi role admin, maka di handle dengan middleware authorization.
8. Membuat 1 helpers untuk melakukan enkripsi password ketika dikirim oleh request signup
9. Pada sisi contoller dibuat 3 controller terpisah yaitu auth untuk menghandle request dari service login dan getProfile, user untuk signup, get, update, delete user. Dan movie controller untuk menghandle request dari service movie.
10. Pada typeORM juga terdapat folder routes bertujuan untuk memecah path dari masing - masing service dan juga menggunakan fungsi - fungsi dari middleware untuk keperluan validasi.
11. Untuk menjalankan project maka diperlukan migration terlebih dahulu untuk user dan movie.
