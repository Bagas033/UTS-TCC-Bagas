# 1. Buat Akun di Dockerhub
~ Dalam membuat akun dockerhub dapat dilakukan secara online atau melalui  [Docker Hub](https://hub.docker.com/), jika dalam membuat akun dockerhub berhasil maka akan seperti gambar dibawah ini

![Halaman Akun Dockerhub](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/dockerhub_1.png)
> Halaman akun Dockerhub

# 2. Pull dan menjalankan image di komputer 
~langkah selanjutnya setelah membuatan akun DockerHub, dengan melakukan clone doodle image dan menjalankan pada komputer, maka selanutnya image yang akan dijalankan dapat dipilih, untuk yang saya jalankan yaitu birthday2019 dengan perintah `cd doodle/birthday2019` pada docker quikstart terminal.

![pindah direktori](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/soal_02_1.png)

~Setelah itu mengetikkan perintah `docker build -t bagas033/birthday2019` untuk melakukan install build birthday2019. brikut adalah gambar proses;

![build image](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/soal_02_2.png)

~berikutnya melakukan run build, yang dilakukan run images dengan measukkan perintah `docker run -t bagas033/birthdays2019`. jika berhasil akan seperti gambar dibawah ini;

![Hasil run](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/soal_02_3.png)
~kemudian menjalankan atau merubah image menjadi containerhal yang perlu dilakukan yaitu menghentikan container terlebih dahulu baru kemudian melakukan pada stop container yang berjalan, namun lakukan cek pada pengecekan dengan measukkan perintah `docker -ps a` lalu akan tampil container yang sedang berjalan;

![container berjalan](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/soal_02_4.png)
Untuk menghentikan container hal yang perlu dilakukan yaitu dengan menggunakan memasukkan  perintah `docker stop 6fe8a4ba919a`, Dan status akan berubah menjadi exit dengan memasukkan perintah `docker -ps a` berikut hasil keduanya;

![hasil Stop](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/soal_02_5.png)

# 3. Buat Dockerfile dan Push ke DockerHub
~hal yang perlu saya lakukan yaitu;
pertama mebuat folder dockerfile untuk menempatkan dockerfile yang akan saya buat.
kemudian dockerFile yang saya gunakan yaitu base image dari ubuntu, dan meletakkan perintah untuk menampilkan pesan dari cmd.
`FROM ubuntu
CMD ["echo", " -> 165610075 -> BAGAS SETIAWAN ~UTS TEKNOLOGI CLOUD~ Sistem pendidikan yang bijaksana setidaknya akan mengajarkan kita betapa sedikitnya yang belum diketahui oleh manusia, seberapa banyak yang masih harus ia pelajari. - Sir John Lubbock"]`
kemudian setelah membuat docker file yang perlu dilakukan membuat build image melalui docker quickstart terminal, dengan memasukkan perintah `docker build -t uts.tcc`, setelah selesai dilanjutkan dengan mengetikkan perintah `docker run -t uts.tcc` untuk menjalankan image yang telah dibuat;

![Proses build](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/soal_04_1.png)

![Proses run image](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/soal_04_2.png)

~lalu melakukan  push ke Repository DockerHub, dengan memasukkan perintah `docker tag uts.tcc bagas033/uts.tcc` dan dilanjutkan dengan mengetikkan perintah `docker push bagas033/uts.tcc`. berikut hasilnya;

![proses push](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/push_dockerhub_1.png)

![proses push](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/push_dockerhub_2.png)

![Hasil push](https://github.com/Bagas033/UTS-TCC-Bagas/blob/master/push_hasil_docker.png)