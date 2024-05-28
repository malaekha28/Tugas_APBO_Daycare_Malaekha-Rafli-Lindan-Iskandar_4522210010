# Tugas_APBO_Daycare_Malaekha-Rafli-Lindan-Iskandar_4522210010
#Class Diagram
![PLANT_UML](https://github.com/malaekha28/Tugas_APBO_Daycare_Malaekha-Rafli-Lindan-Iskandar_4522210010/assets/145976346/55ed7289-c543-49ff-a607-f07b35c13183)
1. OrangTua/Wali:
Class ini merepresentasikan orang tua atau wali dari anak-anak yang terdaftar dalam sistem daycare.
Atribut:
ID_Ortu: ID unik untuk setiap orang tua/wali.
Nama: Nama lengkap orang tua/wali.
Alamat: Alamat tempat tinggal orang tua/wali.
No_Telepon: Nomor telepon yang dapat dihubungi.
Email: Alamat email.
Method:
setNama(nama: string): Mengatur nama orang tua/wali.
getNama(): Mengambil nama orang tua/wali.
setAlamat(alamat: string): Mengatur alamat orang tua/wali.
getAlamat(): Mengambil alamat orang tua/wali.
setNoTelepon(noTelepon: string): Mengatur nomor telepon orang tua/wali.
getNoTelepon(): Mengambil nomor telepon orang tua/wali.
setEmail(email: string): Mengatur alamat email orang tua/wali.
getEmail(): Mengambil alamat email orang tua/wali.

2. Anak:
Class ini merepresentasikan anak yang terdaftar dalam sistem daycare.
Atribut:
ID_Anak: ID unik untuk setiap anak.
Nama: Nama lengkap anak.
Tanggal_Lahir: Tanggal lahir anak.
ID_Ortu: ID orang tua/wali yang terkait.
ID_Staf: ID staf yang bertanggung jawab atas anak tersebut.
Method:
setNama(nama: string): Mengatur nama anak.
getNama(): Mengambil nama anak.
setTanggalLahir(tanggalLahir: date): Mengatur tanggal lahir anak.
getTanggalLahir(): Mengambil tanggal lahir anak.
setIDOrtu(idOrtu: int): Mengatur ID orang tua/wali.
getIDOrtu(): Mengambil ID orang tua/wali.
setIDStaf(idStaf: int): Mengatur ID staf yang bertanggung jawab.
getIDStaf(): Mengambil ID staf yang bertanggung jawab.

3. Staf:
Class ini merepresentasikan staf daycare yang bertanggung jawab atas pengelolaan anak-anak.
Atribut:
ID_Staf: ID unik untuk setiap staf.
Nama: Nama lengkap staf.
Jabatan: Jabatan atau posisi dalam daycare.
No_Telepon: Nomor telepon yang dapat dihubungi.
Email: Alamat email.
Method:
setNama(nama: string): Mengatur nama staf.
getNama(): Mengambil nama staf.
setJabatan(jabatan: string): Mengatur jabatan staf.
getJabatan(): Mengambil jabatan staf.
setNoTelepon(noTelepon: string): Mengatur nomor telepon staf.
getNoTelepon(): Mengambil nomor telepon staf.
setEmail(email: string): Mengatur alamat email staf.
getEmail(): Mengambil alamat email staf.

4. Kehadiran:
Class ini merepresentasikan kehadiran anak di daycare.
Atribut:
ID_Kehadiran: ID unik untuk setiap catatan kehadiran.
ID_Anak: ID anak yang bersangkutan.
Tanggal: Tanggal kehadiran.
Waktu_Masuk: Waktu masuk anak.
Waktu_Keluar: Waktu keluar anak.
Method:
setIDAnak(idAnak: int): Mengatur ID anak.
getIDAnak(): Mengambil ID anak.
setTanggal(tanggal: date): Mengatur tanggal kehadiran.
getTanggal(): Mengambil tanggal kehadiran.
setWaktuMasuk(waktuMasuk: time): Mengatur waktu masuk anak.
getWaktuMasuk(): Mengambil waktu masuk anak.
setWaktuKeluar(waktuKeluar: time): Mengatur waktu keluar anak.
getWaktuKeluar(): Mengambil waktu keluar anak.
Dan seterusnya untuk class Kegiatan, Kesehatan, dan LaporanAktivitas. Dengan class diagram ini, struktur dan hubungan antar entitas dalam sistem daycare dapat dipahami dengan lebih baik.

#ERD
![ERD](https://github.com/malaekha28/Tugas_APBO_Daycare_Malaekha-Rafli-Lindan-Iskandar_4522210010/assets/145976346/b8160a53-b51d-4d8b-8c67-31e847fa30a4)
1. Orang Tua (OrangTua):
Representasi orang tua atau wali dari anak-anak dalam sistem daycare.
Memiliki atribut:
ID_Ortu: ID unik untuk setiap orang tua/wali.
Nama: Nama lengkap orang tua/wali.
Alamat: Alamat tempat tinggal orang tua/wali.
No_Telepon: Nomor telepon yang dapat dihubungi.
Email: Alamat email.
Hubungan:
Orang Tua memiliki hubungan one-to-many dengan Anak, yang diwakili oleh kardinalitas 1 ke n.

2. Anak:
Mewakili anak-anak yang terdaftar dalam sistem daycare.
Memiliki atribut:
ID_Anak: ID unik untuk setiap anak.
Nama: Nama lengkap anak.
Tanggal_Lahir: Tanggal lahir anak.
ID_Ortu: ID orang tua/wali yang terkait.
ID_Staf: ID staf yang bertanggung jawab atas anak tersebut.
Hubungan:
Anak memiliki hubungan one-to-many dengan Kehadiran, yang diwakili oleh kardinalitas 1 ke n.
Anak memiliki hubungan one-to-many dengan Kegiatan, yang diwakili oleh kardinalitas 1 ke n.
Anak memiliki hubungan one-to-many dengan Kesehatan, yang diwakili oleh kardinalitas 1 ke n.
Anak memiliki hubungan one-to-many dengan Laporan Aktivitas, yang diwakili oleh kardinalitas 1 ke n.
Anak memiliki hubungan many-to-one dengan Staf, yang diwakili oleh kardinalitas n ke 1.
Anak memiliki hubungan many-to-one dengan Orang Tua, yang diwakili oleh kardinalitas n ke 1.

3. Staf:
Mewakili staf daycare yang bertanggung jawab atas pengelolaan anak-anak.
Memiliki atribut:
ID_Staf: ID unik untuk setiap staf.
Nama: Nama lengkap staf.
Jabatan: Jabatan atau posisi dalam daycare.
No_Telepon: Nomor telepon yang dapat dihubungi.
Email: Alamat email.
Hubungan:
Staf memiliki hubungan one-to-many dengan Kegiatan, yang diwakili oleh kardinalitas 1 ke n.
Staf memiliki hubungan one-to-many dengan Laporan Aktivitas, yang diwakili oleh kardinalitas 1 ke n.

4. Kehadiran:
Mewakili catatan kehadiran anak di daycare.
Memiliki atribut:
ID_Kehadiran: ID unik untuk setiap catatan kehadiran.
ID_Anak: ID anak yang bersangkutan.
Tanggal: Tanggal kehadiran.
Waktu_Masuk: Waktu masuk anak.
Waktu_Keluar: Waktu keluar anak.
Hubungan:
Kehadiran memiliki hubungan many-to-one dengan Anak, yang diwakili oleh kardinalitas n ke 1.

#USE CASE
![USE CASE](https://github.com/malaekha28/Tugas_APBO_Daycare_Malaekha-Rafli-Lindan-Iskandar_4522210010/assets/145976346/c5f73d9a-de82-448e-a0a8-f0551ca16723)
1. Pendaftaran Anak:
Aktor: Orang Tua/Wali
Deskripsi: Orang tua atau wali mendaftarkan anak mereka ke daycare. Mereka memberikan informasi seperti nama anak, tanggal lahir, alamat, nomor telepon, dan email kepada staf daycare.
Alur:
-Orang tua/wali datang ke daycare untuk mendaftarkan anak mereka.
-Orang tua/wali memberikan informasi pribadi anak dan informasi kontak kepada staf.
-Staf daycare memasukkan informasi tersebut ke dalam sistem.

2. Kehadiran Anak:
Aktor: Staf
Deskripsi: Staf daycare mencatat kehadiran setiap anak saat tiba di daycare dan saat pulang. Hal ini mencatat waktu kedatangan dan waktu kepulangan anak.
Alur:
-Anak tiba di daycare bersama orang tua/walinya.
-Staf daycare memeriksa kehadiran anak dan mencatat waktu kedatangan.
-Ketika anak pulang, staf daycare juga mencatat waktu kepulangan anak.
-Informasi kehadiran anak, termasuk waktu kedatangan dan waktu kepulangan, dimasukkan ke dalam sistem.

3. Kegiatan Harian:
Aktor: Staf, Anak
Deskripsi: Staf daycare merencanakan dan mengelola kegiatan harian untuk anak-anak. Anak-anak terlibat dalam kegiatan-kegiatan tersebut.
Alur:
-Staf daycare merencanakan kegiatan harian berdasarkan usia dan minat anak-anak.
-Staf daycare mengumumkan kegiatan kepada anak-anak dan membimbing mereka selama kegiatan berlangsung.
-Anak-anak berpartisipasi dalam kegiatan yang direncanakan.

4. Catatan Kesehatan Anak:
Aktor: Staf
Deskripsi: Staf daycare mencatat informasi kesehatan anak seperti riwayat penyakit, alergi, atau catatan kesehatan lainnya.
Alur:
-Staf daycare mengumpulkan informasi kesehatan dari orang tua/wali saat pendaftaran anak.
-Staf daycare mencatat setiap perubahan dalam kesehatan anak yang terjadi selama berada di daycare.
-Informasi kesehatan anak disimpan secara terstruktur dalam sistem.

5. Laporan Aktivitas Anak:
Aktor: Staf
Deskripsi: Staf daycare membuat laporan aktivitas harian untuk setiap anak yang berisi rangkuman kegiatan yang dilakukan, perkembangan anak, dan observasi staf.
Alur:
-Staf daycare mencatat observasi mereka tentang perilaku, perkembangan, dan interaksi anak selama hari itu.
-Informasi ini disusun menjadi laporan aktivitas harian yang disampaikan kepada orang tua/wali pada akhir hari.
-Orang tua/wali memiliki akses untuk melihat laporan aktivitas anak melalui sistem daycare.
-Dengan use case ini, berbagai aktivitas yang dilakukan oleh orang tua/wali, staf daycare, dan anak-anak dalam sistem daycare dapat dijelaskan dengan baik. Use case ini membantu menggambarkan fungsionalitas sistem -dan interaksi antara pengguna dan sistem.
