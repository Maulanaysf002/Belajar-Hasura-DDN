## Pengertian

Load balancing merupakan proses pendistribusian traffic atau lalu lintas jaringan secara efisien ke dalam sekelompok server, atau yang lebih dikenal dengan server pool atau server farm. Load balancing ini berguna agar salah satu server dari website yang mendapatkan banyak lalu lintas kunjungan tidak mengalami kelebihan beban.

## Cara Kerja Load Balancing

Jika diibaratkan, load balancing memiliki fungsi yang sama seperti polisi lalu lintas yang memiliki tugas untuk mencegah kemacetan dan insiden lalu lintas lainnya. Dengan begitu, load balancer harus bekerja untuk memastikan arus lalu lintas jaringan tetap lancar dan dapat memberikan keamanan pada sistem kerja jaringan tersebut.

Secara sederhana, Anda dapat menyederhanakan cara kerja load balancing sebagai berikut:

1. Pengguna meminta akses masuk ke server.
2. Load balancer menerima permintaan tersebut dan mendistribusikan lalu lintas tersebut ke beberapa server.
3. Jika salah satu server sudah hampir penuh, load balancer akan mengalihkan lalu lintas tersebut ke server lain yang masih tersedia.

## Jenis Load Balancer

1. Hardware Load Balancer
2. Software Load Balancer
3. Virtual Load Balancer

### Hadrware Load Balancer

![hardware load balancer](/img/hadrware_load_balancer.jpg)

Hardware Load Balancer merupakan perangkat load balancing yang berbentuk perangkat keras atau fisik. Load balancer ini dapat mendistribusikan permintaan lalu lintas jaringan berdasarkan pengaturan yang diterapkan.

Load balancer ini harus diletakkan bersamaan dengan server di pusat data lokal karena bentuknya yang fisik. Jumlah load balancer yang dipasang dapat disesuaikan dengan jumlah lalu lintas tertinggi. Biasanya, load balancer ini dapat menangani lalu lintas dalam jumlah besar. Namun, Hardware Load Balancer memiliki harga yang cukup mahal.

### Software Load Balancer

![software load balancer](</img/software_load_balancer_(slb).png>)

Software Load Balancer termasuk ke dalam perangkat load balancing yang berbentuk perangkat lunak. Artinya, load balancer ini dapat dipasang secara digital pada server. Terdapat dua jenis Software Load Balancer, yaitu komersial dan open source.

Jika dibandingkan dengan Hardware Load Balancer, Software Load Balancer ini harganya relatif lebih murah. Selain itu, load balancer ini juga lebih fleksibel karena Anda dapat mengubah load balancer ini sesuai kebutuhan.

### Virtual Load Balancer

![virtual load balancer](/img/virtual_load_balancer.png)

Load balancer ini mengombinasikan kedua jenis load balancer sebelumnya ke dalam mesin virtual. Anda akan mendapatkan Hardware Load Balancer yang dipasang sebagai perangkat lunak di dalam mesin virtual.

## Metode Metode Load Balancing

### Round Robin

Metode load balancing yang paling umum dan sering digunakan yaitu Round Robin. Metode ini bekerja dengan cara menyalurkan lalu lintas jaringan secara berurutan dari satu server ke server lainnya sehingga menciptakan rotasi pembagian yang stabil.

> Sebagai contoh, website Anda memiliki tiga server yaitu: A, B, dan C. Ketika ada permintaan lalu lintas yang masuk, permintaan tersebut akan masuk ke server A terlebih dahulu. Permintaan selanjutnya akan masuk ke server B, permintaan setelahnya akan masuk ke server C, dan prosesnya akan berulang terus.

### IP Hash

IP Hash adalah metode load balancing yang melakukan pendistribusian lalu lintas jaringan berdasarkan data yang berhubungan dengan IP (incoming packet) dari pengguna.

> Sebagai contoh, data seperti IP destinasi, domain, URL, hingga port number akan menentukan server mana yang diarahkan oleh load balancer.

### Least Bandwidth

Dalam metode Least Bandwidth, pendistribusian lalu lintas jaringan akan dilakukan berdasarkan server dengan jumlah jaringan paling kecil pada ukuran megabyte per second (Mbps) terlebih dahulu. Jadi, ketika ada permintaan masuk, lalu lintas jaringan tersebut akan dialihkan langsung ke server dengan ukuran Mbps paling kecil dibanding yang lain.

### Least Connection

Metode Least Connection akan mendistribusikan lalu lintas jaringan berdasarkan server dengan jumlah koneksi yang paling sedikit terlebih dahulu.

> Jadi, jika salah satu server memiliki beban koneksi yang lebih besar, walaupun posisinya lebih di depan, permintaan lalu lintas jaringan akan dialihkan ke server dengan koneksi yang lebih kecil terlebih dahulu. Hal ini dapat mencegah terjadinya kelebihan beban pada salah satu server.

### Least Response Time

Least Response Time adalah versi upgrade dari metode Least Connection.

> Pada metode ini, distribusi lalu lintas jaringan dilakukan melalui dua cara, yaitu berdasarkan jumlah koneksi yang paling kecil dan waktu respons yang paling cepat. Jadi. ketika ada permintaan masuk, lalu lintas tersebut akan dialihkan ke server dengan koneksi paling kecil dan respons paling cepat terlebih dahulu dibandingkan server lainnya.

## Kelebihan Load Balancer

1. Memaksimalkan Performa Server

   Menerapkan load balancing dapat memaksimalkan performa dari setiap server. Load balancer dapat mempercepat respons server hingga mencegah terjadinya berbagai macam masalah seperti kelebihan beban dan down. Selain itu, load balancer juga dapat membantu membuat jaringan lebih stabil ketika diakses.

2. Menambah Fleksibilitas Server

   Fleksibilitas dari suatu server akan meningkat ketika administrator dapat mengelola lalu lintas yang masuk dengan lancar dan teratur. Load balancer dapat membantu memberikan beban yang merata dan seimbang setiap server agar permintaan lalu lintas dapat masuk dengan lancar dan teratur.

3. Memudahkan Proses Distribusi Lalu Lintas

   Load balancer dapat memudahkan proses distribusi lalu lintas, jadi kemungkinan terjadinya down akan makin kecil. Sebagai contoh, ketika salah satu server tidak dapat menerima permintaan lalu lintas, load balancer akan mengalihkan permintaan tersebut ke server lain yang tersedia dan memadai.

4. Manajemen Kegagalan Server Lebih Efisien

   Penerapan load balancing dapat membantu Anda mengatasi kegagalan server secara lebih efisien. Load balancer dapat mendeteksi server yang gagal menerima permintaan, menghentikan lalu lintasnya, dan mengirimkannya kepada server yang lain. Dengan begitu, manajemen kegagalan server akan dapat dilakukan secara lebih efisien.
