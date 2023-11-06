1. Pastikan terdapat tabel users yang dibuat menggunakan migration pada bab Basic Routing dan Migration.
   Berikut informasi kolom yang harus ada
![1](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/11dcb444-5b67-460e-8fa6-9b979554b22d)

2. Pastikan terdapat model User.php yang digunakan pada bab 󾠲 Model, Controller dan Request-Response Handler.
   Berikut baris kode yang harus ada
![2](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/71b113a3-3a2f-44f5-a14b-5fe8dac86d10)

3. Buatlah file AuthController.php dan isilah dengan baris kode berikut
![3](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/c5b5f83d-f306-4442-a80c-65e68a56150e)

4. Menambahkan group route pada `routes/web.php`.
![4](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/81c30bb4-3dc1-4636-9191-f8c27a76fcd1)

5. Jalankan aplikasi pada endpoint /auth/register dengan body berikut
   ![5](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/a70ee32d-5e30-43b9-9e78-f3cd879cc12e)

## Authentication
1. Buatlah fungsi login(Request $request) pada file AuthController.php
![6](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/246f45be-dcd9-43ad-b9e2-384ef6bdb680)

2. Menambahkan route pada file `web.php`.
![auth2](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/a26f09de-19b4-4ddc-b9e4-f02530096f76)

3. Menjalankan aplikasi pada endpoint `/auth/login` dengan ini body seperti dibawah ini menggunakan postman.
![10](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/8bdb11ee-a276-432f-b865-5c0f60decced)

## Token
1. Menjalankan perintah dibawhah ini untuk membuat migrasi baru.
![token1](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/62c7292a-7ca4-4bd2-92c1-3a7d98bb1841)

2. Menambahkan sintaks dibawah ini pada file migration yang dibuat pada langkah sebelumnya.
![token2](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/5f19f0d7-0f10-43c9-b44d-295412c75b5e)

3. Menambahkan atribut token di `$fillable` pada `User.php`.
![7](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/ec82ab47-79d7-41d1-b423-017b2ef4d2e3)

4. Menambahkan baris berikut pada file `AuthController.php`.
![8](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/31b78f59-8b1c-4c6f-a910-48321e6e1808)

5. Menjalankan perintah dibawah ini untuk menjalankan migrasi terbaru.
![9](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/4e71ea8d-c129-4928-8463-aea0b26feab6)

6. Menjalankan aplikasi pada endpoint `/auth/login` dengan ini body seperti dibawah ini menggunakan postman, dan salin token yang didapat ke notepad.
![10](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/95a63a8a-a2aa-407b-9d46-47b934d0cc3a)

## Authorization
1. Membuat file `Authorization.php` pada folder `App/Http/Middleware` dan isi dengan sintaks dibawah ini.
![11](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/02a52871-c296-4d4f-9355-604d4501f226)

2. Menambahkan middleware yang baru dibuat pada `bootstrap/app.php.`.
![12](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/afd28226-9b5a-465e-a213-93b3cbed344a)

3. Membuat fungsi `home()` pada `HomeController.php`.
![13](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/8dfdf523-ee50-4bc7-a85c-5df51b2af3a1)

4. Menambahkan route pada file `web.php`.
![14](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/843a2af8-6ebe-4047-a6bc-0b74b5c458ba)

5. Menjalankan alikasi pada endpoint `/home` dengan memasukkan nilai token yang telah didapat sebelumnya.
![15](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e10a2bdd-0f9b-4bb4-baca-c8eecf98d2e4)
