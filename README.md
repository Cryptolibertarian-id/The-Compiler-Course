# The Compiler Course



# Types

In C++ the size of a given data type is dependent on the compiler and/or the computer architecture. C++ only guarantees that each fundamental data types will have a minimum size. 

When we use **keyword sizeof** in C or C++, a type is determined by the compiler, which doesn't have to have anything to do with the actual hardware (though it typically does); in fact, different compilers on the same machine can have different values for these.

For example in go language, they support implementation specific type. The use of **int** and **uint keywords** will help the compiler to produce code according to the target computer machine architecture. 

This process is called **Implementation Specific Type** or **platform dependent**, the use of int and uint is highly recommended because there are different computer machine architectures (32 & 64 bit). 

If we make a Go program with the data type int then when compiled with the target architecture 32 bit the size of the data type is also 32 bit, so if we compile on a 64 bit architecture the variable size remains 64 bit.

Go also support **Architecture-independent type**, the data bit size does not change even though the program is executed on any computer machine.

Most of today's computer machine architecture has reached 32 bit and 64 bit. If we write a program and it has an int32 data type, its size will remain constant when we execute it on a 64 bit computer machine architecture.

| Language | Type  | Size (32 bit) | Size (64 bit) | Note                     |
| -------- | ----- | ------------- | ------------- | ------------------------ |
| C        | int   | 2 bytes       | 4 bytes       | TDM-GCC 10.3.0           |
| C++      | int   | 2 bytes       | 4 bytes       | TDM-GCC 10.3.0           |
| Go       | int32 | 4 bytes       | 8 bytes       | Go 1.18.4                |
| Solidity | int32 | 4 bytes       | 4 bytes       | Solidity Compiler 0.15.0 |





| Language |            |                              |       |                     |      |         |      |
| -------- | ---------- | ---------------------------- | ----- | ------------------- | ---- | ------- | ---- |
| C        | char       | int                          | float | double              | bool | pointer | void |
| C++      | char       | short, int, long, long, long | float | double, long double | bool | pointer | void |
| Go       | byte, rune | int                          | float |                     | bool |         |      |
| Solidity |            | int                          |       |                     | bool |         |      |

In Go, **there is no char data type**. It uses byte and rune to represent character values. The byte data type represents ASCII characters while the rune data type represents a more broader set of Unicode characters that are encoded in UTF-8 format.



---



# Execution



## Rust Compilation

Create directory hello/src and then create hello.rs

```rust
fn main() {
	println!("Hello World")
}
```

To compile execute this command :

```bash
$ rustc hello.rs
```



---



## Javascript

Create directory hello/src and then Create file hello.js

```javascript
console.log("Hello World!")
```

To Execute the script using node.js :

```bash
$ node hello.js
```



----



# Basic Structure



## Hello World



### C

```c
#include <stdio.h>

int main() {
  printf("Hello World!");
  return 0;
}
```



### C++

```c++
#include <iostream>

int main()
{
   std::cout << "Hello world!";
   return 0;
}
```



### Go

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello world!")
}
```



### Javascript

```javascript
console.log("Hello World!")
```



----



# Integer Behaviors



## Integer Division



### C

```c
#include <stdio.h>

int main() {
	int x = 8;
	int y = 5;
	printf("%d", x/y);
	return 0;
}
```



### C++

```c++
#include <iostream>

int main() {
	int x = 8;
	int y = 5;
	std::cout << x / y;
	return 0;
}
```

Output : 

```
1 (integer)
```



### Go

```go
package main

import "fmt"

func main() {
	var result int
	result = (8 / 5)
	fmt.Println(result)
}
```

Output : 

```
1 (integer)
```



### Javascript

```javascript
let x = 8;
let y = 5;
console.log(8/5)
```

Output : 

```
1.6 (number)
```

