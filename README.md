# PAB_Pertemuan4.

#### Nama : Ravina Eka Adiya
#### Nim : 2409116078
#### Kelas : B
#### Mata Kuliah : Pemrograman Aplikasi Bergerak
#

## LIB

### Models
#### A. cart_item.dart
kode ini digunakan untuk merepresentasikan satu item di dalam keranjang belanja, di mana setiap CartItem menyimpan satu Product beserta jumlah yang dibeli.

#### B. cart_model.dart
kode ini berfungs sebagai pengelola state keranjang belanja menggunakan ChangeNotifier pada flutter. data keranjang disimpan dalam bentuk 'Map<String, CartItem>' agar pencarian produk berdasarkan id lebih cepat.

#### C. counter_model.dart
kode ini berfungs sebagai pengelola state keranjang belanja menggunakan ChangeNotifier pada flutter. variabel _count dibuat private untuk menjaga keamanan data, lalu diakses melalui getter count.

#### D. product.dart
kode ini mendefinisikan class product yang digunakan untuk merepresentasikan data produk, seperti `id`, `name`, `price`, `emoji`, dan `description`.
