# Post-Test-3-PBO
# **Manajemen Pre-Order Kain Songket**

Program ini dibuat dengan aplikasi Java untuk mengelola data pre-order kain songket dengan menerapkan konsep OOP. Struktur program dibagi menjadi beberapa package, yaitu model untuk menyimpan struktur data, service untuk logika CRUD, dan main untuk menu interaksi pengguna. Pada bagian model diterapkan inheritance, di mana terdapat superclass PreOrder yang menyimpan atribut umum seperti id, namaPelanggan, alamat, dan jumlah, serta dua subclass yaitu PreOrderSongket yang menambahkan atribut motif dan PreOrderEksklusif yang menambahkan atribut bahan. Fitur yang tersedia dalam program ini meliputi menambah pesanan, melihat daftar pesanan, memperbarui data, menghapus data, serta melakukan pencarian berdasarkan nama pelanggan. Semua data pesanan dikelola menggunakan ArrayList dan input pengguna divalidasi agar lebih aman. Program berjalan secara berulang menampilkan menu utama dan hanya akan berhenti jika pengguna memilih menu keluar.


# Penjelasan Package & Program #


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

<img width="539" height="21" alt="{F0673702-AD98-421B-BD5A-49833B05E534}" src="https://github.com/user-attachments/assets/51d7e86b-dba4-4992-9bcc-4d41c106fd4a" />

Deklarasi subclass lain yaitu PreOrderEksklusif yang juga mewarisi superclass PreOrder.

<img width="298" height="22" alt="{6595D6BB-80D1-42A1-B900-2A275133DD9B}" src="https://github.com/user-attachments/assets/b9efff26-9b3f-4f15-93c5-60650c4d5c81" />

Menambah atribut baru bahan, hanya dimiliki kain eksklusif.

<img width="948" height="105" alt="{13358696-6B21-4C4E-9C49-FBF3EB738671}" src="https://github.com/user-attachments/assets/2d919a14-ca17-4ba1-b33b-13bbe471acc8" />

Constructor subclass, tetap memanggil constructor superclass lalu menambahkan inisialisasi atribut bahan.

<img width="556" height="160" alt="{20345EB7-CF5E-4CA6-94D7-F64163E57B01}" src="https://github.com/user-attachments/assets/0ab04771-7cb4-4cb1-aa79-50b0cf5a81b9" />

Getter dan setter untuk atribut bahan.

<img width="788" height="114" alt="{2E9183BF-36D1-4937-80A8-467B1999FBE7}" src="https://github.com/user-attachments/assets/571f8f12-93c6-47f4-9f74-c15f73c9c57d" />

Method toString() dioverride agar menampilkan data lengkap termasuk bahan.

**# Package Service (PreOrderService) #**

<img width="579" height="127" alt="{DF44A59F-091A-462D-9693-A1FB3A8C14D2}" src="https://github.com/user-attachments/assets/b7ed6900-8a1d-4a8c-b86e-df517b812e51" />

Mengimpor library Java yang dibutuhkan serta kelas dari package Model.

<img width="366" height="18" alt="{D04F9D1A-D0DA-4ED5-B7E3-A4E0FE1A91C6}" src="https://github.com/user-attachments/assets/346eadbf-7cf2-42f2-8034-7f42ef8774c2" />

Deklarasi kelas PreOrderService yang berisi semua logika CRUD.

<img width="722" height="45" alt="{E000040F-8B40-439D-8016-DA09758E6CA1}" src="https://github.com/user-attachments/assets/338a6eea-2c38-4876-a9d8-579e6bc945a7" />

ArrayList digunakan untuk menyimpan semua data pre-order dan Scanner digunakan untuk membaca input pengguna.

<img width="804" height="623" alt="{AC27DE49-999D-45D6-9568-FE4ECB8BDCCA}" src="https://github.com/user-attachments/assets/be7e99be-4420-43d1-bed1-9902bf64da0b" />
<img width="676" height="492" alt="{B4E64768-6B47-4543-98E6-F2F90D03C51D}" src="https://github.com/user-attachments/assets/376dd673-a652-44ec-b5a5-949138396938" />

Method ini menambah pesanan baru. Program meminta nama pelanggan, alamat, jumlah kain, lalu pilihan jenis kain. Jika memilih songket, diminta motif. Jika eksklusif, diminta bahan. Objek baru dibuat sesuai subclass lalu disimpan di listPreOrder.

<img width="657" height="246" alt="{22789A4D-406C-4758-83C8-DB519060132D}" src="https://github.com/user-attachments/assets/f8100702-c967-4c98-b9f9-486cffff2318" />

Method ini menampilkan semua data pesanan. Jika list kosong, ditampilkan pesan belum ada data.

<img width="879" height="650" alt="{9547A428-BEDC-4F47-87C6-60925FD00BCD}" src="https://github.com/user-attachments/assets/1a961451-42f6-4051-8785-5c6c3d553a76" />

Method ini memperbarui data berdasarkan ID. Jika ID ada, pengguna bisa mengubah nama, alamat, atau jumlah. Jika jumlah tidak valid, data lama tetap dipakai.

<img width="830" height="306" alt="{69C86FFA-C561-4180-866D-75284C9EBC00}" src="https://github.com/user-attachments/assets/6104ce3d-7946-48db-b850-b32bf4eeafb0" />

Method ini menghapus pesanan berdasarkan ID. Jika ID tidak ditemukan, program memberi pesan error.

<img width="761" height="345" alt="{576F547D-BAE6-4C81-9D41-6FF17E96294F}" src="https://github.com/user-attachments/assets/bfe41160-4e70-4fe3-b1fa-a076e1f24b38" />

Method ini mencari data berdasarkan nama pelanggan. Jika ada yang cocok, data ditampilkan. Jika tidak, muncul pesan tidak ada data.

<img width="612" height="217" alt="{FC8AC509-C87D-40CA-B026-39635D5AA078}" src="https://github.com/user-attachments/assets/6614a7e6-894c-4f27-b98a-d7ca36d28740" />

Method bantu untuk mencari objek pre order berdasarkan ID pelanggan.

**# Package Main (MainApp) #**

<img width="512" height="49" alt="{CFC4B210-AD55-42A2-9823-800889DC5F0A}" src="https://github.com/user-attachments/assets/079c3abd-34a5-4669-af60-920b248d8956" />

Deklarasi Class MainApp dan method main sebagai titik masuk program.

<img width="574" height="42" alt="{9AFBDF8F-67E9-4363-8EE0-7536887202A3}" src="https://github.com/user-attachments/assets/e7ae1b11-e2ac-4170-aaa6-88b9480911d8" />

Scanner dipakai untuk membaca input, sedangkan PreOrderService dipakai sebagai pengelola semua data.

<img width="682" height="246" alt="{1C3EA20F-CE9E-40A8-8E50-983EC1CAEB51}" src="https://github.com/user-attachments/assets/d46e11bd-c308-45dd-8e57-01988c606210" />

Menu utama yang ditampilkan terus meneerus dengan loop do while.

<img width="658" height="147" alt="{E826E6FC-45C1-4DA6-942A-8B0BC8545099}" src="https://github.com/user-attachments/assets/d592cd56-183b-4e36-9719-fb1cc30cc1ef" />

Validasi input agar hanya angka saja yang diterima, dan jika tidak valid atau menginpuy huruf dan karakter maka akan diset ke 1.

<img width="911" height="215" alt="{9E553978-AFE1-46B2-9DD9-F44CE2271418}" src="https://github.com/user-attachments/assets/6564ee82-1eb5-4c24-8366-bd8fd3a781b7" />

Switch case menjalankan method sesuai menu yang dipilih.

<img width="452" height="115" alt="{600DDE6D-CAE0-4D6F-BD02-2B45791AA3B2}" src="https://github.com/user-attachments/assets/341fc0bc-bd44-4c27-81d8-769892e1630d" />

looping atau perulangan akan berhenti apabila pengguna memilih angka 6, dan Scanner.close di sini ditutup settelah program selesai berjalan.


**# Output #**

<img width="714" height="391" alt="{2AA0CA9C-3222-4B1D-92DF-FB7576057391}" src="https://github.com/user-attachments/assets/d7186009-b6af-4b79-a074-2216236ea480" />

Pengguna diminta untuk mengimput atau memilih angka yang ingin di tuju, di sini dipilih angka 1 untuk menambahkan pesanan dan detail nya. terdapat dua pilihan yaitu 1. dengan pilhan Songket dan 2. untuk pilohan Eksklusif. di sini dipilih songket atau angka 1.

<img width="706" height="391" alt="{E1F8EC37-637B-402B-8349-C25185AAC169}" src="https://github.com/user-attachments/assets/4f3635f7-76ae-4958-8efa-6f20bda20b35" />

kemudian menginput kembali angka satu untuk memilih menu eksklusif, di mana pada menu ini terdapat menu bahan eksklusif yaitu dapat memilih atau request jenis bahan sesuai keinginan pelanggan.

<img width="1227" height="287" alt="{BC04B3B6-F752-48BD-B3C9-8E8D79229948}" src="https://github.com/user-attachments/assets/f37b2dce-fb18-4943-a993-1cd2eb1fefec" />

menu nomor dua digunakan unutk menampilkan informasi dan detail pemesanan.

<img width="875" height="301" alt="{C6B88136-4D60-4A82-B88C-0025132A1F88}" src="https://github.com/user-attachments/assets/03570a41-dc17-4be7-9429-06e882745722" />

menu nomor tiga digunakan untuk mengupdate pesanan, dapat dilihat pada gambar di atas bahwa ketika kembali mengimoutkan angka dua maka detail pesanan telah berhasil di update.

<img width="948" height="235" alt="{B5CD8CB6-8023-4FAB-8A9B-D12455706FFB}" src="https://github.com/user-attachments/assets/8d0383fd-1d4a-4e32-a669-3dc8eb1b7d05" />

menu nomor empat digunakan untuk menghapus pesanan.

<img width="1241" height="261" alt="{2712460B-6762-4D62-A7E4-B81FCB9A8245}" src="https://github.com/user-attachments/assets/c7187d1d-ab07-4460-8a70-2c9c38a62537" />

Pesanan berhasil dihapus.

<img width="1252" height="240" alt="{0758610B-E361-4DA1-BE35-13F0C453842A}" src="https://github.com/user-attachments/assets/fcb71ba9-2709-4b25-8919-335cc5281cd2" />

menu nomor lima dapat digunakan apabila pelanggan ingin mencari pesaanan berdasarkan ID.

<img width="1001" height="210" alt="{5F8F009D-2BD8-451E-B072-97111A6A1460}" src="https://github.com/user-attachments/assets/82782a45-41f3-4e7a-b81b-51c3a3856a08" />

apabila ingin keluar dari program atau aplikasi pemesanan, pengguna dapat memilih menu nomor enam.
