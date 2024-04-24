
# REFLECTION

a. what is amqp?

- kepanjangan dari AMQP adalah Advanced Message Queuing Protocol. AMQP merupakan sebuah sebuah protokol standar yang digunakan dalam lapisan aplikasi untuk middleware yang berorientasi pada pesan.
Biasanya, protokol ini digunakan untuk membangun sistem pengiriman pesan. Dengan menggunakan AMQP, berbagai jenis aplikasi dapat saling berkomunikasi dengan efisien dengan melakukan pertukaran pesan.


b. what it means? guest:guest@localhost:5672 , what is the first quest, and what is
the second guest, and what is localhost:5672 is for?

- guest:guest@localhost:5672 merupakan string koneksi untuk sebuah server AMQP. guest:guest merupakan kombinasi kombinasi nama pengguna dan kata sandi default untuk autentikasi pada server.
  nama pengguna dan kata sandi defaultnya juga guest pada konfigurasi standar broker pesan seperti RabbitMQ. Akan tetapi, di lingkungan produksi, disarankan untuk mengubah kredensial default ini karena pertimbangan keamanan.
- @localhost:5672 merupakan alamat host dan port yang digunakan. Localhost merujuk pada alamat local, yang berarti bahwa message broker (RabbitMQ) berjalan di komputer yang sama di mana kode ini dieksekusi. Port 5672 adalah port default yang digunakan oleh RabbitMQ untuk melakukan komunikasi menggunakan protokol AMQP.

# SIMULATION SUBSCRIBER

<a href="https://ibb.co/bNx34xt"><img src="https://i.ibb.co/MPbhzbd/BEFORE.png" alt="BEFORE" border="0"></a>

# 3 subsriber 
<a href="https://ibb.co/FgyJYC2"><img src="https://i.ibb.co/HnbYP36/Whats-App-Image-2024-04-24-at-16-48-24.jpg" alt="Whats-App-Image-2024-04-24-at-16-48-24" border="0"></a>


Ketika saya menjalankan cargo run sebanyak 3 kali di tiga console yang berbeda pada subscriber dan cargo run sebanyak 4 kali pada publisher, terlihat bahwa spike dari message queue berkurang. Hal ini menandakan penanganan pesan lebih cepat daripada sebelumnya karena request yang diterima queue akan dibagi-bagi untuk ditangani oleh ketiga subscriber.
