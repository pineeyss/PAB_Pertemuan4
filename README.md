# PAB_Pertemuan4.

#### Nama : Ravina Eka Adiya
#### Nim : 2409116078
#### Kelas : B
#### Mata Kuliah : Pemrograman Aplikasi Bergerak
#

## Struktur dan Penjelasan Kode

#

##### <img width="169" height="22" alt="Tangkapan Layar 2026-02-25 pukul 11 26 01" src="https://github.com/user-attachments/assets/01a09698-146c-458d-8d32-cb43e448e98b" />

##### pubspec.yaml
file ini berisi konfigurasi proyek Flutter, seperti nama aplikasi, versi, dan batasan SDK.

#
### **LIB**

#### Models
##### <img width="160" height="134" alt="Tangkapan Layar 2026-02-25 pukul 11 25 20" src="https://github.com/user-attachments/assets/9eeaea80-9e6e-43a7-a75d-499d73c95a41" />

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
##### <img width="169" height="264" alt="Tangkapan Layar 2026-02-25 pukul 11 25 36" src="https://github.com/user-attachments/assets/81f68ac7-0d19-4098-89de-52684755ab45" />

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

##### <img width="172" height="85" alt="Tangkapan Layar 2026-02-25 pukul 11 25 50" src="https://github.com/user-attachments/assets/1a3debdd-ae31-4011-aeb6-cf1d11d6387b" />

##### main.dart
file ini adalah file utama yang menjalankan aplikasi Flutter dengan `ChangeNotifierProvider` untuk menyediakan `CartModel` ke seluruh aplikasi.

#

## Dokumentasi Program

##### <img width="2560" height="1606" alt="image" src="https://github.com/user-attachments/assets/708bc06f-80c1-4044-ad5e-28df90a369f1" />
##### Tampilan utama dari program ini.
#

##### <img width="286" height="48" alt="Tangkapan Layar 2026-02-25 pukul 11 42 36" src="https://github.com/user-attachments/assets/bd79a595-b999-4dc7-bc34-b59bf9727cff" />
##### 1. Add to cart from product list.
#

##### <img width="506" height="208" alt="image" src="https://github.com/user-attachments/assets/ab2785f7-2c5d-4748-94c3-44171fe4ba60" />
##### 2. Show cart items dengan quantity.
#

##### <img width="267" height="112" alt="Tangkapan Layar 2026-02-25 pukul 11 55 18" src="https://github.com/user-attachments/assets/db8db630-b376-4396-b110-b33b95642a80" />
##### 3. Update quantity (+/-).
#

##### <img width="223" height="50" alt="Tangkapan Layar 2026-02-25 pukul 12 00 31" src="https://github.com/user-attachments/assets/66d51e3f-c5b6-4646-979c-dbcddd99ebdd" />
##### 4. Remove items from cart
#

##### <img width="612" height="539" alt="Tangkapan Layar 2026-02-25 pukul 12 03 42" src="https://github.com/user-attachments/assets/80a93735-7263-4e00-936d-0c49d832abba" />
##### 5. Display total price correctly
#

##### <img width="966" height="132" alt="image" src="https://github.com/user-attachments/assets/bc7c1fd5-a10e-4d47-bafb-ba6203452051" />
##### 6. Search/Filter
#

##### <img width="500" height="211" alt="Tangkapan Layar 2026-02-25 pukul 12 06 03" src="https://github.com/user-attachments/assets/6af1f2d6-584d-4091-bded-9a4e99e39ca0" />
##### 7. Categories
#
