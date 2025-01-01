## Pengertian Model OSI (Open System Interconnection)

Model OSI (Open System Interconnection) diciptakan **oleh International Organization for Standardization (ISO)** yang menyediakan kerangka logika terstruktur bagaimana proses komunikasi data berinteraksi melalui jaringan.

Dahulu komunikasi data yang melibatkan komputer-komputer dari vendor yang berbeda-beda. Masing-masing vendor menggunakan protocol dan format data yang berbeda-beda. Sehingga ISO membuat suatu arsitektur komunikasi yang dikenal sebagai model OSI yang mendefinisikan standar untuk menghubungkan komputer-komputer dari vendor yang berbeda.

![alt text](/img/osi_model.png)

## 1. Aplication Layer

Application layer dalam model OSI 7 layer adalah **lapisan tertinggi yang berfungsi sebagai antarmuka langsung antara pengguna dan jaringan**. Lapisan ini menyediakan layanan untuk aplikasi pengguna dan bertanggung jawab untuk memastikan bahwa data dapat digunakan dengan benar oleh aplikasi.

Application layer merupakan lapisan yang terdekat dengan pengguna komputer. Karena protokol lapisan aplikasi ini terdapat dalam sistem jaringan komputer, maka application layer dapat menjadi lapisan awal atau terakhir, sehingga bisa berkaitan dengan berbagai aplikasi perangkat lunak atau aplikasi dalam komputer seperti, website browser, email client, dan lain sebagainya.

> **protokol yang tersedia**
>
> HTTP (untuk browsing web), SMTP (untuk email), FTP (untuk transfer file).

### Proses Sederhana pada Application Layer:

Misalnya, saat mengakses situs web:

1. Anda mengetik URL di browser.
2. Browser mengirim permintaan HTTP ke server web melalui jaringan.
3. Server web memproses permintaan dan mengirim kembali halaman web.
4. Browser menampilkan halaman kepada Anda.
5. Semua langkah di atas dikendalikan oleh lapisan aplikasi
6. menggunakan protokol seperti HTTP atau HTTPS.

## 2. Presentation Layer

Presentation Layer adalah salah satu dari tujuh lapisan dalam OSI Model (Open Systems Interconnection) yang bertanggung jawab untuk mengatur data sehingga dapat dipahami oleh lapisan di atasnya dan di bawahnya. Lapisan ini dikenal juga sebagai Layer 6.

**Fungsi Utama Presentation Layer :**

1. **Format Data**
   Mengubah data menjadi format yang dapat dimengerti oleh aplikasi. Contoh:
   Konversi data dari JSON ke XML atau sebaliknya.
   Mengatur encoding teks seperti ASCII, Unicode.
2. **Enkripsi dan Dekripsi**
   Melakukan proses enkripsi untuk menjaga keamanan data saat dikirimkan, dan dekripsi untuk membaca data yang diterima.
   Contoh: TLS/SSL untuk keamanan komunikasi.
3. **Kompressi Data**
   Mengurangi ukuran data untuk mempercepat pengiriman dan mengurangi konsumsi bandwidth.
   Contoh: Kompresi file menggunakan algoritma seperti GZIP.
4. **Translasi Data**
   Mengubah data dari satu format ke format lain, sehingga sistem dengan arsitektur yang berbeda dapat saling berkomunikasi.
   Contoh: Konversi floating-point number dari format IEEE ke format vendor tertentu.

**Contoh Protokol di Presentation Layer :**

1. **TLS/SSL (Transport Layer Security/Secure Sockets Layer)**,
   Menyediakan keamanan melalui enkripsi data dalam komunikasi jaringan.
2. **JPEG, PNG, GIF**,
   Format file untuk pengolahan gambar.
3. **MPEG, MP3**,
   Format untuk pengolahan data audio dan video.
4. **ASCII, EBCDIC, Unicode**,
   Standar encoding untuk teks.
5. **XDR (External Data Representation)**,
   Standar untuk serialisasi data.
