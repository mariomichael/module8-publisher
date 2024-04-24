1. How many data your publisher program will send to the message broker in one  run?
Program publisher akan mengirim 5 data ke message broker dalam satu run. Hal ini karena setiap pemanggilan ke `publish_event` akan mengirimkan 1 pesan.
<br />
2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
Artinya kedua program sama-sama menggunakan parameter koneksi yang sama untuk menyambung ke AMQP message broker. Keduanya memiliki username, password, address, dan port yang sama. Kesamaan ini memastikan kedua program dapat berkomunikasi secara efektif dengan instance message broker yang sama.

![RabbitMQ](images/rabbitmq_init.png)