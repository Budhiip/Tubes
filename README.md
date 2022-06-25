# Pemrograman Intergratif-22
**Budhi Priambodo  1202190065 || IT 02-01** 

<br />

-----

### Tahap 1 
### INSTALL COMPOSER

•	Downlaod Composer https://getcomposer.org/download/

   ![image](https://user-images.githubusercontent.com/83237598/173079242-fe7b1417-8b7f-4974-9fb5-bae272d419b9.png)

•	Install file composer seperti biasa. Jika sudah buka terminal dan ketik “composer”, maka akan muncul tampilan seperti digambar, yang mana composer sudah terinstall.

  ![](Assets/008.png)

### INSTALL LARAVEL VIA COMPOSER 

•	Buka website https://laravel.com/docs/9.x#installation-via-composer, untuk menyalin command installasi laravel via composer

•	Buat folder baru di komputer untuk menginstall laravel (bebas lokasinya). Klik kanan dan buka dengan Git Bash Here

   ![image](https://user-images.githubusercontent.com/83237598/173079292-86228a98-5018-4aa8-8c48-0ab4c8e335c6.png)
 
 •	Buat project untuk install laravel dengan command
 
```
 composer create-project laravel/laravel nama_project
```
•	Masuk  terlebih dahulu ke folder project yang sudah dibuat dengan command
```
cd aggregrate/
```
• Kemudian buka file installasi laravel dengan text editor (disini dengan visual studio code) dengan command 
```
code ./aggregrate
```

• Maka akan secara otomatis membuka aplikasi visual studio code
•	Klik menu terminal pada bagian atas, pilih terminal baru, lalu masukkan command
```
php artisan serve
```
  ![Screenshot (141)](https://user-images.githubusercontent.com/61863147/175769877-05cabf1e-e2e3-4c7f-90b2-e07b2e32e35a.png)

•	Copy server laravel, untuk dibuka di browser

 ![Screenshot (117)](https://user-images.githubusercontent.com/61863147/175769820-93b5a568-9e43-479b-9ec1-57e223dc4f82.png)  



<br />

-----
### Tahap 2
•	Ubah DB_DATABASE di .env sesuai dengan nama database yang dibuat di phpmyadmin

![Screenshot (119)](https://user-images.githubusercontent.com/61863147/175769899-97ef4455-448f-454c-bf09-8b767c83bc25.png)

![Screenshot (120)](https://user-images.githubusercontent.com/61863147/175769914-5887ff49-d3e9-4172-a06e-b9552fd3a5d8.png)

• Buat 2 table rss dan news dengan fitur migrations menggunakan perintah
  ```
  php artisan make:migration create_rss_table
  
  php artisan make:migration create_news_table
  ```
• Tambahkan kolom name dan url pada tabel rss, seperti pada gambar dibawah
  ![Screenshot (122)](https://user-images.githubusercontent.com/61863147/175769940-4167e367-7059-4e96-a28e-904c113f5128.png)


• Tambahkan kolom title, img_url, description, source_url,  dan rss_id pada tabel news, seperti pada gambar dibawah
  ![Screenshot (121)](https://user-images.githubusercontent.com/61863147/175769952-8003a745-2631-4e58-bf20-589b88bdb0fa.png)


• Untuk menjalankan migrasi yang dibuat jalankan perintah diterminal seperti dibawah, lalu cek database
  ```
  php artisan migrate
  ```
  ![Screenshot (123)](https://user-images.githubusercontent.com/61863147/175769980-d53ddb13-a259-4c09-a243-ad1d4140a076.png)


• Buat koneksi  model  ke database  dengan membuat seeder dan controller untuk tabel Rss dan News, dengan perintah
  ```
  php artisan make:model Rss –-seed -–controller
  ```
  
  ![Screenshot (125)](https://user-images.githubusercontent.com/61863147/175770042-b8583d3e-a9c2-41a9-aa51-f7b15d19bee8.png)


• Edit file Rss.php, RssSeeder.php serta DatabaseSeeder.php seperti pada gambar dibawah
  ![Screenshot (125)](https://user-images.githubusercontent.com/61863147/175770134-8f66225e-8c17-4d3c-86e9-dac3a5b69e05.png)
  ![Screenshot (127)](https://user-images.githubusercontent.com/61863147/175770137-2eabb3ae-0bac-40a9-a03f-b06d8ddb58d8.png)   
  ![Screenshot (128)](https://user-images.githubusercontent.com/61863147/175770138-eab1bea6-c27c-41ba-9dc0-396f15bbab81.png)

  
• Kemudian cek koneksi dengan perintah
  ```
  php artisan db:seed
  ```
  ![Screenshot (133)](https://user-images.githubusercontent.com/61863147/175770168-67a785a7-e350-4e9a-8111-52e042cc4887.png)


• Edit file News.php, NewsController.php, web.php, serta file migration News seperti pada gambar dibawah
  ![Screenshot (129)](https://user-images.githubusercontent.com/61863147/175770187-946cee82-1cf7-4d81-98ea-edae3c377398.png)
  ![Screenshot (137)](https://user-images.githubusercontent.com/61863147/175770219-d8ebdd9e-3c44-4211-bf5f-1855b4a8f43f.png)
  ![Screenshot (145)](https://user-images.githubusercontent.com/61863147/175770272-81e705c6-54f4-414d-85ff-2ff514b322d4.png)
  ![Screenshot (138)](https://user-images.githubusercontent.com/61863147/175770296-e1c4724c-71fd-4da5-87be-ec286f7c67d0.png)
  

• Cek localhost di http://127.0.0.1:8000/aggregrate/1 dan di database phpmyadmin
![Screenshot (139)](https://user-images.githubusercontent.com/61863147/175770311-f66ff5d9-c441-4879-85b3-f9f9b75ab482.png)
![Screenshot (140)](https://user-images.githubusercontent.com/61863147/175770316-91437143-d231-4b77-ae7a-1595d6acd969.png)
