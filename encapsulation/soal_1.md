## Buatkan kelas Student dengan kriteria sebagai berikut :

#### Atribut:
- Nama(`name`): hanya bisa diakses dan dimodifikasi dari luar kelas.
- NIM (Nomor Induk Mahasiswa) (`nim`): tidak boleh diakses langsung dari luar kelas, tetapi bisa dimodifikasi dan dilihat melalui properti.
- IPK (Indeks Prestasi Kumulatif) (`gpa`): tidak boleh diakses atau diubah langsung dari luar kelas. Hanya bisa diubah jika nilainya valid (nilai antara 0.0 dan 4.0).

#### Fungsi:
Sebuah method `DisplayInfo()` untuk menampilkan informasi lengkap tentang mahasiswa `(Nama, NIM, IPK)`.
Properti untuk mengakses dan memodifikasi NIM dan IPK sesuai aturan yang sudah disebutkan di atas.