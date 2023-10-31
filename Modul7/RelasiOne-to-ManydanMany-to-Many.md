## Pembuatan Tabel
1. Memastikan sudah ada database dengan nama `lumenpost`.
![1](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/41f8c046-72e1-4e1e-871b-5f792a7d66f2)

2. Mengubah konfigurasi database pada file `.env`.
![2](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/7e1ad400-1ee4-4a81-9fd6-441e431cfd59)

3. Menghidupkan library dengan melakukan uncomment sintak pada file `app.php`.
![3](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e9e0cc22-7f9a-45c4-bdb4-bca8545c40ba)

4. Menjalankan perintah dibawah pada command line untuk membuat file migration.
![4](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e9667e85-e694-4932-a8a3-f85a8a6a0358)

5. Merubah fungsi `up()` pada file `migrasi create_posts_table`.
![5](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/7d6c886f-17a1-4954-871e-15d7e9852ad4)

6. Merubah fungsi `up()` pada file `create_comments_table`.
![6](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/8e1b18ee-1354-4bfe-b50a-b56a0da6af86)

7. Merubah fungsi `up()` pada file `create_tags_table`.
![7](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/986b8d72-f089-4ddb-aab8-2baf64ff1d7e)

8. Merubah fungsi `up()` pada file `create_post_tag_table`.
![8](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/fd0e3490-284b-440c-a2cf-98ae6d6c3708)

9. Menjalankan command `php artisan migrate`.
![9](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/11aedc6e-907d-4fb2-b197-ddb1a4671422)

## Pembuatan Model
1. Membuat file dengan nama `Post.php` dan isi dengan sintak berikut.
![10](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/44e42d5f-aef6-4acc-acb0-9932fd46b7f2)

2. Membuat file dengan nama `Comment.php` dan isi dengan sintak berikut.
![11](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/93de7a8e-2d76-409a-a690-502ec384191e)

3. Membuat file dengan nama `Tag.php` dan isi dengan sintak berikut.
![12](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/41b5f22b-70b0-4df6-ac98-584d44074d5d)

## Relasi One-to-Many
1. Menambahkan fungsi `comments()` pada file `Post.php`.
![13](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/9c535a0d-d88d-4efb-8bad-fa682e1a26a2)

2. Menambahkan fungsi `post()` dan atribut postId pada `$fillable` pada file `Comment.php`.
![14](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/5a71ea2c-2d33-4133-8b48-ae821e17a98b)

3. Membuat file dengan nama `PostController.php` dan isi dengan sintak berikut.
![15](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/50a189a6-1649-4c3b-b720-6d21c24becca)

4. Membuat file dengan nama `CommentController.php` dan isi dengan sintak berikut.
![16](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/38709512-d3af-4472-8f2a-b405aeaf2a65)

5. Menambahkan sintak dibawah pada `routes/web.php`.
![17](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/f36ad961-3a63-4d0f-bedf-7ffe7d640008)

6. Membuat satu post menggunakan postman.
![18](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/f8dc1b73-9a36-4ecb-b68a-d10909137964)

7. Membuat satu comment menggunakan postman.
![19](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/cf767fd5-6e53-454d-851b-7adfa1947bed)

8. Menampilkan post menggunakan postman.
![20](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/1a1199cb-a327-43f6-a2d8-358966c63c2c)

## Relasi Many-to-Many
1. Menambahkan fungsi `tags()` pada file `Post.php`.
![21](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/1ac31183-31ac-4cb5-9ae8-323bd95ef1d8)

2. Menambahkan fungsi `posts()` pada file `Tag.php`.
![22](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/dcde33d8-5687-4e82-9a7f-093da1d69b01)

3. Membuat file dengan nama `TagController.php` dan isi dengan sintak berikut.
![23](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/5161d0aa-3f46-4eeb-89f2-59ba7b984629)

4. menambahkan fungsi `addTag` dan response `tags` pada `PostController.php`.
![24](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/feb149cc-80b0-4cd7-8d13-c1019424f56f)

5. Menambahkan sintak dibawah pada `routes/web.php`.
![25](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e372c02f-9d67-441a-a547-50a6f39ea8c5)

6. Membuat satu tag menggunakan postman.
![26](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/f3d9c3bc-f14a-4d72-b348-797d8a264a09)

7. Menambahkan tag `jadul` pada post `disana engkau berdua`.
![27](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/2b03ad3e-1953-458f-9efe-2516d609f1a9)

8. Menampilkan post `disana engkau berdua` menggunakan Postman.
![28](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/22dd65b5-c180-4ebc-a7ac-a5a914e651da)

9. Membuat postingan `tanpamu apa artinya` menggunakan postman.
![29](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/666d43fd-256b-4be6-bf1a-bbcc5f358045)

10. Menambahkan tag `jadul` pada postingan `tanpamu apa aritnya`.
![30](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/cc4b6e55-3ad1-45b2-9311-8fe930acf7b2)

11. Membuat tag `lagu` menggunakan postman.
![31](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/82c4f599-fcb1-415e-bdb8-fe91551b961a)

12. Menambahkan tag `lagu` pada postingan `tanpamu apa artinya`.
![32](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/14ccdd86-364e-4338-bec0-31a6522b7af7)

13. Menampilkan post pertama.
![33](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/e0715a8d-9db4-4202-99b6-77d1f86a7146)

14. Menampilkan post kedua.
![34](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/74c4a2e2-d00f-4a7a-aa09-2fb7438bf960)
