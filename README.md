## 1.2. Understanding how it works

![understanding how it works](image.png) <br>
Berdasarkan lampiran diatas, terlihat bahwa pertama-tama output akan menampilkan "Rafli's Komputer: hey hey!" terlebih dahulu sebelum menampilkan perintah-perintah yang berada pada task di dalam spawner. Ini terjadi, karena baris tersebut dieksekusi sebelum line `drop(spawner)` dan `executor.run()` yang berarti pesan ini dicetak sebelum task yang di spawn mulai dijalankan oleh executor. Ketika executor dijalankan, task yang telah di spawn sebelumnya baru akhirnya mulai bekerja. Lalu output mulai menampilkan "Rafli's Komputer: howdy!" dan setelah 2 detik kemudian menampilkan "Rafli's Komputer: done!". Jadi, kesimpulannya "Rafli's Komputer: hey hey!" akan tercetak duluan karena dieksekusi langsung di thread utama sebelum executor memulai task asinkron yang di *spawn*.