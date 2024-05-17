## Refleksi tutorial 11

![alt text](before-service.png)
![alt text](after-service.png)

1. Dari kedua gambar di atas. Ketika kita belum mengekspos service, log tidak akan ditampilkan karena tidak ada browser yang dibuka. Sedangkan, saat kita mengeskpos service, service akan melakukan request GET dan nantinya request tersebut dapat dilihat di dalam log kita.

2. Dengan adanya -n (Namespace) kita bisa mengspesifikasikan pada namespace yang ingin kita lihat perintah GET. Tujuan dari penggunaannya -n adalah untuk mengatasi kondisi dimana kita memiliki banyak service yang berbeda yang memiliki nama yang sama dan tersebar di berbagai namespace yang berbeda.
