# The Compiler Course







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

