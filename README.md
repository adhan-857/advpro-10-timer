# Tutorial Modul 10:  Asynchoronous Programming
### Ramadhan Andika Putra (2206081976) - AdPro A <br>

**1.2. Understanding how it works**<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/fe17773e-b053-4668-9f3b-0588455257d5)<br>
Pada gambar, terlihat bahwa *output* "hey hey" di-*print* terlebih dahulu. Hal ini dikarenakan output "howdy" dan "done" berada di dalam *asynchronus function*. Di mana fungsi asinkronus berjalan di luar fungsi `main` yang menjalankannya. Oleh karea itu, "hey hey" akan di-*print* terlebih dahulu karena fungsi `main` akan terus menjalankan programnya. Sementara itu, fungsi asinkronus masih menuggu hasil dari `future`.