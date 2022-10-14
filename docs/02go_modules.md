# Go Modules

Go modules adalah manajemen depedensi resmi dari Go. Go modules penggunaannya hanya melalui CLI(Command Line Interface) jika di Windows melalui CMD dan di Unix menggunakan Terminal.

## Inisialisasi Project menggunakan Go modules

```bash title="Konfigurasi go modules"
mkdir project-name
cd project-name
go mod init project-name
```

Maka akan terbuat sebuah file dengan nama <code>go.mod</code> yang berisi nama package dan versi golang yang kita pakai.

```go title="go.mod"
module project-name

go 1.19
```