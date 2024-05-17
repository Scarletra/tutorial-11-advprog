## Refleksi tutorial 11

![alt text](before-service.png)
![alt text](after-service.png)

1. Dari kedua gambar di atas. Ketika kita belum mengekspos service, log tidak akan ditampilkan karena tidak ada browser yang dibuka. Sedangkan, saat kita mengeskpos service, service akan melakukan request GET dan nantinya request tersebut dapat dilihat di dalam log kita.

2. Dengan adanya -n (Namespace) kita bisa mengspesifikasikan pada namespace yang ingin kita lihat perintah GET. Tujuan dari penggunaannya -n adalah untuk mengatasi kondisi dimana kita memiliki banyak service yang berbeda yang memiliki nama yang sama dan tersebar di berbagai namespace yang berbeda.

## Reflection on Rolling Update & Kubernetes Manifest File

1. Recreate deployment memerlukan waktu yang lebih lama karena (downtime) dalam melakukan pembaruan aplikasi karena proses deployment ini perlu menghapus aplikasi nya terlebih dahulu dan kemudian membuat aplikasi yang baru. Di sisi lain, rolling update deployment bekerja dengan cara mengubah aplikasi secara perlahan ke versi terbaru.

2. Pertama, app springboot-petclinic-rest yang sudah discale ke versi 3.0.2 akan direcreate 
![alt text](step1.png)


    Dengan memanfaatkan sifat dari repilcaset yang akan selalu menggantikan pod yang terhapus, maka akan digantikan versinya menjadi 3.2.1 dengan menjalankan perintah berikut
![alt text](step2.png)

    Kita dapat mengecek apakah perubahan tersebut berhasil atau tidaknya. Akan muncul window yang akan menampilkan secara detil.
![alt text](step3.png)

    Lalu kita coba delete pod yang sudah ada sebelumnya
![alt text](step4.png)

    Pod baru akan dibuat untuk menggantikan pod yang sudah dihapus sebelumnya
![alt text](step5.png)

    Kita run kembali service nya dan akan muncul seperti di bawah
![alt text](step6.png)
