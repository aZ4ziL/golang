# Variabel

Bahasa Go ada dua jenis untuk mendeklarasikan penulisan variabel, ada yang dituliskan tipe datanya dan ada yang tidak. Walaupun caranya berbeda tetapi tujuannya sama, bedanya hanya di penulisannya saja.

## Mendeklarasi Variabel Dengan Tipe Data

Silahkan buat folder project baru terserah apa namanya, lalu masuk ke dalam foldernya dan ketik `go mod init nama-project` 

```go title="Variabel Dengan Tipe Data"
package main

import "fmt"

func main() {
    var namaDepan string = "Sweet"

    var namaBelakang string
    namaBelakang = "O`mine"

    fmt.Println("Halo", namaDepan, namaBelakang)
}
```

### Penjelasan

Pada kode di atas kita bisa lihat cara penulisan variabel harus menggunakan `var` dan `tipe datanya`. Untuk lebih jelasnya bisa perhatikan aturan dibawah ini.

```go title="Aturan Variabel dengan tipe data"
var <nama-variabel> <tipe-data>

// Atau
var <nama-variabel> <tipe-data> = <nilai>
```

## Mendeklarasi Variabel Tanpa Tipe Data

Go mengadopsi konsep inference yaitu metode untuk mendeklarasikan variabel menurut tipe data dari nilai variabelnya. Dengan metode ini kita tidak perlu menuliskan kode `var`. Untuk lebih jelasnya mari kita lihat kode dibawah ini.

```go title="Variabel Tanpa Tipe Data"
var namaDepan string = "John" // Variabel dengan tipe data

namaBelakang := "Cena"
```

Bisa kita simpulkan untuk membuat sebuah variabel tanpa tipe data kita tidak perlu menuliskan kode `var` dengan menggunakan kode `:=` dan keyword var dihilangkan. Tipe data dengan nama `namaDepan` bisa kita lihat tipe datanya adalah bertipe `string`. Tipe data dengan nama `namaBelakang` tipe datanya akan otomatis menjadi `string`, karena nilai dari variabelnya berjenis string.

## Mendeklarasi Multi Variabel

Go juga mendukung metode deklarasi multi variabel secara sekaligus dengan cara menuliskan variabel-variabelnya dengan pembatas tanda koma `(,)`. Untuk pengisian nilainya boleh juga secara bersamaan dan juga tidak.

```go title="Multi variabel dengan mengisi nilai secara tidak bersamaan"
var nama1, nama2, nama3 string
nama1 = "John"
nama2 = "Wick"
nama3 = "Ente"
```

```go title="Multi variabel dengan mengisi nilai secara bersamaan"
var nama1, nama2, nama3 string = "John", "Wick", "Ente"
```

```go title="Multi variabel tanpa tipe data"
nama, umur, berat := "John", 45, 72.65
```

## Variabel Underscore `_`

Di bahasa Go memiliki aturan yang berbeda(unik) dari bahasa lain, yaitu tidak boleh ada satupun variabel yang tidak dipakai atau `not used`. Jadi, semua variabel yang dideklarasikan harus digunakan. Jika tidak maka saat compile program akan muncul pesan `error`

```
name declared and not used
```

Artinya: variabel dideklarikan tetapi tidak digunakan.

```go title="Variabel Underscore"
name, _ := "John", 45

_ := "Wick"
```

Variabel name berisikan nilai `John` sedangkan nilai Wick akan ditampung kedalam variabel underscore `(_)`, artinya tidak akan pernah digunakan. Jadi apapun variabel underscore itu tidak akan digunakan saat proses compile.