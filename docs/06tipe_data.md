# Tipe Data

Pada bahasa Go mempunyai beberapa jenis tipe data, di antaranya adalah berjenis `numerik` seperti (desimal ataupun non desimal), `string`, dan `boolean`

Pada pembelajaran ini akan dijelaskan beberapa tipe data yang telah disediakan oleh Go serta cara penggunaannya.

## Tipe Data Numerik `Non Desimal`

Tipe data non desimal atau `non floating point` ada beberapa jenis yaitu:

- `uint` adalah tipe data bilangan cacah(bilangan positif)
- `int` adalah tipe data bilangan bulat(bilangan positif dan negatif)

Nah dari beberapa tipe diatas dibagi lagi menjadi beberapa tipe data berdasarkan maksimal cakupan nilainya, bisa dilihat pada dibawah ini:

| Jenis  | Cakupan Bilangan Yang Di Tampung           |
|--------|--------------------------------------------|
| uint8  | 0 - 255                                    |
| uint16 | 0 - 65535                                  |
| uint32 | 0 - 4294967295                             |
| uint64 | 0 - 18446744073709551615                   |
| uint   | uint32 / uint64                            |
| byte   | sama dengan uint8                          |
| int8   | -128 - 127                                 |
| int16  | -32768 - 32767                             |
| int32  | -2147483648 - 2147483647                   |
| int64  | -9223372036854775808 - 9223372036854775807 |
| int    | int32 / int64                              |
| rune   | int32 / int64                              |

Pengembang Go dianjurkan memakai tipe data variabel sebisa mungkin dipilih sesuai dengan jenisnya, karena jika sembarangan saja maka penggunaaan memori akan banyak.

```go
var positive uint8 = 88
var negative = -1243234455

fmt.Printf("Positive: %d\n", positive)
fmt.Printf("Negative: %d\n", negative)
```

---

## Tipe Data Desimal

Untuk tipe data `desimal` ada dua jenis yaitu `float32` dan `float64` sama dengan tipe data `numerik non desimal` mempunyai nilai lebar cakupan yang bisa di tampung.

```go
bilanganDesimal := 5.532

fmt.Printf("Bilangan Desimal: %f\n", bilanganDesimal)
fmt.Printf("Bilangan Desimal: %.2f\n", bilanganDesimal)
```

---

## Tipe Data Boolean

Tipe data boolean mempunyai nilai `true` dan `false`.

```go title="Contoh Boolean"
var isAuthenticated bool = true

fmt.Printf("Authenticated: %t\n", isAuthenticated)
```

Gunakan `%t` untuk format data `bool` jika menggunakan `fmt.Printf()`

---

## Nilai `nil` dan `zero`

Keyword `nil` sebenarnya bukanlah tipe data tetapi adalah sebuah nilai. Variabel yang mempunyai nilai `nil` berarti variabel itu tidak memiliki nilai sama sekali atau kosong.

> Semua tipe data diatas memiliki nilai `nil` atau nilai default. Jadi meskipun kita sudah mendeklarikan dengan nilai awal, tetapi dia mempunyai nilai default yaitu `nil`

- Zero value untuk `string` adalah `""`
- Zero value untuk `bool` adalah `false`
- Zero value untuk `numerik non desimal` maupun `numerik desimal` adalah `0`

> `CATATAN`: Zero value berbeda dengan nilai `nil`. `Nil` merupakan nilai yang kosong, sangat-sangat kosong. Nilai `nil` tidak bisa digunakan pada tipe data diatas. Nilai `nil` hanya bisa digunakan pada:

- pointer
- fungsi
- slice
- map
- channel
- interface yang kosong
- any (alias interface) 
