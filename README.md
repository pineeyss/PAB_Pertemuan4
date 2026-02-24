# PAB_Pertemuan4.

#### Nama : Ravina Eka Adiya
#### Nim : 2409116078
#### Kelas : B
#### Mata Kuliah : Pemrograman Aplikasi Bergerak
#

#### main.dart
Kode ini adalah file utama (`main.dart`) yang menjalankan aplikasi Flutter dengan `ChangeNotifierProvider` untuk menyediakan `CartModel` ke seluruh aplikasi. `MyApp` mengatur konfigurasi `MaterialApp` seperti tema dan halaman awal, yaitu `ProductListPage`, sehingga fitur keranjang belanja bisa diakses dan dikelola dari berbagai halaman menggunakan Provider.

#

#### pubspec.yaml
Kode ini adalah file `pubspec.yaml` yang berisi konfigurasi proyek Flutter, seperti nama aplikasi, versi, dan batasan SDK. Di bagian `dependencies` ditambahkan package `provider` untuk state management, sedangkan `dev_dependencies` berisi kebutuhan testing dan lints. Opsi `uses-material-design: true` mengaktifkan penggunaan komponen Material Design di aplikasi.

#
## **LIB**
### Models
#### A. cart_item.dart
kode ini digunakan untuk merepresentasikan satu item di dalam keranjang belanja, di mana setiap CartItem menyimpan satu Product beserta jumlah yang dibeli.

#### B. cart_model.dart
kode ini berfungs sebagai pengelola state keranjang belanja menggunakan ChangeNotifier pada flutter. data keranjang disimpan dalam bentuk 'Map<String, CartItem>' agar pencarian produk berdasarkan id lebih cepat.

#### C. counter_model.dart
kode ini berfungs sebagai pengelola state keranjang belanja menggunakan ChangeNotifier pada flutter. variabel _count dibuat private untuk menjaga keamanan data, lalu diakses melalui getter count.

#### D. product.dart
kode ini mendefinisikan class product yang digunakan untuk merepresentasikan data produk, seperti `id`, `name`, `price`, `emoji`, dan `description`.

#
### Pages
#### A. cart_page.dart
kode ini menampilkan dan mengelola isi keranjang belanja menggunakan `Provider` dan `CartModel`. jika kosong akan muncul pesan, jika ada isi akan ditampilkan daftar produk lengkap dengan kontrol jumlah, hapus item, total harga, serta tombol checkout. tampilan otomatis ter-update karena menggunakan `Consumer`.

#### B. counter_display_page.dart
kode ini hanya menampilkan nilai counter yang dikirim dari halaman sebelumnya melalui parameter counter. karena hanya menerima data tanpa akses untuk mengubahnya, halaman ini hanya bisa menampilkan nilai tersebut dan tidak bisa melakukan increment atau perubahan state.

#### C. counter_page.dart
kode ini menggunakan StatefulWidget dan setState untuk mengelola state lokal _counter. tombol Increment dan Reset digunakan untuk mengubah nilai counter dan memicu rebuild widget, sedangkan tombol View Counter akan berpindah ke CounterDisplayPage sambil mengirim nilai counter saat ini sebagai parameter.

#### D. counter_provider_page.dart
Kode ini menggunakan provider untuk mengelola state `CounterModel`. nilai counter ditampilkan melalui `Consumer`, sehingga hanya bagian teks angka yang akan rebuild saat nilainya berubah, bukan seluruh halaman. Tombol Increment, Decrement, dan Reset memanggil method pada `CounterModel` menggunakan `context.read()`, sehingga perubahan state langsung memperbarui UI secara otomatis.

#### E. home_page.dart
Kode ini adalah halaman `HomePage` yang menggunakan `StatefulWidget` untuk mengelola state lokal `_counter` dengan `setState`. Nilai counter ditampilkan di body dan juga sebagai badge merah di AppBar. Tombol **Increment** menambah nilai counter, sedangkan tombol **Go to Profile** akan berpindah ke `ProfilePage` sambil mengirim nilai counter dan fungsi `_reset` sebagai callback agar halaman lain bisa mengakses dan mereset data tersebut.

#### F. product_list_page.dart
Kode ini adalah halaman `ProductListPage` yang menampilkan daftar produk dalam bentuk grid dengan data dummy. Setiap produk memiliki tombol **Add** untuk menambahkan item ke keranjang menggunakan `CartModel` dari Provider. Di AppBar terdapat ikon keranjang dengan badge jumlah item yang otomatis ter-update melalui `Consumer`, dan saat ditekan akan menuju ke `CartPage` untuk melihat isi keranjang.

#### G. profile_page.dart
Kode ini adalah halaman `ProfilePage` yang menerima nilai `counter` dan fungsi `onReset` dari `HomePage`. Nilai counter ditampilkan sebagai “Points”, lalu diteruskan lagi ke `SettingsPage` saat tombol **Go to Settings** ditekan, sehingga data dan callback tetap bisa digunakan di halaman berikutnya.

#### H. settings_page.dart
Kode ini adalah halaman `ProfilePage` yang menerima nilai `counter` dan fungsi `onReset` dari `HomePage`. Nilai counter ditampilkan sebagai “Points”, lalu diteruskan lagi ke `SettingsPage` saat tombol **Go to Settings** ditekan, sehingga data dan callback tetap bisa digunakan di halaman berikutnya.

