# JSON Web Token (JWT)

## Penyesuaian Database
1. Merubah kolom token pada file migrasi `AddColumnTokenUsers`.
![1](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/2e967e05-a67f-4634-a881-5679047e11f7)

2. Menjalankan pereintah `php artisan migrate:fresh` untuk memperbarui data yang lama.
![2](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/f5140183-232b-4231-9029-5198e3ce6e2a)

3. Menjalankan endpoint `/auth/register` menggunakan postman seperti dibawah ini.
![3](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/f6291897-d50e-415c-9667-e3ca9aef4309)

## JWT Manual
1. Menambahkan 3 fungsi pada file `AuthController.php`.
![4](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/35719865-1c45-4a9f-9cec-3cb2b0db5815)

2. Merubah fungsi login.
![5](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/d716598c-37f2-4779-ab65-6b1d3163f7f7)

3. Menambahkan 4 fungsi pada file `Middleware/Authorization.php`.
![6](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/7128f011-7908-43ac-9581-ab4dd777eeb5)

4. Melakukan perubahan pada fungsi `handle` pada file `Authorization.php`.
![7](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/b1f74921-d250-4b25-910a-16c320dfdc0b)

5. Menjalankan endpoint `/auth/login` menggunakan postman serta menyalin token yang didapat setelah menjalankan endpoint tersebut.
![8](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/aa75aa2d-0a74-4d69-93eb-30630137b1de)

6. Menjalankan endpoint `/home` serta memasukkan token yang telah didapat dari langkah sebelumnya.
![9](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/7ee35dfd-7378-49a4-8d96-b09c31bccd30)

## JWT Library
1. Melakukan akses terhadap website `https://djecrety.ir/` dan generate jwt key secara online.
![10](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/1fb5b971-b25d-4aa6-a73b-705368449fb0)

2. Setelah mendapatkan key yang sudah di generate lakukan perubahan pada file `.env` dengan membuat variabel baru dengan nama `JWT_SECRET` dan isi value nya dengan jwt key yang sudah di generate pada langkah sebelumnya.
![11](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/fae4aeaf-3187-47f8-92ee-c72fa9ce11d0)

3. Melakukan instalasi package jwt firebase dengan menjalankan perintah `composer require firebase/php-jwt`.
![12](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/db45c742-8b9d-4fe7-a1b9-2643da6ab4f8)

4. Menambahkan fungsi dibawah ini pada file `AuthController.php`.
![13 1](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/376bf975-6632-4bd7-9136-c59b7f2443e5)

5. Merubah fungsi `login` pada file `AuthController.php`.
![13](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/02c4dae5-6e23-433e-8b40-fab101ef7bb1)

6. Membuat `JwtMiddleware.php` dan isi file tersebut dengan sintaks dibawah ini.
![14](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/c60a2a2b-816b-404f-9b7e-b36f3076a4e3)

7. Menambahkan middleware yang dibuat pada langkah sebelumnya pada `bootstrap/app.php`.
![15](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/12a70cc2-8428-43b0-b712-a734f9d8d3ee)

8. Menambahkan route baru pada `web.php`.
![16](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/6e9ae605-d4de-405a-8dd0-a7d4881effee)

9. Menjalankan endpoint `/auth/login` dengan menggunakan postman dan menyalin token yang didapat setalah menjalankan endpoint tersebut.
![17](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/8542b943-cde9-4980-8b14-72608059dd40)

10. Menjalankan endpoint `/home` serta memasukkan token yang didapat dari langkah sebelumnya.
