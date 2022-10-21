# Komentar

Komentar Program adalah tulisan-tulisan atau keterangan-keterangan yang dapat memperjelas detail program yang dibuat oleh programmer. Komentar tidak dianggap sebagai bagian tubuh program, sehingga compiler tidak mengikutsertakan komentar dalam proses compile program.

Ada 2 jenis komentar di dalam `Go` yaitu: inline &multiline. Pada pembahasan kali ini dijelaskan tentang penerapan dan perbedaan jenis komentar ini.

## Komentar Inline

Aturan untuk menulis komentar ini di awali dengan tanda `double slash` ( // ) kemudian di ikuti dengan pesan komentarnya. Komentar inline ini hanya bisa dilakukan dengan satu baris saja. Jika kita ingin membuatnya lagi maka harus mengetikkan tanda `//` lagi.

```go title="Komentar Inline"
func main() {
    // Ini adalah komentar
    // Ini juga merupakan komentar

    fmt.Println("Ini akan tampil di terminal") // ini merupakan komentar
}
```

## Komentar Multiline

Jika kita ingin menggunakan pesan yang begitu panjang tidak mungkin jika penerapan komentar inline yang akan kita pakai. Maka itu akan susah dan menhabiskan waktu yang lama. Untuk membuat komentar multiline diawali dengan tanda `/*` dan di akhiri dengan tanda `*/`.

```go title="Komentar Multiline"
func main() {
    /*
        Hello saya merupakan komentar
        dan ini juga pesan komentar

        bisa banyak baris yang digunakan.
    */
}
```