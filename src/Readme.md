Cinema Ticket Booking App

Aplikasi ini adalah sistem pemesanan tiket mini cinema berbasis GUI (Graphical User Interface) menggunakan Java Swing. Aplikasi ini memungkinkan pengguna untuk:

Memesan tiket berdasarkan film, harga, jam tayang, dan jumlah tiket.
Memilih kursi yang diinginkan dari layout kursi.
Menyimpan data pemesanan ke tabel.
Memperbarui atau menghapus pemesanan yang sudah ada.
Fitur Utama
1. Input Informasi Pemesan
   Nama Pemesan: Nama pelanggan yang akan memesan tiket.
   Film: Pilihan film (contohnya: "PEMBURU IBLIS").
   Harga Tiket: Dua pilihan kelas, yaitu:
   EXECUTIVE (Rp30,000)
   DELUXE (Rp50,000)
   Jam Tayang: Pilihan jadwal tayang film seperti: "13:00 - 15:30".
   Jumlah Tiket: Spinner untuk memilih jumlah tiket (maksimum 10 tiket per pesanan).
2. Layout Kursi
   Kursi tersedia dalam layout 4x4 dengan label seperti A1, A2, hingga D3.
   Warna kursi:
   Hijau: Kursi tersedia.
   Kuning: Kursi sedang dipilih.
   Merah: Kursi sudah dipesan.
3. Tombol Aksi
   Pesan:
   Memesan tiket berdasarkan data yang dimasukkan.
   Memeriksa apakah kursi yang dipilih sesuai dengan jumlah tiket.
   Menambahkan data ke tabel dengan detail: nama, film, jam tayang, jumlah tiket, kursi, dan total harga.
   Update:
   Memperbarui data pemesanan yang dipilih di tabel.
   Mengembalikan kursi yang sebelumnya dipilih ke status "kosong" (hijau).
   Hapus:
   Menghapus data pemesanan dari tabel.
   Mengembalikan warna kursi yang dihapus menjadi hijau.
4. Tabel Pemesanan
   Menampilkan semua pemesanan yang sudah dilakukan dalam bentuk tabel.
   Kolom yang tersedia:
   Nama
   Film
   Jam Tayang
   Jumlah Tiket
   Kursi
   Total Harga
   Cara Kerja Aplikasi
   Form Input: Isi nama pemesan, pilih film, harga tiket, jam tayang, dan jumlah tiket yang diinginkan.
   Pilih Kursi: Klik kursi yang ingin dipesan. Warna berubah menjadi kuning.
   Pesan Tiket: Klik tombol "Pesan" untuk menyimpan data ke tabel. Kursi yang sudah dipesan akan berubah menjadi merah.
   Update Pemesanan: Pilih baris di tabel, ubah data di form, lalu klik "Update".
   Hapus Pemesanan: Pilih baris di tabel, lalu klik "Hapus". Kursi yang dihapus akan tersedia kembali (hijau).
   Penjelasan Kode
   Panel Input Data:

Menggunakan GridBagLayout untuk membuat layout input data.
Komponen input seperti JTextField, JComboBox, dan JSpinner.
Panel Kursi:

Menggunakan GridLayout untuk menampilkan tombol-tombol kursi.
Warna kursi berubah sesuai status (hijau, kuning, merah).
Panel Aksi:

Tombol-tombol untuk melakukan aksi seperti "Pesan", "Update", dan "Hapus".
Logika Warna Kursi:

Data kursi yang sudah dipesan disimpan dalam HashMap. Kunci berupa kombinasi film, jam tayang, dan harga tiket.
Saat memilih film atau jadwal lain, warna kursi diperbarui berdasarkan data dalam HashMap.
Tabel Pemesanan:

Menggunakan DefaultTableModel untuk menampilkan data pemesanan.
Tabel memungkinkan penambahan, pengeditan, dan penghapusan data.
Validasi:

Memastikan semua input lengkap sebelum pemesanan.
Mengecek apakah jumlah kursi yang dipilih sesuai dengan jumlah tiket.
Teknologi yang Digunakan
Java Swing: Untuk GUI.
DefaultTableModel: Untuk menyimpan dan menampilkan data tabel.
HashMap: Untuk melacak status kursi berdasarkan kombinasi film, jam tayang, dan harga tiket.
