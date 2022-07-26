# Laporan Praktek


###### Nama  : Andico Novalino Andryanto :shipit:
###### Kelas : XII RPL 1 :cold_face:
###### Absen : 15 :pirate_flag:

## Modul 1
Soal nomor 1
Melakukan proses instalasi framework laravel kedalam folder dengan nama masing masing

![image](https://user-images.githubusercontent.com/91455522/180902947-7ce2c6ef-1579-45e6-b314-47ad4dc3ea4c.png)

## Modul 2
Soal Nomor 1
Buatlah migration tabel kategori menggunakan teknik yang telah di pelajari dalam 
mdoul ini.

**Langkah pertama**
> membuat migration dalam command prompt :sunglasses: ![image](https://user-images.githubusercontent.com/91455522/180904477-a003b2ab-022e-40c1-9a56-27de431b79c0.png)

**Langkah kedua**
> setelah melakukan perintah pada cmd akan membuat file migration baru dengan nama **2022_07_25_034957_create_produk_table.php** pada database penjualan seperti dibawah ini![image](https://user-images.githubusercontent.com/91455522/180905506-dc443201-6e15-45e7-96bd-de56dc011c89.png)

**Langkah ketiga**
> buka file **2022_07_25_034957_create_produk_table.php** lalu ubah script, menjadi script dibawah ini![image](https://user-images.githubusercontent.com/91455522/180906176-f258dcfc-0b5d-4c47-befd-36730636a219.png)

**Langkah keempat**
> setelah melakukan langkah ketiga, ketik perintah ``` php artisan migrate ``` untuk menjalan kan method run() pada file migration menghasilkan tabel pada database penjualan.![image](https://user-images.githubusercontent.com/91455522/180907386-9f24e83b-e072-41d8-a2d3-0e764c55c384.png)![image](https://user-images.githubusercontent.com/91455522/180907785-b162bda2-6fa9-435d-83fe-6052782abaf0.png) Muncul 6 table baru pada gambar di atas yang dibuat dari file migration yang baru saja dibuat.

**Langkah kelima**
> kita akan mencoba script ``` php artisan migrate:rollback ``` fungsi script di pinggir ini digunakan untuk menghapus tabel atau mengembalikan satu operasi terakhir yang telah dilakukan seperti pada contoh dibawah ini![image](https://user-images.githubusercontent.com/91455522/180908298-789be67b-2362-4131-8cb4-2f8959ed7959.png)
ada juga script untuk mengembalikan 2 operasi terakhir ``` php artisan migrate:rollback -step=5 ``` juga terdapat script me rollback seluruh operasi migration dengan script ``` php artisan migrate:rollback ``` ada kalanya kita menggunakan script ``` php artisan migrate:refresh ``` untuk me rollback seluruh operasi migration dan langsung menjalankan migration.

**Langkah keenam**
> kita akan memodifikasi tabel migration dengan menggunakan perintah Schema::create().atau Schema::rename() untuk mengubah nama.kita akan membuat migration baru ubah_tabel_produk ``` php make migration: ubah_tabel_produk ```, selanjutnya ubah method up() pada migration yang baru saja kita buat 
![image](https://user-images.githubusercontent.com/91455522/180909623-87a6ca6f-d924-450f-af1d-c0fe0bc12c35.png) 
![image](https://user-images.githubusercontent.com/91455522/180910612-65e2f6d6-86ba-48a4-a292-777c723da9a5.png)
![image](https://user-images.githubusercontent.com/91455522/180907785-b162bda2-6fa9-435d-83fe-6052782abaf0.png)

**Langkah ketuju**
> kita akan membuat model dengan nama barang ``` php artisan make:model barang ```  lalu tambah protected pada model barang untuk mendefinisikan satu variabel bernama table ![image](https://user-images.githubusercontent.com/91455522/180911748-be7f68c0-593a-4f41-b0ed-8b284c27897b.png)

**Langkah kedelapan**
> membuat seeder, script seperti dibawah ini ``` php artisan make:seeder barangTableSeeder ```

**Langkah kesembilan**
> ![image](https://user-images.githubusercontent.com/91455522/180912764-6bac166a-401d-4236-b826-ba4d2f224d7e.png) ubah isi seeder **barangTableSeeder** seperti pada gambar diatas. Lalu panggil seeder di databaseseeder untuk script nya seperti dibawah ini. ![image](https://user-images.githubusercontent.com/91455522/180912944-b74b4112-de52-42bf-89b4-479805224817.png). ``` php artisan db:seed ```


**Langkah terakhir**
> hasil dari lagnkah 1 - 9 adalah seperti digambar ini. ![image](https://user-images.githubusercontent.com/91455522/180913534-facc5660-0034-4625-aeb1-fd437d0ddb88.png)
