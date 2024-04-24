# adpro-tutorial8-subscriber

a. what is amqp?
Jawab:
amqp merupakan singkatan dari **Advanced Message Queuing Protocol** yang merupakan standard dalam melakukan passing business messages antara aplikasi dan organisasi, yang berarti aplikasi dari client dibuat untuk bisa berkomunikasi dengan apliaksi sumber yang mengirimkan informasi / data.

b. what it means? guest:guest@localhost:5672 , what is the first quest, and what is the second guest, and what is localhost:5672 is for?
Jawab:
`guest:guest@localhost:5672` adalah sebuah connection URI (Uniform Resource Identifier) yang digunakan untuk menghubungkan sebuah message broker yang mendukung AMQP (seperti RabbitMQ). URI ini menyediakan semua informasi yang dibutuhkan untuk menjalin hubungan dari aplikasi client ke broker.

`guest` pertama: Username yang digunakan untuk diautentikasi dengan message broker

`guest` kedua: Password yang berhubungan dengan username

`localhost:5672` : Menspesifikasikan hostname atau IP address dan juga portnumber yang di-listen oleh AMQP service.

Foto:
![image](https://github.com/reyhanwiyasa/adpro-tutorial8-subscriber/assets/119433464/829e11d1-8567-4dc9-9c2f-5ea4e26ed88b)
Pada gambar diatas dapat dilihat kalau pada suatu saat sempat terdapat 100 message pada queue. Ini terjadi karena subscriber memererlukan waktu yang lebih lama untuk menghandle tiap event yang berada di message queue. Hal ini menyebabkan terjadinya penumpukkan message karena publisher meng-publish message lebih cepat daripada subscriber membuat message.

![image](https://github.com/reyhanwiyasa/adpro-tutorial8-subscriber/assets/119433464/6f891056-49f5-4877-abd7-78d2aa4a1120)
Tiap subscriber berfungsi seperti aplikasi terpisah yang independent satu sama lain sehingga mereka mendapat data yang berbeda-beda ketika publisher mengirimkan banyak data ke message queue. Ketika data sudah terambil dari message queue, maka message akan hilang dan aplikasi lain tidak bisa menggunakannya.

Salah satu cara untuk meningkatkan performa dari aplikasi subscriber adalah dengan membuatnya menjadi multithreading agar dapat mengolah banyak event dari publisher sekaligus.
