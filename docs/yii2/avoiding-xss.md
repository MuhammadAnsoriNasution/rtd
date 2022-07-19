# Avoiding XSS

XSS atau skrip lintas situs terjadi ketika keluaran tidak lolos dengan benar saat mengeluarkan HTML ke browser. Misalnya, jika pengguna dapat memasukkan namanya dan alih-alih Alexander ia memasukkan <script>alert('Hello!');</script>, setiap halaman yang menampilkan nama pengguna tanpa keluar darinya akan menjalankan JavaScript alert('Hello!') ; mengakibatkan kotak peringatan muncul di browser. Bergantung pada situs web alih-alih peringatan yang tidak bersalah, skrip semacam itu dapat mengirim pesan menggunakan nama Anda atau bahkan melakukan transaksi bank.

## Usage/Examples

Untuk melakukan filter kita bisa memanfaatkan `\yii\helpers\HtmlPurifier::process($description)` yang tertera pada dokumentasi yii2.
contoh penerapan pada model

```php

    public function rules()
    {
        return [
            [['nama', 'alamat_property', 'no_telpon', 'jenis_penawaran'], 'filter', 'filter' => '\yii\helpers\HtmlPurifier::process', 'message' => '{attribute} input itdak valid'],
            [['nama', 'alamat_property', 'no_telpon', 'jenis_penawaran'], 'required'],
        ];
    }
```
