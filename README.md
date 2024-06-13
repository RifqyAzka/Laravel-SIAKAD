Web Project
Proyek ini adalah aplikasi web yang menggunakan Laravel. Berikut adalah petunjuk untuk menjalankan proyek ini di lokal.

Persyaratan
Pastikan Anda telah menginstal PHP, Composer, dan memiliki akses ke CLI. Anda juga memerlukan ngrok untuk menyiapkan terowongan HTTP.

Langkah-langkah untuk Menjalankan Proyek

1. Menginstal Dependensi dengan Composer

Untuk mengunduh semua dependensi yang diperlukan oleh proyek ini, jalankan perintah berikut di direktori proyek Anda:
composer install

2. Mengubah File example.env menjadi .env dan Menyesuaikan Isinya

Ubah nama file example.env menjadi .env dan sesuaikan isinya dengan informasi database yang Anda miliki. Contoh konfigurasi .env:
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nama_database
DB_USERNAME=username_database
DB_PASSWORD=password_database

3. Menghasilkan Kunci Aplikasi

Jalankan perintah berikut untuk menghasilkan kunci aplikasi:
php artisan key:generate

4. Menjalankan Migrasi Database

Untuk membuat tabel database yang diperlukan oleh aplikasi, jalankan perintah berikut:
php artisan migrate

5. Menjalankan Seeder Database (Opsional)

Jika Anda memiliki seeders untuk mengisi database dengan data awal, jalankan perintah berikut:
php artisan migrate --seed

6. Menginstal Ngrok

Ngrok adalah alat yang digunakan untuk menyiapkan terowongan HTTP dari lokal ke internet. Instal ngrok dari situs resmi Ngrok.

Menjalankan Ngrok

7. Jalankan ngrok untuk membuat terowongan HTTP ke port 8000:
ngrok http 8000

8. Menjalankan Server Laravel

Untuk menjalankan aplikasi Laravel, gunakan perintah berikut:
php artisan serve

Penjelasan Ngrok
Ngrok sangat berguna untuk menguji aplikasi web yang membutuhkan akses dari internet ke server lokal. Pastikan untuk menggunakan URL yang dihasilkan oleh ngrok sebagai endpoint untuk API atau webhook yang memerlukan akses dari luar jaringan lokal Anda.

Catatan Tambahan
Pastikan Anda selalu memperbarui URL ngrok setiap kali Anda memulai ulang ngrok, karena URL yang dihasilkan oleh ngrok bersifat sementara.
Jika Anda menghadapi masalah saat menjalankan proyek, pastikan untuk memeriksa log dan pesan error untuk penjelasan lebih lanjut.
