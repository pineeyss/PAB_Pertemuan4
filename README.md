# PAB_Pertemuan4.

#### Nama : Ravina Eka Adiya
#### Nim : 2409116078
#### Kelas : B
#### Mata Kuliah : Pemrograman Aplikasi Bergerak
#

## Struktur dan Penjelasan Kode

##### main.dart
file ini adalah file utama yang menjalankan aplikasi Flutter dengan `ChangeNotifierProvider` untuk menyediakan `CartModel` ke seluruh aplikasi.

#

##### pubspec.yaml
file ini berisi konfigurasi proyek Flutter, seperti nama aplikasi, versi, dan batasan SDK.

#
### **LIB**
#### Models
##### A. cart_item.dart
file ini digunakan untuk merepresentasikan satu item di dalam keranjang belanja, di mana setiap CartItem menyimpan satu Product beserta jumlah yang dibeli.

##### B. cart_model.dart
file ini berfungsi sebagai pengelola state keranjang belanja menggunakan ChangeNotifier pada flutter. data keranjang disimpan dalam bentuk `Map<String, CartItem>` agar pencarian produk berdasarkan id lebih cepat.

##### C. counter_model.dart
file ini berfungs sebagai pengelola state keranjang belanja menggunakan ChangeNotifier pada flutter. variabel _count dibuat private untuk menjaga keamanan data, lalu diakses melalui getter count.

##### D. product.dart
file ini mendefinisikan class product yang digunakan untuk merepresentasikan data produk, seperti `id`, `name`, `price`, `emoji`, dan `description`.

#
#### Pages
##### A. cart_page.dart
file ini menampilkan dan mengelola isi keranjang belanja menggunakan `Provider` dan `CartModel`. jika kosong akan muncul pesan, jika ada isi akan ditampilkan daftar produk lengkap dengan kontrol jumlah, hapus item, total harga, serta tombol checkout. tampilan otomatis ter-update karena menggunakan `Consumer`.

##### B. counter_display_page.dart
file ini hanya menampilkan nilai counter yang dikirim dari halaman sebelumnya melalui parameter counter. karena hanya menerima data tanpa akses untuk mengubahnya, halaman ini hanya bisa menampilkan nilai tersebut dan tidak bisa melakukan increment atau perubahan state.

##### C. counter_page.dart
file ini menggunakan StatefulWidget dan setState untuk mengelola state lokal _counter. 

##### D. counter_provider_page.dart
file ini menggunakan provider untuk mengelola state `CounterModel`. 

##### E. home_page.dart
file ini adalah halaman yang menggunakan `StatefulWidget` untuk mengelola state lokal `_counter` dengan `setState`.

##### F. product_list_page.dart
file ini adalah halaman yang menampilkan daftar produk dalam bentuk grid dengan data dummy. setiap produk memiliki tombol add untuk menambahkan item ke keranjang menggunakan `CartModel` dari Provider.

##### G. profile_page.dart
file ini adalah halaman yang menerima nilai `counter` dan fungsi `onReset` dari `HomePage`. 

##### H. settings_page.dart
file ini adalah halaman yang menerima nilai `counter` dan fungsi `onReset` dari `HomePage`.

#

## Dokumentasi Program

##### <img width="1280" height="803" alt="Tangkapan Layar 2026-02-25 pukul 00 24 53" src="https://github.com/user-attachments/assets/82bfc00b-589b-44c1-8261-dc78a5af59ee" />

##### <img width="1280" height="803" alt="Tangkapan Layar 2026-02-25 pukul 00 25 00" src="https://github.com/user-attachments/assets/934c4fd9-c9a0-40e4-9b7b-a08b8163ce99" />
##### gambar diatas adalah gambar saat program dijalankan.
#
##### <img width="1280" height="803" alt="Tangkapan Layar 2026-02-25 pukul 00 25 19" src="https://github.com/user-attachments/assets/d27b163e-3752-49be-8e92-f9bd4cd246bf" />
##### dan disini saya mencoba memasukkan 2 item untuk saya checkout.
#
##### <img width="1280" height="803" alt="Tangkapan Layar 2026-02-25 pukul 00 25 40" src="https://github.com/user-attachments/assets/cded8306-f358-4b53-9032-c79508f1b96a" />
##### setelah saya menekan tombol checkout maka akan muncul pop up seperti digambar untuk mengonfirmasi total item yang akan dipesan dan total harga yang akan dibayar.
#
##### <img width="1280" height="803" alt="Tangkapan Layar 2026-02-25 pukul 00 25 51" src="https://github.com/user-attachments/assets/d4de8238-50b1-48c8-92ad-2267d541e629" />
##### setelah saya konfirm untuk melalukan checkout, program langsung kembali ke halaman awal atau home.
