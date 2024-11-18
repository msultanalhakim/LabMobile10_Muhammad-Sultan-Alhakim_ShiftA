# Tugas Praktikum Mobile - Pertemuan 10

Nama: Muhammad Sultan Alhakim

NIM: H1D022105

Shift: A

Untuk mengimplementasikan autentikasi login menggunakan akun Google hingga aplikasi dapat menampilkan username dan profil pengguna, langkah-langkah yang perlu disiapkan yaitu:

1. Siapkan Firebase

Langkah pertama yang dilakukan adalah menyiapkan Firebase Authentication di Firebase Console. Pada bagian Sign-in method di Authentication, metode login menggunakan Google diaktifkan. Setelah itu, aplikasi akan mendapatkan Client ID dari Firebase yang diperlukan untuk mengonfigurasi aplikasi agar dapat menggunakan Google Sign-In. Setelah login Google diaktifkan, Anda akan mendapatkan Client ID dari Firebase yang diperlukan untuk mengonfigurasi aplikasi agar dapat menggunakan Google Sign-In. Selanjutnya, Anda mengonfigurasi aplikasi untuk menggunakan Google Sign-In, di mana aplikasi akan meminta izin kepada pengguna untuk mengakses data dasar mereka, seperti nama lengkap (displayName), alamat email (email), dan foto profil (photoURL). Izin ini sangat penting karena aplikasi perlu data tersebut untuk menampilkan informasi pengguna.Kemudian, aplikasi dikonfigurasi untuk meminta izin kepada pengguna untuk mengakses data dasar mereka, seperti nama lengkap, email, dan foto profil. Izin ini diperlukan agar aplikasi bisa menampilkan informasi pengguna setelah mereka berhasil login.

2. Proses Autentikasi

Proses autentikasi dimulai ketika pengguna memilih untuk login menggunakan akun Google di aplikasi. Setelah pengguna memilih akun mereka, aplikasi akan meminta izin dari pengguna untuk mengakses data dasar mereka, termasuk nama, email, dan foto profil.
Setelah izin diberikan, aplikasi menerima sebuah token autentikasi dari Google. Token ini berfungsi sebagai bukti bahwa pengguna telah berhasil login dengan akun Google mereka. Token tersebut kemudian dikirimkan ke Firebase untuk memverifikasi identitas pengguna. Firebase akan memeriksa token dan memastikan bahwa akun yang digunakan valid.

Jika autentikasi berhasil, Firebase akan mengembalikan informasi pengguna dalam bentuk objek user. Objek ini berisi data seperti nama lengkap (displayName), email, dan foto profil (photoURL). Informasi-informasi ini akan digunakan oleh aplikasi untuk menampilkan data pengguna di antarmuka pengguna.

3. Proses Fetching Data

Setelah proses login berhasil, aplikasi akan menggunakan informasi dari objek user yang diberikan oleh Firebase untuk menampilkan data pengguna di aplikasi. Foto profil, nama lengkap, dan email pengguna akan ditampilkan pada halaman profil. Data ini diambil dari objek user yang dikembalikan oleh Firebase, seperti user.displayName untuk nama, user.email untuk email, dan user.photoURL untuk foto profil. Selain itu, aplikasi juga menyediakan opsi logout. Ketika pengguna memilih untuk logout, aplikasi akan mengakhiri sesi login dengan Firebase dan Google, serta menghapus data pengguna yang ada di aplikasi. Proses logout ini memastikan bahwa sesi login berakhir dengan baik dan data pengguna tidak disimpan secara permanen.


![image](https://github.com/user-attachments/assets/ee399b63-d743-4905-974a-e4d19281cacb)

![Screenshot 2024-11-13 152437](https://github.com/user-attachments/assets/651d676c-9e5a-40d7-a92a-a08d9c3d607b)

![image](https://github.com/user-attachments/assets/914cfb23-d29d-4e9d-97e5-35d2c4014ea8)
![image](https://github.com/user-attachments/assets/c43c2ab4-af2b-4377-a92d-08717a97be38)
