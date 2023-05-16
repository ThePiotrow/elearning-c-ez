# GO 

## QCM - Go Programming Literacy (Intermediate Level)
<br>
<br>


### **Question**: Which software implementation paradigms are supported by Go?

> `Procedural`

> `Distributed`

> `Concurrent`


#
### **Question** : The Go programming language is used by some big tech companies and is popular in certain domains. What are some of these domains?

> `Cloud-native development`

> `Distributed network services`


#
### **Question** : In which areas does Go present shortcomings?

> `Support for generics`

> `GUI library support`


#
### **Question** : Which statement defines a module path at example.local/demo?

> `go mod init example.local/demo`


#
### **Question** : What are some implementation-specific data types in Go?

> `uintptr`

> `int`

> `uint`


#
### **Question** : What will be the output from this code snippet?

```go
func main() {
	x := 5
	y := 2
	fmt.Println(x%y)
}
```

> `1`


#
### **Question** : Which statement declares and initializes an array of four integer values in Go?

> `arr := [4]int{0, 1, 2, 3}`


#
### **Question** : Complete the code snippet so that the resultant output will be Wednesday.

```go
package main

import "fmt"

func main() {
	workday := 3
 	switch <missing code> {
	case 1: fmt.Println("Monday")
	case 2: fmt.Println("Tuesday")
	case 3: fmt.Println("Wednesday")
	case 4: fmt.Println("Thursday")
	case 5: fmt.Println("Friday")
	default: fmt.Println("Take the weekend off!")
	}
}
```

> `workday`


#
### **Question** : How is inheritance supported by Go?

> `With interfaces`


#
### **Question** : Complete the code snippet provided so that it will give a result of 10.

```go
package main

import "fmt"

func multiply(x, y *int) int {
	return *x * *y
}

func main() {
	x := 5
	y := 2
	fmt.Println(multiply(<missing code>))
}
```

> `&x, &y`


#
### **Question** : Complete the code snippet to successfully create a method volume() for the Box type.

```go
package main

import "fmt"

type Box struct {
	D float64
	W float64
	H float64
}

func <missing code> volume() float64 {
	return b.D * b.W * b.H
}

func main() {
	b := Box{D: 5, W: 4, H: 3}
	fmt.Println(b.volume())	
}
```

> `(b Box)`

> `(b *Box)`


#
### **Question** : Complete the code snippet so that the code iterates over all the shapes calling each object's volume() method.

```go
func totalVolume(shapes ...Shape) float64 {
var volume float64
for _, s := <missing code> shapes {
	volume += s.volume()
}
return volume
}
```

> `range`


#
### **Question** : Which statements accurately describe error handling in Go?

> `Functions may return error values`

> `Errors in Go are simple values`


#
### **Question** : Given that the signature for Go's built-in panic() function is func panic(v interface{}), what types of values can be passed to panic()?

> `Any data type`


#
### **Question** : Assuming "myFile.txt" exists in the current directory, complete the code snippet that would result in the file name, size, and permissions being printed.

```go
// return a FileInfo describing file
func main() {
	f, err := <missing code>("myFile.txt")
	if err != nil {
		log.Fatal(err)
	}
	log.Println("file name:", f.Name())
	log.Println("file size:", f.Size())
	log.Println("file permissions:", f.Mode())
}
```

> `os.Stat`