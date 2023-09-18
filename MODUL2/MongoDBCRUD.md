1. Lakukan koneksi ke MongoDB menggunakan connection string
![1](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/249bd6d7-b6fa-4445-a5ca-a19c0b23930d)
2. Buat database dengan melakukan klik “Create Database”
![Cuplikan layar 2023-09-18 222300](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e68e4c67-f6eb-468a-881f-55a186968ba5)

3. Lakukan insert buku pertama dengan melakukan klik “Add Data”, pilih “Insert Document”, isi dengan data yang diinginkan dan klik “Insert”
   
![Cuplikan layar 2023-09-18 222323](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/67de3862-d445-4a2b-b262-2e5e281b9a4e)


4. Lakukan insert buku kedua dengan cara yang sama.

![Cuplikan layar 2023-09-18 222357](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e07f0057-848a-45e6-a5a8-dc36f88573d3)


5. Lakukan pencarian buku dengan author “Osamu Dazai” dengan mengisi filter yang diinginkan dan klik “Find”
  
![Cuplikan layar 2023-09-18 222450](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/be0760e1-4bc4-4fd1-91b9-34bf13deeb34)


6. Lakukan perubahan summary pada buku “No Longer Human” menjadi “Buku yang
bagus (<NAMA>,<NIM>) dengan melakukan klik “Edit Document” (berlambang
pensil), mengisi nilai summary yang baru, dan melakukan klik “Update”

![Cuplikan layar 2023-09-18 222608](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/827b70f9-8aae-4c1a-b024-36ab4a87e0c1)


7. Lakukan penghapusan pada buku “I Am a Cat” dengan melakukan klik “Remove
Document” (berlambang tong sampah) dan melakukan klik “Delete”

![Cuplikan layar 2023-09-18 222630](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/33f17420-aef7-4c94-9c40-a5e53eae5c24)


## Menggunakan Mongo DB Shell

1. Lakukan koneksi ke MongoDB Server dengan menjalankan command mongosh bagi
yang menggunakan terminal build in OS sehingga tampilan terminal kalian akan
menjadi seperti berikut

![Cuplikan layar 2023-09-18 222651](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/2443d334-f4ef-42c7-bcdf-b6e582591d35)


2. Mencoba melihat list database yang ada di server dengan menjalankan command
`show dbs`

![Cuplikan layar 2023-09-18 222715](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/9b7d5219-acd1-4004-a00a-34ca4ccea871)


Untuk berpindah ke database “bookstore” gunakan command `use bookstore` , kalian
dapat memastikan telah berpindah ke database yang benar dengan melihat tulisan
sebelum tanda “>”

![Cuplikan layar 2023-09-18 222739](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/bb68b8bf-9f0f-4e10-93e4-9090a3f2bf70)


Cobalah untuk melihat collection yang ada pada database tersebut dengan
menggunakan command `show collections`

![Cuplikan layar 2023-09-18 223555](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/a542a83a-5d8c-4141-a204-d78ac22a1e7a)


3. Lakukan insert buku “Overlord I” dengan menggunakan command
`db.books.insertOne(<data kalian>)` , setelah insert buku berhasil maka MongoDB akan
mengembalikan pesan sebagai berikut.

![Cuplikan layar 2023-09-18 222814](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/c3f47078-9367-4666-8034-beef296dca72)


4. Lakukan insert buku “The Setting Sun” dan “Hujan” dengan insert many dengan
menggunakan command `db.books.insertMany(<data kalian>)` , dan akan mengembalikan pesan sebagai berikut.

![Cuplikan layar 2023-09-18 222839](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/35e3e8fa-b177-4229-b087-ad280f20113c)


5. Lakukan pencarian buku dengan menggunakan command `db.books.find()` untuk
melakukan pencarian semua buku.

![Cuplikan layar 2023-09-18 222903](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/755d6289-09db-48bb-87bf-2d89f3a508f6)


6. Tampilkan seluruh buku dengan author “Osamu Dazai” dengan mengisi argument
pada find() dengan menggunakan command `db.books.find({<filter yang ingin
diisi>})`

![Cuplikan layar 2023-09-18 222929](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/2a83257b-5ac3-4d80-b88c-9d94dd4709e0)

7. Lakukan perubahan summary pada buku “Hujan” menjadi “Buku yang bagus
(<NAMA>,<NIM>) dengan mengunakan `command db.books.updateOne({<filter>},
{$set: {<data yang akan di update>}})` sehingga output yang dihasilkan oleh MongoDB
akan menjadi seperti berikut


![Cuplikan layar 2023-09-18 222947](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/6b91284a-400f-4604-9249-c063a099abdb)


8. Lakukan perubahan publisher menjadi “Yen Press” pada semua buku “Osamu
Dazai” dengan menggunakan command `db.books.updateMany({<filter>}, {$set: {<data
yang akan di update>}})`


![Cuplikan layar 2023-09-18 223006](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/2b865c45-daef-4bf4-b20b-7167dcda56d5)


9. Lakukan penghapusan pada buku “Overlord I” dengan menggunakan command
`db.books.deleteOne({<argument>})`

![Cuplikan layar 2023-09-18 223026](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/3359c6e6-da64-4868-9037-469f4a7302b2)


10.Lakukan penghapusan pada semua buku “Osamu Dazai dengan menggunakan
command `db.books.deleteMany({<argument>})` 

![Cuplikan layar 2023-09-18 223042](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/dea1c240-6d76-47e4-97af-80e62b80c7db)

