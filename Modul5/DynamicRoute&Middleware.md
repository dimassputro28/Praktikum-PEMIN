## Dynamic Route & Middleware

## Langkah Percobaan

1. Dynamic route adalah route yang dapat berubah-ubah, contohnya pada saat kita membuka suatu halaman web, kadang kita melihat '/users/1' atau '/users/2' , hal ini yang dinamakan dynamic routes. Untuk menambahkan dynamic routes pada aplikasi lumen kita, kita dapat menggunakan
syntax berikut,

![1](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/048efbab-1010-47f4-b3d4-19ce8a953c56)

![1 1](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/baab2d70-6ab0-44a0-b082-6ec7bcad3c2b)

Saat menambahkan parameter pada routes, kita tidak terbatas pada 1 variable saja, namun kita dapat menambahkan sebanyak yang diperlukan seperti kode berikut,

![Cuplikan layar 2023-10-09 210824](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/0ce5cdfe-a137-4ffb-9c54-48473aa668e2)

![Cuplikan layar 2023-10-09 210918](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e00a615e-0e60-4969-8e06-083985eb7f4e)

Pada dynamic routes kita juga bisa menambahkan optional routes, yang mana optional routes tidak mengharuskan kita untuk memberi variable pada endpoint kita, namun saat kita memanggil endpoint, dapat menggunakan parameter variable ataupun tidak, seperti pada kode dibawah ini,

![Cuplikan layar 2023-10-09 211001](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/d4277d76-ac4d-465c-8248-951e5ceb8496)

![Cuplikan layar 2023-10-09 211038](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/38302491-20d5-4583-b4a1-44f8016670ed)


2. Aliases Route
Aliases Route digunakan untuk memberi nama pada route yang telah kita buat, hal ini dapat membantu kita, saat kita ingin memanggil route tersebut pada aplikasi kita. Berikut syntax untuk menambahkan aliases route
![Cuplikan layar 2023-10-09 211140](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/a1d2c949-ebfd-40f9-8b8c-d0b32ab5eb04)

![Cuplikan layar 2023-10-09 211216](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/97cba24e-2486-4e1b-a10e-665e31a3c461)


4. Group Route
  Pada lumen, kita juga dapat memberikan grouping pada routes kita agar lebih mudah pada saat penulisan route pada web.php kita. Kita dapat melakukan grouping dengan
menggunakan syntax berikut,
![Cuplikan layar 2023-10-09 211317](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/96462aee-0a59-4fa2-9e78-0fed1b55ea9d)

5. Middleware
   Middleware adalah penengah antara komunikasi aplikasi dan client. Middleware biasanya digunakan untuk membatasi siapa yang dapat berinteraksi dengan aplikasi kita dan semacamnya, kita dapat menambahkan middleware dengan menambahkan file pada folder 'app/Http/Middleware' . Pada folder tersebut terdapat file ExampleMiddleware , kita dapat men-copy file tersebut untuk membuat middleware baru. Pada praktikum kali ini akan dibuat middleware Age dengan isi,
   
![Cuplikan layar 2023-10-09 211355](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/91b02b7a-a7c8-4169-bb6d-df45abb4baf6)

Kemudian, setelah menambahkan filter pada 'AgeMiddleware' , kita harus mendaftarkan 'AgeMiddleware' pada aplikasi kita, pada file 'bootstrap/app.php' seperti berikut ini,
![Cuplikan layar 2023-10-09 211442](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/b494fc16-de4a-4e59-90a9-46c66f54ee20)

Pada baris 65 terdapat comment mengenai proses mendaftarkan suatu middleware dalam aplikasi kita. Untuk menambahkan middleware pada aplikasi kita, kita dapat men- uncomment baris 75 hingga 77, kemudian menambahkan age middleware ke dalamnya. Namun, karena kita hanya ingin menambahkan middleware pada route tertentu, kita akan menghapus comment pada baris 79 hingga 81, kemudian menambahkan middleware age di dalamnya. Lalu, kita dapat menambahkan middleware pada routes kita dengan menambahkan opsi middleware pada salah satu route, contohnya,

![Cuplikan layar 2023-10-09 211634](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/1df526d5-fab6-482d-97f4-45a80a72fc1a)

hasil percobaan dibawah umur, 
![Cuplikan layar 2023-10-10 140520](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/8b66685a-7764-454f-ab50-e389c3797277)

hasil percobaan diatas 17 tahun, 
![Cuplikan layar 2023-10-10 140558](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e2220b21-cede-4cef-b466-b8d0269a92d1)


