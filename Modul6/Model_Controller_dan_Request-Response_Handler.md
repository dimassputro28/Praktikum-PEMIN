# Model, Controller dan Request-Response Handler
### Model
1. Memastikan adanya table users pada aplikasi.
![1](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/b7ab0320-bada-4194-b49e-3046dfd868c9)

2. Mengganti isi dari file `User.php` pada path `app/Models`dengan menggunakan sintkas dibawah ini.
![2](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/0dcbc9a3-7e88-4b14-9b7c-9aa238f84422)

### Controller
1. Membuat salinan dari file `ExampleController.php` pada folder `app/Http/Controllers` dengan nama `HomeController.php` serta membuat function index dengan sintaks dibawah ini.
![3](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/113e53d5-f97e-40d8-939c-d02d70e477d7)

2. Mengubah route pada file `routes/web/php` seperti dibawwah ini.
![4](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/b58c0343-c016-419f-9e38-2d72d6b7b775)

3. Menjalakan aplikasi dengan memasukkan `localhost:8000` pada browser sehingga muncul tampilan seperti dibawah ini.
![5](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/99e98d15-7904-4bd7-8d16-c28d97983843)

### Request Handler
1. Melakukan import library request pada file `HomeController.php`.
![6](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/bcf4a1d4-6dfa-40bc-b379-cdb8a71580d8)

2. Merubaha `function index()` menjadi seperti dibawah ini.
![7](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/9000ec8f-bb2b-4b46-933e-ebd2de75b82e)

3. Menjalankan kembali aplikasi terssebut.
![8](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/1a95b08d-c3a4-4caa-8651-d8aeb0b3199c)

### Response Handler
1. Melakukan import library response pada file `HomeController.php`.
![9](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e6f88759-d295-4816-943d-81765b82961a)

2. Membuat `function hello()`.
![10](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/9bbd8504-66e3-4811-8457-3335636cf143)

3. Menambahkan route `/hello` pada file `routes/web.php`.
![11](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/59c53ff0-3ff1-467a-9566-23c0a3b15231)

4. Menjalankan aplikasi pada route /hello.
![12](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/0c64a4c5-a9d1-461b-861b-36c14e8d4530)

### Penerapan
1. Melakukan import model User dengan menambahkan sintaks berikut pada file `HomeController.php`.
![13](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/46a18bf5-38e5-4ddd-ae71-4dd67151c7e1)

2. Menambahkan `function defaultUser()`, `function createUseer()`, dan `function getUsers()`.
![14](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/75f992ae-d013-4496-b361-f4920d3a870a)

3. Menambahkan route untuk setiap function yang telah dibuat sebelumnya.
![15](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/d5bcfaca-7b71-4eb6-be36-946f4ec7890b)

4. Menjalankan aplikasi pada route `/users/default` menggunakan Postman.
![16](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e8df30e4-cd95-4850-93ac-71ffe30d9de6)

5. Menjalankan kembali aplikasi melalui Postman pada route `/users/new` dengan mengisi field body seperti dibawah ini.
![17](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/b6b5c2ca-72bc-4f83-a54e-2c9c8e436823)

6. Menjalankan aplikasi pada route `/users/all`.
![Cuplikan layar 2023-10-24 104729](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/5575bf91-c42d-45cc-8d1b-bbd69a76d0e5)
