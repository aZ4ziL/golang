# Program Hello World

Untuk mempelajari bahasa pemrograman yang baru biasanya kita harus tahu bagaimana bentuk dari program sederhana `hello world`. Jika kita sudah paham dengan code sederhana ini, maka kita akan lebih paham untuk mempelajarinya.

## Code Program Hello World

Buat sebuah file dengan nama `main.go` di dalam folder project kita yang di dalamnya ada file `go.mod`

```go title="Program Hello World"
package main

import "fmt"

func main() {
    fmt.Println("Hello World")
}
```

```bash title="Output"
Hello World
```