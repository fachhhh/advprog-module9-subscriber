# Advprog Module 9 Tutorial
Hadyan Fachri\
2306245030\
Advprog A

## Reflection
**a. What is amqp?**
- AMQP (Advanced Message Queuing Protocol) adalah protokol standar terbuka yang digunakan untuk pertukaran pesan antar sistem secara asinkron. Protokol ini mendukung komunikasi yang andal, terdistribusi, dan aman antara komponen perangkat lunak, seperti dalam arsitektur berbasis event atau microservices. AMQP memungkinkan penerapan antrian pesan (message queues) yang efisien, seperti yang digunakan oleh RabbitMQ atau Kafka, untuk memastikan pengiriman pesan yang teratur dan scalable.

**b. What does it mean? guest:guest@localhost:5672 , what is the first guest, and what is the second guest, and what is localhost:5672 is for?**
- `guest:guest`:
    - Guest pertama: Username default untuk mengakses RabbitMQ (biasanya "guest").
    - Guest kedua: Password default (biasanya "guest").
    Keduanya adalah kredensial standar yang digunakan untuk autentikasi ke RabbitMQ dalam lingkungan pengembangan.

- `localhost:5672`:
    - `localhost`: Menunjukkan bahwa RabbitMQ berjalan di mesin lokal (server yang sama dengan aplikasi). 
    - `5672`: Port default yang digunakan oleh AMQP untuk komunikasi dengan RabbitMQ. Port ini memungkinkan publisher dan subscriber terhubung ke broker pesan.

- Pada kode subscriber/publisher, URL `amqp://guest:guest@localhost:5672` digunakan untuk menghubungkan aplikasi Rust ke instance RabbitMQ yang berjalan di mesin lokal dengan kredensial default. Jika di-deploy di lingkungan produksi, kredensial dan alamat harus disesuaikan untuk keamanan.