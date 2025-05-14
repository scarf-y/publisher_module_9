# Tutorial Module 9 - Software Architectures

Nama: Daffa Naufal Rahadian<br>
NPM: 2306213003

## Refleksi 1
a. How much data your publisher program will send to the message broker in one
run?
<br/>
Dalam satu kali jalan, program publisher akan mengirim 5 buah pesan ke message broker. Masing-masing pesan berisi data berupa user_id dan user_name, yang dibungkus dalam struct UserCreatedEventMessage. Jadi, secara total, ada lima pesan yang dikirim, masing-masing dengan data pengguna berbeda.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber
program, what does it mean?
<br/>
URL tersebut adalah alamat koneksi ke RabbitMQ message broker yang digunakan oleh kedua program (publisher dan subscriber). Karena URL-nya sama, berarti kedua program ini terhubung ke broker yang sama, yaitu:
- guest (pertama) adalah username untuk login ke broker,
- guest (kedua) adalah password-nya,
- localhost:5672 menunjukkan bahwa koneksi diarahkan ke komputer lokal pada port 5672, yang merupakan port default RabbitMQ untuk protokol AMQP.

Dengan begitu, pesan yang dikirim oleh publisher akan bisa diterima oleh subscriber karena mereka berada di jaringan/message broker yang sama.


