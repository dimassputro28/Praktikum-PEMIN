## Integrasi MongoDB dan Express

## Percobaan Instalasi NodeJS
1. Download dan jalankan node setup setelah itu jalankan command `node -v` untuk memeriksa apakah NodeJS sudah terinstall
![Cuplikan layar 2023-09-18 222630](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/3a768f89-b1c7-43d2-8fd4-ff007ac5f157)

## Inisiasi Project Express dan Pemasangan Package
1. Lakukan pembuatan folder dengan nama express-mongodb dan masuk ke dalam folder tersebut lalu buka melalui text editor masing-masing
![Cuplikan layar 2023-09-20 125721](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/f771feef-f813-40ed-91ff-48b12b3a0385)

2. Lakukan npm init untuk mengenerate file package.json dengan menggunakan command `npm init -y`
![Cuplikan layar 2023-09-20 125830](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/515e7e75-f411-4dae-9eae-e8467121dee3)

3. Lakukan instalasi express, mongoose, dan dotenv dengan menggunakan command `npm i express mongoose dotenv`
![Cuplikan layar 2023-09-20 125940](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/3b71ef4b-1523-4d5c-8d46-7108ffb19522)

## Koneksi Express ke MongoDB
1. Buatlah file index.js pada root folder dan masukkan kode di bawah ini
![Cuplikan layar 2023-09-20 130047](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/b902c844-a675-473f-83a8-8199e8bf3834)
![Cuplikan layar 2023-09-20 130128](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/fd26a6a6-9259-43cd-af6d-a0311ca83d7f)
Setelah itu coba jalankan aplikasi dengan command `node index.js`
![Cuplikan layar 2023-09-20 130253](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/718613a1-4235-47bd-b630-cbaf19f19280)

2. Lakukan pembuatan file .env dan masukkan baris berikut
![Cuplikan layar 2023-09-20 130415](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/20559425-e11c-43fd-8ac9-b5c4fd8ef115)
Setelah itu ubahlah kode pada listening port menjadi berikut dan coba jalankan aplikasi kembali
![Cuplikan layar 2023-09-20 130435](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/d479bc74-2f8b-49af-ae7c-0cfca21b438e)

3. Copy connection string yang terdapat pada compas atau atlas dan paste kan pada .env seperti berikut
![Cuplikan layar 2023-09-20 130625](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/11b35466-5c50-4956-9412-2d49355fef98)

4. Tambahkan baris kode berikut pada file index.js
![Cuplikan layar 2023-09-20 130848](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/da686013-7025-4e9d-8484-cebc89083a2e)
Setelah itu coba jalankan aplikasi kembali
![Cuplikan layar 2023-09-20 132616](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/3052d467-fcb8-42c2-87f7-404077dc0ae3)

## Pembuatan Routing
1. Lakukan pembuatan direktori routes di tingkat yang sama dengan index.js
![Cuplikan layar 2023-09-20 132758](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/f04a788f-cba7-4265-895a-8275f69b4607)

2. Buatlah file book.route.js di dalamnya
![Cuplikan layar 2023-09-20 132830](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/521316f9-850b-408b-b744-ab78fbaba1f4)

3. Tambahkan baris kode berikut untuk fungsi getAllBooks
![Cuplikan layar 2023-09-20 132910](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/8fabb3b2-6e5b-47e1-a5d6-12cf7c3eb025)

4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan deleteBook
![Cuplikan layar 2023-09-20 133039](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/b38b9ea7-9ca2-47de-9a15-08a76cf3c1af)

5. Lakukan import book.route.js pada file index.js dan tambahkan baris kode berikut
![Cuplikan layar 2023-09-20 133244](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/c204ebed-a1ab-4ba8-91b4-b63c4be1c5b0)

6. Uji salah satu endpoint dengan Postman
![Cuplikan layar 2023-09-20 134107](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/bad2a0f9-92b8-490d-9c6a-c64c6e8c2411)

## Pembuatan Controller

1. Lakukan pembuatan direktori controllers di tingkat yang sama dengan index.js dan buatlah file book.controller.js di dalamnya
![Cuplikan layar 2023-09-20 134201](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/5094973b-532c-4e85-9a26-870a1c1889b8)

2. Salin baris kode dari routes untuk fungsi getAllBooks
![Cuplikan layar 2023-09-20 134233](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/5a956c6d-ead8-4018-99b8-865e6dcb8de6)

3. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan deleteBook
![Cuplikan layar 2023-09-20 134410](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/fcc674a7-9915-43de-b90a-52ae88b87da6)

4. Lakukan import book.controller.js pada file book.route.js
![Cuplikan layar 2023-09-20 134529](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/4738fc66-5604-413e-9fbf-d0172c1e964b)

5. Lakukan perubahan pada fungsi agar dapat memanggil fungsi dari book.controller.js
![Cuplikan layar 2023-09-20 134810](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/a50baf83-e695-4b8b-9374-754f4ef2c3f3)

6. Lakukan pengujian kembali, pastikan response tetap sama
![Cuplikan layar 2023-09-20 134909](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/f2df3498-0662-44ed-ab26-5d38cc32646f)

## Pembuatan Model
1. Lakukan pembuatan direktori models di tingkat yang sama dengan index.js dan buatlah file book.model.js di dalamnya
![Cuplikan layar 2023-09-20 135001](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/601e679a-7922-479c-96cc-930f53282a5c)

2. Tambahkan baris kode berikut sesuai dengan tabel di atas
![Cuplikan layar 2023-09-20 135036](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/8c0e6437-67ea-4b55-8d22-6250b69019cd)

## Operasi CRUD
1. Hapus semua data pada collection books
![Cuplikan layar 2023-09-20 135205](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/98dd08ad-d172-4e68-b808-515b9b6e0b5f)

2. Lakukan import book.model.js pada file book.controller.js
![Cuplikan layar 2023-09-20 135406](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/97da792f-5f98-4a9b-a9b2-f4bd8db7c18f)

3. Lakukan perubahan pada fungsi createBook
![Cuplikan layar 2023-09-20 135601](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/858831c1-81c7-485c-9b95-ad8ef0f656ca)

4. Buatlah dua buah buku dengan data di bawah ini dengan Postman
![Cuplikan layar 2023-09-20 135955](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/9a27ad53-f9b8-4a0d-9318-86d01f653a0a)
![Cuplikan layar 2023-09-20 140044](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/814772e8-9b80-4927-ba1f-d919c3c7b1df)

5. Lakukan perubahan pada fungsi getAllBooks
![Cuplikan layar 2023-09-20 140202](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/54febfc2-4885-45ed-8e02-f08ee3cf8542)

6. Lakukan perubahan pada fungsi getOneBook
![Cuplikan layar 2023-09-20 140251](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/7764f472-76e2-4f06-a74a-5d63181ab538)

7. Tampilkan semua buku dengan Postman
![Cuplikan layar 2023-09-20 140408](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/9d722398-ce03-4bd0-80d4-21eaa57eb91d)

8. Tampilkan buku Dilan 1990 dengan Postman
![Cuplikan layar 2023-09-20 140626](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/13b348b6-4d8c-4553-80dc-49bf49148199)

9. Lakukan perubahan pada fungsi updateBook
![Cuplikan layar 2023-09-20 140719](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/0bcebac7-a0d5-4785-b807-2f9f4927d3f9)

10. Ubah judul buku Dilan 1991 menjadi “<NAMA PANGGILAN> 1991” dengan Postman
![Cuplikan layar 2023-09-20 140923](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/688edbce-f036-460f-920a-f262c7e75bb4)

11. Lakukan perubahan pada fungsi deleteBook
![Cuplikan layar 2023-09-20 141007](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/29c61bfb-2889-42ec-898c-c17cb44c78fa)

12. Hapus buku Dilan 1990 dengan Postman
![Cuplikan layar 2023-09-20 141123](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/ead046f5-fd56-4348-b0ab-d33f9690395a)
