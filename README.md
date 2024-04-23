# adpro-tutorial8-subscriber

a. what is amqp?
Jawab:
amqp merupakan singkatan dari **Advanced Message Queuing Protocol** yang merupakan standard dalam melakukan passing business messages antara aplikasi dan organisasi, yang berarti aplikasi dari client dibuat untuk bisa berkomunikasi dengan apliaksi sumber yang mengirimkan informasi / data.

b. what it means? guest:guest@localhost:5672 , what is the first quest, and what is the second guest, and what is localhost:5672 is for?
Jawab:
`guest:guest@localhost:5672` adalah sebuah connection URI (Uniform Resource Identifier) yang digunakan untuk menghubungkan sebuah message broker yang mendukung AMQP (seperti RabbitMQ). URI ini menyediakan semua informasi yang dibutuhkan untuk menjalin hubungan dari aplikasi client ke broker.

`guest` pertama: Username yang digunakan untuk diautentikasi dengan message broker

`guest` kedua: Password yang berhubungan dengan username

`localhost:5672` : Menspefikasikan hostname atau IP address dan juga portnumber yang di-listen oleh AMQP service.
