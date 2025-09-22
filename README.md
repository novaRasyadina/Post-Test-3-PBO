# Post-Test-3-PBO
# **Manajemen Pre-Order Kain Songket**

Program ini dibuat dengan aplikasi Java untuk mengelola data pre-order kain songket dengan menerapkan konsep OOP. Struktur program dibagi menjadi beberapa package, yaitu model untuk menyimpan struktur data, service untuk logika CRUD, dan main untuk menu interaksi pengguna. Pada bagian model diterapkan inheritance, di mana terdapat superclass PreOrder yang menyimpan atribut umum seperti id, namaPelanggan, alamat, dan jumlah, serta dua subclass yaitu PreOrderSongket yang menambahkan atribut motif dan PreOrderEksklusif yang menambahkan atribut bahan. Fitur yang tersedia dalam program ini meliputi menambah pesanan, melihat daftar pesanan, memperbarui data, menghapus data, serta melakukan pencarian berdasarkan nama pelanggan. Semua data pesanan dikelola menggunakan ArrayList dan input pengguna divalidasi agar lebih aman. Program berjalan secara berulang menampilkan menu utama dan hanya akan berhenti jika pengguna memilih menu keluar.


**# Penjelasan Package #**


<img width="352" height="270" alt="{2745D803-73BE-42FC-BAE1-FD0470A367C5}" src="https://github.com/user-attachments/assets/7e332b4a-1db1-4624-b09c-92ccf0879e9e" />

* Package Model 
Package ini berisi class-class yang mendefinisikan struktur data pesanan. Di dalamnya ada PreOrder.java yang menjadi superclass. Kelas ini menyimpan data umum seperti id, namaPelanggan, alamat, dan jumlah. Selain itu ada dua subclass. Pertama, PreOrderSongket.java yang merupakan subclass dari PreOrder. Kelas ini menambahkan atribut motif untuk membedakan pesanan kain songket. Kedua, PreOrderEksklusif.java juga merupakan subclass dari PreOrder. Kelas ini menambahkan atribut bahan yang khusus untuk kain eksklusif. Jadi, PreOrder adalah superclass, sedangkan PreOrderSongket dan PreOrderEksklusif adalah subclass-nya.

* Package Service 
package Service yang berisi Class PreOrderService.java. class ini bertugas sebagai pengelola semua data. Fungsinya antara lain menambah pesanan baru, menampilkan semua daftar pesanan, memperbarui pesanan, menghapus, serta mencari berdasarkan nama pelanggan. Service ini bekerja dengan cara menyimpan semua data di sebuah ArrayList yang isinya bisa berupa objek dari superclass PreOrder maupun subclass PreOrderSongket dan PreOrderEksklusif.

* Package Main 
Package ini isinya hanya satu file yaitu MainApp.java. File ini berisi method main yang menjadi titik awal program berjalan. Di sinilah menu ditampilkan ke layar, lalu pengguna bisa memilih aksi seperti tambah pesanan, tampilkan semua, update, hapus, atau cari data. Semua aksi itu tidak ditulis di sini, tapi dipanggil dari kelas layanan yang ada di package Service.

**# Package Model (Superclass PreOrder) #**

<img width="361" height="29" alt="{99114B0C-1C85-4ED2-A804-45521843EB24}" src="https://github.com/user-attachments/assets/5f8cd0ed-1ba0-489e-9ec5-a065053453ee" />

Deklarasi kelas PreOrder yang berfungsi sebagai superclass untuk semua jenis pre-order.

<img width="556" height="22" alt="{9F19EA72-2269-403B-BA9B-7219D8ECF71B}" src="https://github.com/user-attachments/assets/a8b5e8d6-34c3-430c-8838-815cc35220ab" />

Variabel counter digunakan untuk membuat ID unik setiap kali objek baru dibuat. Nilainya bertambah otomatis.

<img width="448" height="98" alt="{FF92109B-7486-4035-9FFE-8AB7CEEF6733}" src="https://github.com/user-attachments/assets/e6bc09bc-d31e-433d-b0f8-aab412342e10" />

Atribut yang menyimpan informasi pesanan. Modifier private digunakan agar hanya bisa diakses lewat getter dan setter. Ini adalah penerapan encapsulation.

<img width="732" height="135" alt="{B8F594D6-25AF-4494-88AB-79478BB89DCA}" src="https://github.com/user-attachments/assets/ebc1f9d4-e233-4f5b-a7d8-8dd279355905" />

Constructor yang dijalankan setiap kali objek dibuat. ID otomatis bertambah, sedangkan nama pelanggan, alamat, dan jumlah diisi dari input pengguna

<img width="399" height="68" alt="{AAE5D259-B1DA-43CE-A978-57CD1D7F7218}" src="https://github.com/user-attachments/assets/fcb0fa5c-91e9-420c-aba7-c78c5bff3bdf" />

Getter untuk mengambil nilai ID. Tidak ada setter agar ID tetap konsisten.

<img width="603" height="166" alt="{972A5AA4-CF0C-45D1-8FB8-1B70B05CE3CA}" src="https://github.com/user-attachments/assets/6cba147f-0d5a-4d97-995c-3f5dd1ab4d99" />

Getter dan setter untuk namaPelanggan, digunakan untuk membaca dan mengubah nama.

<img width="611" height="164" alt="{009B03D2-695F-4140-BAF9-F0AFD154CF5E}" src="https://github.com/user-attachments/assets/f3982f58-e0d8-44f5-ae91-0cb025b8d4c3" />

Getter dan setter untuk alamat, sama seperti nama pelanggan.

<img width="562" height="153" alt="{570B50A5-EBDE-4BF3-BDAF-4AC3BFD7156D}" src="https://github.com/user-attachments/assets/0dd4f967-27c0-4cec-a40a-c75619d8f25f" />

Getter dan setter untuk jumlah, mengatur jumlah kain yang dipesan.

<img width="505" height="187" alt="{99646258-CDCF-49F0-990A-ACE022204CD7}" src="https://github.com/user-attachments/assets/451ad6b5-2824-4587-bbba-86819d8655ec" />

Method toString() dioverride agar saat objek dipanggil, langsung menampilkan informasi pesanan dalam format yang mudah dibaca.

**# Package Model (Subclass PreOrderSongket) #**

subclass ini juga berada di dalam package model yang dinamai PreOrderSongket

<img width="527" height="32" alt="{92458E66-5383-415E-8FCF-667BD190F40F}" src="https://github.com/user-attachments/assets/ef073451-cf38-4604-b480-bc2509d465e7" />

Deklarasi kelas PreOrderSongket yang mewarisi semua atribut dan method dari PreOrder.

<img width="336" height="20" alt="{15DC6237-35EB-4454-8FB1-62E1872EEADF}" src="https://github.com/user-attachments/assets/ccb7b044-7505-470f-9ad6-43a05d572aa3" />

Menambah atribut khusus untuk menyimpan motif kain songket.

<img width="948" height="88" alt="{A18037EF-A7D1-41E6-A33C-1C2645C4F6DB}" src="https://github.com/user-attachments/assets/14a25662-0a7d-411a-ab8c-90342d0c062d" />

Constructor subclass. Bagian super(...) memanggil constructor superclass agar atribut dasar tetap terisi, lalu atribut motif diisi sesuai input.

<img width="491" height="162" alt="{58238F44-470A-4C8A-8E61-F575D70743A8}" src="https://github.com/user-attachments/assets/82824fdb-fc59-41ae-9cf9-97553fc7a8f8" />

Getter dan setter untuk motif kain.

<img width="777" height="128" alt="{69FBD0A3-72DD-42F3-BD4C-793A8C603CE4}" src="https://github.com/user-attachments/assets/4914b81f-9c20-4d1d-88ea-43ad2064a6ba" />

Method toString() dioverride agar selain data dasar, juga menampilkan jenis kain songket dan motif. Override adalah proses ketika subclass (kelas turunan) menuliskan ulang method yang sudah ada di superclass (kelas induk) dengan tujuan menyesuaikan perilakunya. Jadi method dengan nama yang sama, parameter yang sama, tapi isinya berbeda antara superclass dan subclass.
Override dipakai agar objek dari subclass bisa memberikan hasil yang lebih spesifik sesuai kebutuhannya, tanpa mengubah kode superclass.


**# Package Model (Subclass PreOrderEkslusif) #**

subclass ini masih berada dalam package yang sama dengan subclasss sebelumnya yaitu dalam package model.
