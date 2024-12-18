## Vana Datapig Auto Bot

Bot ini otomatis memproses data wallet, menghasilkan preferensi, menandatangani pesan, dan mengirimkannya ke API Datapig. Bot juga dilengkapi dengan mekanisme retry dan penanganan batas harian. Bot ini berjalan setiap 24 jam untuk memproses wallet secara otomatis.

## Fitur

Pemrosesan Wallet Otomatis: Bot memproses data setiap wallet, menghasilkan preferensi, menandatangani pesan, dan mengirimkannya ke API Datapig.

Mekanisme Retry: Bot mencoba kembali hingga 3 kali jika proses minting gagal.

Penanganan Batas Harian: Bot secara otomatis mendeteksi dan menangani respons "Daily Limit Reached" dari API Datapig dan melanjutkan ke wallet berikutnya.

Eksekusi Terjadwal: Bot berjalan setiap 24 jam dan memproses wallet pada interval yang sudah ditentukan.

Multiakun: Bot mendukung pemrosesan beberapa akun sekaligus. Private keys dari setiap akun cukup ditambahkan ke file pk.txt, masing-masing pada baris baru.


## Persyaratan

Sebelum memulai, pastikan kamu sudah memenuhi persyaratan berikut:

Node.js: Versi 16 atau lebih tinggi.

npm: Package manager untuk menginstal dependensi.

Private keys untuk wallet yang ingin kamu interaksikan.

Reference Codes (opsional, tapi disarankan untuk reward tambahan) untuk wallet kamu.



---

## Instalasi

1. Clone repository

Salin dan jalankan perintah berikut di terminal:

```
git clone https://github.com/BlacMagister/Datapig.git
```
```
cd Datapig
```


2. File pk.txt

masukkan private keys wallet kamu di dalamnya:

```
nano pk.txt
```


3. Instal dependensi

Jalankan perintah berikut untuk menginstal semua dependensi yang diperlukan:

```
npm install
```




---

## Menjalankan Bot

Setelah setup selesai, kamu bisa menjalankan bot dengan perintah berikut:

```
node main.js
```

Bot ini akan memproses setiap wallet yang ada di dalam file pk.txt, menghasilkan preferensi acak, menandatangani pesan, mengirimkannya ke API Datapig, dan melakukan minting file ke blockchain. Proses ini akan diulang setiap 24 jam.


---

Menjalankan Bot Secara Terus-Menerus

Untuk memastikan bot berjalan terus-menerus di background, kamu bisa menggunakan screen. Berikut adalah cara menjalankannya:

1. Mulai sesi screen baru: Jalankan perintah berikut:

```
screen -S datapig-bot
```


2. Jalankan bot: Setelah berada di dalam sesi screen, jalankan perintah bot seperti biasa:

```
node main.js
```


3. Detaching dari sesi screen: Jika kamu ingin melepaskan sesi dan biarkan bot berjalan di background, tekan:

```
Ctrl + A, lalu tekan D
```


4. Kembali ke sesi screen: Jika kamu ingin kembali ke sesi yang sudah berjalan, gunakan perintah:

```
screen -r datapig-bot
```
