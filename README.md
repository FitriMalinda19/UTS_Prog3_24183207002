# UTS_Prog3_24183207002
![image alt](https://github.com/FitriMalinda19/ujicoba/blob/2b28493381c6e0a82f9cc89e9865130cff418cd8/ssrun.png)
![iimage alt]()
Atribut Utama (Variabel Global)
- daftarPesanan: Sebuah ArrayList untuk menampung daftar item makanan/minuman yang dipilih oleh pelanggan sebelum dicetak ke struk.
- totalBiaya: Variabel integer untuk menyimpan akumulasi total harga yang harus dibayar.

Fungsi/Method Utama
- Pertemuan_6() (Constructor): Bagian yang dijalankan pertama kali. Fungsinya untuk mengisi data otomatis seperti tanggal hari ini dan pilihan di dropdown (ComboBox) untuk Kasir dan Kategori.
- bersihkanLayar(): Fungsi pembantu untuk mengosongkan kembali semua field dan meriset variabel ke kondisi awal. Fungsi ini juga mengisi ulang tanggal_field dengan tanggal sistem terbaru agar aplikasi siap digunakan kembali.

Logika Interaksi Pengguna
- dropdown_kategoriActionPerformed: Berfungsi untuk mengubah isi daftar menu di JList (list_menu) secara dinamis berdasarkan kategori yang dipilih (Makanan, Minuman, atau Snack).
- tambah_buttonActionPerformed:
   • Mengambil menu yang dipilih dan jumlahnya.
   • Memisahkan teks harga dari nama menu menggunakan split(" - ").
   • Menghitung sub-total (harga \times jumlah) dan menambahkannya ke dalam daftarPesanan serta menjumlahkannya ke totalBiaya.
- total_buttonActionPerformed: Menampilkan kepada pengguna berapa total biaya sementara yang harus dibayar.
- pesan_buttonActionPerformed (Proses Checkout):
   • Validasi: Memastikan daftar pesanan tidak kosong dan uang pembayaran cukup.
   • Perhitungan: Menghitung uang kembalian berdasarkan input pembayaran.
   • Pengambilan Data: Menentukan metode pembayaran dan mengambil data tanggal langsung dari layar menggunakan fungsi .getText() agar data tidak bernilai null.
   • Cetak Struk: Menggabungkan semua data (termasuk tanggal dan pelanggan) menjadi satu string teks panjang dan menampilkannya melalui JOptionPane.

Komponen GUI yang Digunakan
- JTextField: Untuk input teks (nama pelanggan, nomor meja, jumlah, bayar, dan penampilan tanggal otomatis).
- JComboBox: Menu pilihan dropdown untuk kategori dan kasir.
- JList: Untuk menampilkan daftar menu yang tersedia.
- JRadioButton: Untuk memilih satu di antara dua metode pembayaran (Cash/Transfer).
- JOptionPane: Untuk menampilkan pesan peringatan (validasi) dan jendela struk belanja.
- JPanel: Kanvas atau area untuk menaruh dan mengelompokkan semua komponen agar tertata rapi.
- JLabel: Tulisan petunjuk atau instruksi statis agar pengguna tahu kotak mana yang harus diisi.
