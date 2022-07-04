# Whatsapp Web js

untuk menggunakan Whatsapp web silahkan kunjungi [http://env-3280255.user.cloudjkt01.com/](http://env-3280255.user.cloudjkt01.com/) berikut, pada url tersebut masukkan description lalu tambah, setelah itu di bawah akan muncul description yang di isi tadi dengan status connecting. tunggu beberapa saat hingga barcode muncul, setelah barcode muncul scan barcode tersebut dengan akun Whatsapp, mausk dari tautkan perangkat. ketika scan berhasil silahkan tunggu hingga status ready. dan Api pun siap di gunakan, perlu di ingat harap mencatat id yang muncul ketika menambahkan akun

## API Reference

#### Send Message

```http
  POST /send-message
```

| Body      | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `number`  | `number` | **Required**. Your number  |
| `message` | `string` | **Required**. Your message |
| `sender`  | `string` | **Required**. Your id      |

| Headers        | value              |
| :------------- | :----------------- |
| `Content-Type` | `application/json` |
