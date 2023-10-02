## Basic Routing dan Migration

## Langkah Percobaan

1. Untuk menambahkan endpoint dengan method GET pada aplikasi kita, kita dapat mengunjungi file web.php pada folder routes. Kemudian tambahkan baris ini pada akhir file
![Cuplikan layar 2023-09-26 231833](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e5b666bd-ac7f-40ac-9183-925e3e6363b8)

Setelah itu coba jalankan aplikasi dengan command, 'php -S localhost:8000 -t public'
![Cuplikan layar 2023-09-26 232024](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/1263ddc6-9981-492e-ab83-1c32e6f1596d)

2. POST, PUT, PATCH, DELETE, dan OPTIONS
Sama halnya saat menambahkan method GET, kita dapat menambahkan methode POST, PUT, PATCH, DELETE, dan OPTIONS pada file web.php dengan code seperti ini,
![Cuplikan layar 2023-09-26 232141](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/d708553b-d2d2-4960-87a8-3bf43ee3b6ba)

   - Kita dapat menginstall ekstensi dengan membuka panel extensions lalu mencari thunder client, Setelah menginstall Thunder Client, kita akan melihat logo seperti petir pada activity bar kita (sebelah kiri). Kita dapat membuat request dengan menekan "New Request" pada ekstensi
     ![Cuplikan layar 2023-09-27 091336](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/84e3abd1-15fb-47f6-8978-f43aa11d78c4)

   - Akses url yang baru saja ditambahkan pada aplikasi dengan methodnya
       ![Cuplikan layar 2023-09-27 131334](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/4c4a62ee-31c9-4acb-b9e9-c13ca9f8e1df)

4. Migrasi Database
   a. Sebelum melakukan migrasi database pastikan server database aktif kemudian pastikan sudah membuat database dengan nama 'lumenapi', Kemudian ubah konfigurasi database pada file .env menjadi seperti ini
   ![Cuplikan layar 2023-09-27 131817](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/dd56a052-6951-4119-ba0b-06629828be38)

   b. Setelah mengubah konfigurasi pada file .env, kita juga perlu menghidupkan beberapa library bawaan dari lumen dengan membuka file app.php pada folder bootstrap dan mengubah baris ini,
   ![Cuplikan layar 2023-09-27 131901](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/50f4f03e-23ae-4508-bbcf-f04e4e0151a3)

   c. Setelah itu jalankan command berikut untuk membuat file migration,
   ![Cuplikan layar 2023-09-27 132017](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/b9b51bd9-a0f7-49b0-8c20-27bba309ba6c)

   d. Ubah fungsi up pada file migrasi 'create_users_table'
   ![Cuplikan layar 2023-09-27 132138](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/18652753-900d-463a-8bdb-f0c2602035f5)

   e. Ubah fungsi up pada file migrasi 'create_products_table'
   ![Cuplikan layar 2023-09-27 132228](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/6c1df384-bbee-4b78-856e-3c5b33c7719a)

   f. Kemudian jalankan command, 'php artisan migrate'
   ![Cuplikan layar 2023-09-27 134125](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/94647dd2-4fd0-4051-bf70-04bd7f99f150)




   
   

      
