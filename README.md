# EAS_PI
### Nama : Anggada Putra Nagamas
### NRP  : 05311840000025

## **Penjelasan Aplikasi :**
* EAS_PI merupakan website sederhana yang memungkinkan pengguna untuk melakukan donasi dan melihat daftar donasi. Input pada website ini berupa nama, gender, jenis donasi, dan jumlah donasi. Output pada website ini berupa daftar donasi (nama, jenis donasi, dan jumlah donasi).

## **Setup Program :**
* Database yang digunakan yaitu donasi.sql

## **Controller :**
* **Index()** : digunakan untuk mengatur $_SESSION yang akan digunakan dan mengarahkan view yang digunakan jika belum mengisi dan sudah mengisi informasi donatur.
* **Filter()** : digunakan untuk filter pada view rekap donasi atau daftar donasi yang telah diinput sebelumnya.
* **inputData()** : digunakan untuk menginput data pada $_SESSION ke dalam database.

## **Models :**
Model yang digunakan yaitu model sumbangan.
Struktur dari tabel yang digunakan yaitu:
Tabel sumbangan :
  * **s_id** : untuk menyimpan data id donasi.
  * **p_id** : untuk menyimpan data id donatur.
  * **j_id** : untuk menyimpan data id jenis donasi.
  * **jumlah** : untuk menyimpan data jumlah donasi.
Tabel penyumbang :
  * **id** : untuk menyimpan data id donatur.
  * **name** : untuk menyimpan data nama donatur.
  * **gender** : untuk menyimpan data gender donatur.
Tabel jenis_sumbangan :
  * **id** : untuk menyimpan data id jenis donasi.
  * **barang** : untuk menyimpan data jenis donasi atau item yang didonasikan. 

Method yang digunakan pada model sumbangan :
  * **getName()** : digunakan untuk mendapatkan jenis donasi yang diinputkan.
  * **setUser()** : digunakan untuk menginputkan semua data donatur (nama, gender, id, dll). 
  * **isThere()** : digunakan untuk mendapatkan id dari jenis donasi.
  * **setJS()** : digunakan untuk menginputkan data jenis donasi ke dalam database.
  * **setSumbangan()** : digunakan untuk menginputkan semua data donasi (nama, gender, id, jumlah, jenis, dll).
  * **getSumbangan()** : digunakan untuk mendapatkan semua data donasi (daftar donasi).
  * **getFilterSumbangan()** : digunakan untuk mendapatkan data donasi berdasarkan donatur (name).
  
## **Views :**
Pada EAS_PI saya menggunakan 3 views yaitu: home, sumbangan, dan jenis.
* **home** : digunakan sebagai halaman awal. Pada halaman awal ini pengguna dapat memilih untuk melakukan donasi atau melihat daftar donasi. Ketika pengguna menekan tombol "Donasi" maka pengguna akan berpindah ke halaman donasi, sedangkan ketika pengguna menekan tombol "Daftar Donasi" maka pengguna akan berpindah ke halaman daftar donasi.

![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/eashome.PNG)

* **sumbangan** : digunakan untuk menampilkan halaman donasi. Pada halaman ini pengguna dapat melakukan input data donasi seperti nama, jenis kelamin (gender), jenis donasi, dan jumlah donasi.
![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/eassumbang.PNG)

Gambar di bawah ini adalah tampilan atau output ketika input data donasi berhasil dilakukan
![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/eassumbanganinput.PNG)

* **jenis** : digunakan untuk menampilkan halaman daftar donasi. Pada halaman ini pengguna dapat melihat rekap donasi. Selain itu terdapat fitur search untuk mencari rekap donasi sesuai dengan yang kita inginkan, baik rekap donasi berdasarkan nama penyumbang, jenis donasi, dan jumlah donasi.
![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/easjenis.PNG)

Gambar di bawah ini adalah filter daftar donasi berdasarkan jenis donasi.

![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/easjenis2.PNG)

Gambar di bawah ini adalah filter daftar donasi berdasarkan nama donatur.

![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/easjenis3.PNG)
