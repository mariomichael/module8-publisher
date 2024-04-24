1. How many data your publisher program will send to the message broker in one  run?
Program publisher akan mengirim 5 data ke message broker dalam satu run. Hal ini karena setiap pemanggilan ke `publish_event` akan mengirimkan 1 pesan.
<br />
2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
Artinya kedua program sama-sama menggunakan parameter koneksi yang sama untuk menyambung ke AMQP message broker. Keduanya memiliki username, password, address, dan port yang sama. Kesamaan ini memastikan kedua program dapat berkomunikasi secara efektif dengan instance message broker yang sama.

![RabbitMQ](images/rabbitmq_init.png)
Tampilan RabbitMQ ketika dijalankan pada localhost:15672/

![Termimal](images/terminal1.png)
Ini adalah ampilan terminal ketika publisher melakukan publish 5 event message dan subscriber menerimanya.

![Spike](images/spikes.png)
Ini adalah tampilan dari spike yang muncul ketika cargo run dijalankan pada publisher. Perubahan grafik ini ditentukan dari frekuensi pengiriman data oleh publisher. Grafik menaik lalu menurun karena publisher mengirim data sekali lalu berhenti. Jika mengirim data terus, grafik akan terus menaik.