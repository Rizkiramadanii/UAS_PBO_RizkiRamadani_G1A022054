# UAS_PBO_RizkiRamadani_G1A022054
berikut ini merupakan UAS saya Rizki ramadani dengan npm G1A022054 membuat kode fasilitas pemesanan makanan menggunakan python

di dalam program terdapat 2 kelas dan beberapa method atau fungsi yang ada di dalamnya disini saya akan menjelaskan secara keseluruhan fungsi dari program masing - masing

- Kelas Menu:
yang pertama ada kelas menu di sini kita membuat sebuah menu untuk di tunjukkan oleh user beserta harga makanannya masing - masing agar user tidak kebinggungan untuk memilih makanan nantinya, di dalamnya ada beberapa fungsi dan konstruktor yakni :

1. __init__(self): Konstruktor ini digunakan untuk menginisialisasi objek menu. Pada bagian ini, menu_items diisi dengan daftar item makanan dan harga yang     disimpan dalam bentuk kamus.

2. display_menu(self): Fungsi ini bertujuan untuk menampilkan daftar menu beserta harga. Setiap item dalam menu_items akan ditampilkan dengan menggunakan perulangan, dan informasi seperti ID, nama item, dan harga akan dicetak ke layar.

3. get_menu_price(self, item_id): Fungsi ini digunakan untuk mendapatkan harga suatu item berdasarkan ID-nya. Jika ID item ditemukan dalam menu_items, harga item akan dikembalikan. Jika tidak, fungsi ini akan mengembalikan None.

- Kelas Order:
yang kedua ada kelas order ini adalah kelas agar user dapat memesan makanannya dengan memilih angka satu sampai lima yang masing masing ada fungsi nya. lebih lengkapnya dapat dilihat dibawah ini.

1. __init__(self): Konstruktor ini digunakan untuk menginisialisasi objek pesanan. Pada bagian ini, menu diinisialisasi sebagai objek dari kelas Menu, dan order_items diinisialisasi sebagai sebuah daftar kosong yang akan digunakan untuk menyimpan item pesanan.

2. add_item(self, item_id, quantity): Fungsi ini digunakan untuk menambahkan item ke dalam pesanan. Pertama, harga item diperoleh dari objek Menu dengan memanggil fungsi get_menu_price. Jika harga ditemukan (tidak None), maka item tersebut ditambahkan ke order_items berserta kuantitas dan harga totalnya. Informasi item juga dicetak ke layar sebagai umpan balik untuk pengguna. fungsi ini akan dijalankan jika user memilih angka 1 pada keyboardnya.

3. remove_item(self, item_index): Fungsi ini digunakan untuk menghapus item dari pesanan berdasarkan nomor item dalam daftar pesanan. Jika nomor item valid (di antara 1 dan panjang order_items), item tersebut dihapus dari order_items dan informasi item yang dihapus dicetak ke layar sebagai umpan balik untuk pengguna. fungsi ini akan dijalankan jika user menekan angka 2 di keyboardnya.

4. calculate_total(self): Fungsi ini digunakan untuk menghitung total harga pesanan dengan menjumlahkan harga total dari setiap item dalam order_items. Total harga pesanan kemudian dikembalikan. ini merupakan fungsi untuk menghitung total dari semua pesanan yang di buat dan menghitung harga keseluruhan yang harus di bayar oleh user.

5. display_order(self): Fungsi ini digunakan untuk menampilkan isi pesanan. Jika daftar pesanan kosong, pesan "Pesanan kosong" dicetak ke layar. Jika tidak, setiap item dalam order_items akan dicetak dengan menggunakan perulangan, termasuk nomor item, nama item, kuantitas, harga per item, dan harga total. fungsi ini akan berjalan jika user menekan angka 3 pada keyboardnya.

6. place_order(self): Fungsi ini digunakan untuk menyelesaikan proses pemesanan. Jika daftar pesanan kosong, pesan "Pesanan kosong. Tidak dapat melakukan pemesanan" dicetak ke layar. Jika tidak, total harga pesanan dihitung dengan memanggil fungsi calculate_total. Total harga pesanan dicetak ke layar, dan pesan "Pesanan berhasil ditempatkan" dicetak sebagai konfirmasi. fungsi ini adalah fungsi terakhir dalam memesan makanan jika user memilih angka 4 pada keyboard nya maka akan muncul semua pesanan dan harga total yang harus di bayar oleh user.

7. Fungsi main(): Fungsi ini merupakan fungsi utama yang memulai aplikasi. Pada awalnya, objek Order dan Menu dibuat. Kemudian, fungsi display_menu dari objek Menu dipanggil untuk menampilkan daftar menu. Setelah itu, terdapat perulangan yang memunculkan menu utama dan meminta pengguna untuk memilih tindakan yang diinginkan. Pilihan pengguna diambil menggunakan input, dan kemudian dilakukan pengujian kondisi if-elif-else untuk memanggil fungsi yang sesuai dalam objek Order. 

Setiap tindakan yang dilakukan oleh pengguna akan mengakibatkan pemanggilan fungsi-fungsi dalam kelas Order, seperti add_item, remove_item, display_order, dan place_order. Program akan terus berjalan dalam perulangan hingga pengguna memilih opsi "Keluar" (menu nomor 5).

Program tersebut berkaitan dengan OOP karena menggunakan konsep dasar OOP, seperti:

Kelas: Program tersebut menggunakan kelas Menu dan Order untuk merepresentasikan objek-objek yang terkait dengan menu dan pesanan. Kelas-kelas ini memiliki atribut dan metode yang terkait dengan fungsionalitas masing-masing.

Objek: Dalam program tersebut, objek-objek dibuat berdasarkan kelas-kelas yang telah didefinisikan. Misalnya, objek order dibuat berdasarkan kelas Order dan objek menu dibuat berdasarkan kelas Menu. Objek-objek ini memungkinkan manipulasi dan pemanggilan metode yang terkait dengan objek tersebut.

Encapsulation: Program tersebut menggunakan enkapsulasi dengan menyembunyikan detail implementasi kelas di dalamnya. Misalnya, metode add_item dalam kelas Order mengakses informasi item melalui objek menu, tetapi detail implementasi dan struktur data menu tidak perlu diketahui oleh pengguna kelas Order.

Inheritance: Meskipun dalam program tersebut tidak terlihat, tetapi konsep inheritance dapat digunakan dalam pengembangan lebih lanjut. Misalnya, jika ada jenis pesanan khusus, seperti "Pesanan Online" atau "Pesanan Langsung", dapat dibuat kelas turunan dari kelas Order dengan tambahan atribut dan metode yang spesifik untuk jenis pesanan tersebut.

Polymorphism: Dalam program tersebut, tidak terlihat adanya polimorfisme secara langsung. Namun, jika ada metode umum yang diimplementasikan di kelas induk dan diperluas (overridden) di kelas anak, konsep polimorfisme dapat diterapkan.

Dengan menggunakan OOP, program tersebut menjadi lebih terstruktur, modular, dan mudah diorganisasi. Konsep-konsep OOP membantu dalam memisahkan tanggung jawab, mengelompokkan fungsionalitas terkait dalam kelas, serta memungkinkan untuk pengembangan dan perluasan lebih lanjut dengan menggunakan pewarisan dan polimorfisme.

Semoga penjelasan ini dapat membantu dalam memahami lebih rinci tentang program dan hubungannya dengan OOP. 
