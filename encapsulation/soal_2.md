## Buatkan kelas Student dengan kriteria sebagai berikut :

### Kriteria Kelas Person (Induk):
#### Atribut:
- Nama(`name`): hanya dapat diakses dan diubah dari luar kelas melalui properti.
- Alamat (`address`): hanya bisa diakses di dalam kelas dan oleh kelas turunan.
- Nomor Telepon (`phoneNumber`): hanya bisa diakses oleh kelas Person sendiri.

#### Fungsi:
- Method `DisplayPersonalInfo()` yang akan menampilkan informasi pribadi `(Nama dan Alamat)`.

### Kriteria Kelas Student (Turunan dari Person):
#### Atribut:
- NIM(`nim`): hanya dapat diakses dan diubah melalui properti.
- IPK (`gpa`): sama seperti soal sebelumnya, tetapi dengan validasi tambahan, yaitu mahasiswa dengan IPK **kurang dari** 2.0 akan dianggap dalam kondisi **"warning"**.

#### Fungsi:
- Method `DisplayStudentInfo()` yang menampilkan data lengkap mahasiswa `(Nama, Alamat, NIM, dan IPK)`.
- Method `CheckGPAStatus()` yang akan memeriksa status akademik mahasiswa. **Jika IPK di bawah 2.0**, tampilkan pesan "Warning: Your GPA is below the minimum threshold."

#### Konstruktor:
Gunakan konstruktor untuk menginisialisasi nilai dari atribut `name`, `nim`, dan `gpa` saat objek Student dibuat.

---

##### Output yang diharapkan =
```cs
Nama: Alice
Alamat: Jl.Merpati No. 5
NIM: 123456
IPK: 1.8
Warning: Your GPA is below the minimum threshold.
```