# EAS_PI
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
* **home** : digunakan sebagai halaman awal. Pada halaman awal ini pengguna dapat memilih untuk melakukan donasi atau melihat daftar donasi.
![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/eashome.PNG)

* **sumbangan** : digunakan untuk menampilkan halaman donasi. Pada halaman ini pengguna dapat melakukan input data donasi.
![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/eassumbang.PNG)

![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/eassumbanganinput.PNG)

* **jenis** : digunakan untuk menampilkan halaman daftar donasi. Pada halaman ini pengguna dapat melihat rekap donasi.
![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/easjenis.PNG)

![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/easjenis2.PNG)

![alt text](https://github.com/anggadaputra11319/EAS_PI/blob/master/screenshoteas/easjenis3.PNG)
