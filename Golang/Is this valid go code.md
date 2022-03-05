Is this valid go code ?
```golang
fmt.Printf(fmt.Sprintf("%s\n", "Hello"));
```
---
Yes. Because `fmt.Printf` and `fmt.Println` supports single **non-string** arguments to print. No need of format specifiers for **single** arguments.