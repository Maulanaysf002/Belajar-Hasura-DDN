## Pengertian Model OSI (Open System Interconnection)

Model OSI (Open System Interconnection) diciptakan **oleh International Organization for Standardization (ISO)** yang menyediakan kerangka logika terstruktur bagaimana proses komunikasi data berinteraksi melalui jaringan.

Dahulu komunikasi data yang melibatkan komputer-komputer dari vendor yang berbeda-beda. Masing-masing vendor menggunakan protocol dan format data yang berbeda-beda. Sehingga ISO membuat suatu arsitektur komunikasi yang dikenal sebagai model OSI yang mendefinisikan standar untuk menghubungkan komputer-komputer dari vendor yang berbeda.

![alt text](/img/osi_model.png)

## 1. Aplication Layer

Application layer dalam model OSI 7 layer adalah **lapisan tertinggi yang berfungsi sebagai antarmuka langsung antara pengguna dan jaringan**. Lapisan ini menyediakan layanan untuk aplikasi pengguna dan bertanggung jawab untuk memastikan bahwa data dapat digunakan dengan benar oleh aplikasi.

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
