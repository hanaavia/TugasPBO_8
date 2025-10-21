# TugasPBO_8
 Tugas  8 PBO (B) implementasi World Of Zuul
 Nama    : Via Hana Nurma Putri
 NRP     : 5025241048
 Prodi   : Teknik Informatika

 World of Zuul adalah game petualangan berbasis teks yang konsepnya mirip seperti game eksplorasi zaman dulu, tapi sepenuhnya dikendalikan lewat perintah yang diketik oleh pemain. Game ini tidak menggunakan tampilan visual atau grafik, jadi semua interaksi dilakukan lewat terminal/console. Pemain bisa menjelajahi beberapa ruangan yang saling terhubung, dan latar tempat dari game ini biasanya digambarkan seperti area universitas.
Untuk bergerak atau berinteraksi, pemain memasukkan command tertentu seperti "go" untuk berpindah ruangan, "help" untuk melihat daftar command yang bisa digunakan, dan "quit" untuk keluar dari game. Setiap ruangan dalam game memiliki kemungkinan arah perpindahan ke ruangan lain yaitu north, east, south, dan west, jadi saat pemain mengetik perintah seperti "go north", game akan memindahkan pemain ke ruangan yang berada di arah utara jika memang tersedia. Konsep eksplorasinya sederhana, tapi cukup efektif untuk memahami struktur logika pemrograman berbasis objek.

Dalam implementasinya, World of Zuul dibuat menggunakan lima class utama, yaitu sebagai berikut:


Game : ini adalah class pusat dari keseluruhan program. Game yang menangani jalannya permainan, menerima input dari pemain, dan menentukan aksi apa yang harus dilakukan berdasarkan command yang diberikan. Bisa dibilang, ini adalah otak utama dari game.

Room : class yang digunakan untuk merepresentasikan setiap ruangan di dalam game. Tiap Room bisa punya koneksi ke ruangan lain melalui arah north, east, south, atau west. Di sinilah struktur map game ditentukan.

Command : class yang berfungsi untuk menyimpan perintah yang dimasukkan oleh pemain. Jadi command ini dikemas sebagai sebuah objek supaya lebih mudah diolah oleh sistem. Misalnya command “go north” akan dipisah antara kata utama (“go”) dan argumennya (“north”).

Parser : class yang bertugas membaca input dari pemain (yang diketik di console) dan mengubahnya menjadi object Command. Jadi Parser ini semacam penerjemah dari teks biasa ke format yang bisa dipahami program.

CommandWords : class yang menyimpan daftar kata perintah valid yang diizinkan dalam game, seperti “go”, “quit”, dan “help”. Dengan adanya class ini, Parser bisa mengecek apakah input pemain termasuk command yang valid atau tidak.
