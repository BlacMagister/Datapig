Datapig Bot

Bot ini otomatis memproses data wallet, menghasilkan preferensi, menandatangani pesan, dan mengirimkannya ke API Datapig. Bot juga dilengkapi dengan mekanisme retry dan penanganan batas harian.

Fitur

Pemrosesan Wallet Otomatis: Memproses data setiap wallet, menghasilkan preferensi, menandatangani pesan, dan mengirimnya ke API Datapig.

Mekanisme Retry: Bot akan mencoba kembali hingga 3 kali jika proses minting gagal.

Penanganan Batas Harian: Secara otomatis mendeteksi dan menangani respons "Daily Limit Reached" dari API Datapig dan melanjutkan ke wallet berikutnya.

Eksekusi Terjadwal: Bot berjalan setiap 24 jam dan memproses wallet pada interval yang sudah ditentukan.


Persyaratan

Sebelum mulai, pastikan kamu sudah memenuhi persyaratan berikut:

Node.js: Versi 16 atau lebih tinggi.

npm: Package manager untuk menginstal dependensi.

Private keys untuk wallet yang ingin kamu interaksikan.

Reference Codes (opsional, tapi disarankan untuk reward tambahan) untuk wallet kamu.


Instalasi

1. Clone repository

git clone https://github.com/BlacMagister/Datapig.git
cd Datapig


2. Buat file pk.txt Buat file bernama pk.txt di direktori root proyek, lalu masukkan private keys wallet kamu di dalamnya.

''nano pk.txt''


3. Instal dependensi Jalankan perintah berikut untuk menginstal semua dependensi yang diperlukan.

npm install



Menjalankan Bot

Setelah setup selesai, kamu bisa menjalankan bot dengan perintah berikut:

node main.js

Bot ini akan memproses setiap wallet yang ada di dalam file pk.txt, menghasilkan preferensi acak, menandatangani pesan, mengirimnya ke API Datapig, dan melakukan minting file ke blockchain. Proses ini akan diulang setiap 24 jam.

Menjalankan Bot Secara Terus-Menerus

Untuk memastikan bot berjalan terus-menerus di background, kamu bisa menggunakan screen. Berikut cara menjalankannya:

1. Mulai sesi screen baru:

screen -S datapig-bot


2. Jalankan bot: Setelah berada di dalam sesi screen, jalankan perintah bot seperti biasa:

node main.js


3. Detaching dari sesi screen: Jika kamu ingin melepaskan sesi dan biarkan bot berjalan di background, tekan:

Ctrl + A, lalu tekan D


4. Kembali ke sesi screen: Jika kamu ingin kembali ke sesi yang sudah berjalan, gunakan perintah:

screen -r datapig-bot
