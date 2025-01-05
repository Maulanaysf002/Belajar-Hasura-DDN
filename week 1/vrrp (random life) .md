## VRRP (Virtual Router Redundancy Protocol)

> VRRP adalah sebuah protokol yang dirancang untuk meningkatkan ketersediaan dan keandalan jaringan dengan menghadirkan redundansi pada perangkat jaringan utama, seperti router.

> Dengan menerapkan VRRP, kita dapat mengurangi risiko kegagalan jaringan dan menjaga layanan tetap berjalan sebagaimana mestinya.

> Tujuan utama dari VRRP adalah memastikan bahwa lalu lintas jaringan tetap mengalir secara lancar meskipun terjadi gangguan pada satu router atau jalur koneksi tertentu.

### Cara Kerja VRRP

![ilustrasi vrrp](/img/ilustrasi%20vrrp.webp)

Konsep dasar di balik VRRP adalah **menciptakan grup router virtual**, di mana satu router dianggap sebagai router utama (master) dan yang lainnya sebagai router cadangan (backup). Router utama bertanggung jawab untuk mengirimkan lalu lintas jaringan, sementara router cadangan siap mengambil alih tugas tersebut jika router utama mengalami kegagalan. Proses ini dilakukan secara otomatis dan transparan terhadap pengguna dan perangkat di jaringan.

VRRP menggunakan **alamat IP virtual** yang dikenali oleh klien atau perangkat lain dalam jaringan sebagai titik gateway. Dalam keadaan normal, router utama akan menggunakan alamat IP virtual ini. **Jika terjadi kegagalan pada router utama (master), router cadangan (backup) akan mengambil alih alamat IP virtual dan fungsi gateway untuk menjaga kelancaran komunikasi jaringan.**

Salah satu aspek penting dari VRRP adalah kemampuannya untuk mendeteksi kegagalan router utama (master). Ini terjadi ketika pertukaran pesan VRRP secara periodik antara router dalam grup. Jika router utama tidak lagi mengirim pesan ini, router cadangan akan mengasumsikan bahwa router utama mengalami masalah dan akan mengambil alih peran sebagai router utama (master).
