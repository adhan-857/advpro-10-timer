# Tutorial Modul 10:  Asynchronous Programming
### Ramadhan Andika Putra (2206081976) - AdPro A <br>

**1.2. Understanding how it works**<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/fe17773e-b053-4668-9f3b-0588455257d5)<br>
Pada gambar, terlihat bahwa *output* "hey hey" di-*print* terlebih dahulu. Hal ini dikarenakan output "howdy!" dan "done!" berada di dalam *asynchronus function*. Di mana fungsi asinkronus berjalan di luar fungsi `main` yang menjalankannya. Oleh karea itu, "hey hey" akan di-*print* terlebih dahulu karena fungsi `main` akan terus menjalankan programnya. Sementara itu, fungsi asinkronus masih menuggu hasil dari `future`.
<br>
<br>

**1.3. Multiple Spawn and removing drop**
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/f1fa21e8-747c-4fe4-9435-f63466bf16d2)
Pada gambar, terlihat bahwa pada *output* yang dihasilkan jika terdapat banyak *spawner* menyebabkan lebih banyak *task* yang dilakukan karena lebih banyak *task* yang masuk antrian ke dalam *task sender* yang berlaku seperti sebuah *message queue*. Jika terdapat banyak spawn *calls*, maka akan terdapat banyak task yang akan dieksekusi secara asinkronus. Setiap *tasks* akan ditambahkan pada *executor* *queue* dan akan dieksekusi ketika *executor* mendapatkan kesempatan untuk menjalankannya. Ketika bagian `drop(spawner)` dihilangkan, *executor* akan tetap menunggu *task* lain untuk di-*spawn* walau semua task yang di-*spawn* telah selesai. Hal ini dikarenakan *executor* menggunakan *event* *dropping spawner* sebagai sinyal bahwa tidak ada lagi task yang akan di-*spawn*.