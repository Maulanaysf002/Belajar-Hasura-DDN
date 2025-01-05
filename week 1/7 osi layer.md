## Pengertian Model OSI (Open System Interconnection)

Model OSI (Open System Interconnection) diciptakan **oleh International Organization for Standardization (ISO)** yang menyediakan kerangka logika terstruktur bagaimana proses komunikasi data berinteraksi melalui jaringan.

Dahulu komunikasi data yang melibatkan komputer-komputer dari vendor yang berbeda-beda. Masing-masing vendor menggunakan protocol dan format data yang berbeda-beda. Sehingga ISO membuat suatu arsitektur komunikasi yang dikenal sebagai model OSI yang mendefinisikan standar untuk menghubungkan komputer-komputer dari vendor yang berbeda.

![alt text](/img/osi_model.png)

**cara kerja OSI layer:**

1. Application layer akan mengirim data yang di kirim oleh user pada perangkat komputer penerima data.
2. Terjadi konversi email menjadi sebuah format jaringan pada presentation layer.
3. Pada session layer akan di bentuk sesi perjalanan data hingga seluruh proses pengiriman data selesai di laksanakan.
4. Pengirim melakukan pemecahan data di transport layer, dan di kumpulkan kembali pada transport layer penerima.
5. Network layer membuat alamat untuk mengarahkan data ke tujuan dengan benar.
6. Akan di lakukan pembentukan data menjadi bentuk frame serta alamat fisik dalam data link layer.
7. Pada physical layer, si lapisan utama, data akan di kirim melalui perantara jaringan menuju lapisan transport penerima.
8. Alur proses akan berbalik serta berulang dari physical layer ke application layer sampai mengarah ke jaringan komputer user.

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

**Peran Presentation Layer dalam Komunikasi**

Data dari aplikasi diubah menjadi format yang bisa dipahami oleh layer di bawahnya.
Data dienkripsi untuk memastikan keamanannya selama proses transmisi.
Setelah data sampai di sisi penerima, layer ini akan mendekripsi, mendekompresi, dan menerjemahkan data ke dalam format yang bisa digunakan oleh aplikasi.

## 3. Session Layer

Session Layer adalah lapisan ke-5 dalam model OSI 7 layer yang bertanggung jawab untuk mengelola dan mengontrol dialog atau sesi komunikasi antara dua perangkat atau aplikasi di jaringan.

Session Layer bertugas untuk membuka, memelihara, dan menutup sesi komunikasi antara aplikasi. Sesi ini mencakup koordinasi, pengaturan, dan sinkronisasi aliran data antara kedua pihak agar komunikasi berjalan lancar tanpa konflik.

**Peran Session Layer:**

1. Membuka, Memelihara, dan Menutup Sesi:

   Memastikan koneksi antara perangkat pengirim dan penerima terjalin dengan benar.
   Mengatur proses komunikasi agar tidak saling tumpang tindih.

2. Sinkronisasi:

   Memberikan titik sinkronisasi selama transfer data untuk mencegah pengulangan total jika terjadi gangguan. Misalnya, dengan menambahkan checkpoint dalam proses transfer data besar.

3. Manajemen Dialog:

   Mengatur mode komunikasi, apakah akan dilakukan secara:

   - Simplex (satu arah),
   - Half-Duplex (dua arah bergantian),
   - Full-Duplex (dua arah secara bersamaan).

4. Pemulihan (Recovery):

   Jika terjadi kegagalan selama sesi, session layer dapat mengatur ulang koneksi tanpa harus memulai ulang dari awal.

> Sesi yang dimaksud adalah **sesi logis** komunikasi antar aplikasi atau perangkat, baik di internet, jaringan lokal, atau sistem lainnya. Session layer tidak menangani koneksi fisik tetapi mengelola interaksi logis yang terjadi di atas koneksi fisik tersebut.

**Beberapa protokol yang ada dalam session layer:**

1. **NetBIOS (Network Basic Input/Output System):**

   Digunakan untuk mengelola komunikasi pada jaringan lokal.

2. **PPTP (Point-to-Point Tunneling Protocol):**

   Digunakan untuk membuat koneksi VPN.

3. **SIP (Session Initiation Protocol):**

   Digunakan untuk mengatur sesi dalam VoIP (Voice over IP).

4. **RPC (Remote Procedure Call):**

   Digunakan untuk memungkinkan program menjalankan fungsi di perangkat lain.

**Hubungan dengan Layer Lainnya:**

1. Layer Atas (Presentation Layer):

   Session layer menyediakan layanan kepada presentation layer dengan memastikan sesi komunikasi tetap stabil sehingga data dapat diproses lebih lanjut.
   Presentation layer bergantung pada session layer untuk sinkronisasi data.

2. Layer Bawah (Transport Layer):

   Session layer menggunakan layanan dari transport layer untuk mengirim dan menerima data dengan andal.
   Transport layer memastikan pengiriman data, sementara session layer mengelola sesi komunikasi itu sendiri.

## 4 Transport Layer

Transport layer bertugas untuk **mengatur pengiriman data antara host pengirim dan penerima**. Lapisan ini memecah data menjadi segmen-segmen yang lebih kecil (fragmentasi), mengelola pengiriman ulang data jika terjadi kesalahan, dan memastikan bahwa data diterima secara berurutan dan tanpa kehilangan.

**Cara Kerja Transport Layer**

Lapisan transport mengambil layanan dari application layer dan menyediakan layanan ke Network Layer.

> **Di sisi pengirim:** Lapisan transport menerima data (pesan) dari lapisan Aplikasi dan kemudian melakukan Segmentasi, **membagi pesan sebenarnya menjadi beberapa segmen, menambahkan nomor port sumber dan tujuan ke dalam header segmen, dan mentransfer pesan ke lapisan Jaringan.**

> **Di sisi penerima:** Lapisan transport menerima data dari lapisan Jaringan, menyusun kembali data yang tersegmentasi, membaca header-nya, mengidentifikasi nomor port, dan meneruskan pesan ke port yang sesuai di lapisan Aplikasi.

**Proses ke Proses Pengiriman**

Sementara Lapisan Data Link memerlukan alamat MAC (alamat 48 bit yang terdapat di dalam Kartu Antarmuka Jaringan setiap mesin host) dari host sumber-tujuan untuk mengirimkan bingkai dengan benar dan lapisan Jaringan memerlukan alamat IP untuk perutean paket yang tepat, dengan cara yang sama Lapisan Transport memerlukan nomor Port untuk mengirimkan segmen data dengan benar ke proses yang tepat di antara beberapa proses yang berjalan pada host tertentu. Nomor port adalah alamat 16-bit yang digunakan untuk mengidentifikasi setiap program klien-server secara unik.

[Sumber Bacaan Transport Layer](https://www.geeksforgeeks.org/transport-layer-responsibilities/)

### Protokol TCP (Transmission Control Protocol)

![TCP](/img/ilustrasi_TCP.gif)

TCP menggunakan mekanisme 3-way handshake untuk memastikan bahwa koneksi jaringan antar komputer terbentuk dengan benar sebelum data mulai dikirim. Selain itu, TCP juga memiliki kemampuan untuk mengontrol aliran data yang dikirim dan menerima konfirmasi bahwa data telah diterima dengan benar.

TCP sering digunakan dalam aplikasi jaringan seperti browsing web, transfer file, streaming video, dan banyak lagi. Protokol ini sangat handal dan dapat diandalkan, meskipun kecepatannya mungkin lebih lambat dibandingkan dengan protokol jaringan lainnya seperti User Datagram Protocol (UDP).

[Sumber Bacaan TCP](https://www.geeksforgeeks.org/what-is-transmission-control-protocol-tcp/)

### Protokol UDP (User Datagram Protokol)

![UDP](/img/ilustrasi_UDP.gif)

UDP adalah protokol transport yang digunakan dalam komunikasi data melalui jaringan komputer terutama pada transmisi data yang sensitif terhadap waktu seperti pemutaran video dan pencarian DNS. Protokol UDP memungkinkan pengiriman data yang sangat cepat namun kekurangan nya adalah seringkali terjadi paket hilang saat transit dan menimbulkan serangan DDoS. Tidak seperti TCP, **protokol ini tidak dapat diandalkan dan tidak memiliki koneksi**.

> UDP merupakan protokol yang berorientasi pada datagram, yang berarti setiap pesan dikirim sebagai unit terpisah tanpa memperhatikan pesan-pesan sebelumnya atau sesudahnya. UDP beroperasi di atas protokol IP (Internet Protocol) dalam suite Protokol TCP/IP

[Sumber Bacaan UDP](<[https://](https://www.geeksforgeeks.org/user-datagram-protocol-udp/?ref=header_outind)>)
