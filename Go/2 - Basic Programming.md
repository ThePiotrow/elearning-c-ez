# GO 

## QCM - Getting Started with Go: Basic Programming
<br>
<br>


### **Question**: What will be the result of this Go program?

```go
package main

import "fmt"

func main() {

	var prodPrice map[string]int
	fmt.Println(prodPrice)
	prodPrice["widget"] = 100
}
```

> a panic error



#
### **Question** : What will be the output from this program?

```go	
package main

import "fmt"

var workday = 5

func main() {
	workday := 3
	switch workday {
	case 1:
		fmt.Println("Monday")
	case 2:
		fmt.Println("Tuesday")
	case 3:
		fmt.Println("Wednesday")
	case 4:
		fmt.Println("Thursday")
	case 5:
		fmt.Println("Friday")
	default:
		fmt.Println("Take the weekend off!")
	}
}
```

> Wednesday


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

> workday


#
### **Question** : Which loop control statement aborts the current iteration of a for loop, but still stays in the for loop?

> continue


#
### **Question** : What are some implementation-specific data types in Go?

> uint

> int

> uintptr


#
### **Question** : Which statement declares and initializes an array of four integer values in Go?

> arr := [4]int{0, 1, 2, 3}


#
### **Question** : Complete the code to loop over all the elements in the map data structure.


```go 
func main() {

	prodPrice := map[string]int{
		"widget":             75,
		"turbo widget":       100,
		"convertible widget": 150,
	}
	for key, value := <missing code> prodPrice {
		fmt.Println(key, value)
	}
}
```

> range


#
### **Question** : What is the resultant output of this program?


```go
package main

import (
    "fmt"
    "strings"
)
 
func main() {
    fmt.Println(strings.Contains("Working with functions", "functions"))
}
```

> true


#
### **Question** : What is the zero value for a pointer data type?

> nil


#
### **Question** : Complete the code snippet to successfully append the slice named slAppend to the slice named sl.


```go
func main() {

	sl := []int{0, 1, 2, 3}
	slAppend := []int{4, 5, 6}
	sl = <missing code>
	fmt.Println("length of sl: ", len(sl))
	fmt.Println("values:", sl)
}
```

> append(sl, slAppend...)

<br>


#
### **Question** : What will be the output from this code snippet?

```go
func main() {
	x := 5
	y := 2
	fmt.Println(x%y)
}
```

> 1


#
### **Question** : Which character is formally used as a blank identifier in Go?

> _


#
### **Question** : Which statement will initialize a constant myConst as an implicitly typed constant?

> const myConst = 1


#
### **Question** : A basic for loop in Go is made up of which components?

> init statement

> condition statement

> post statement


#
### **Question** : Complete the code snippet to output the value stored by the variable val.

```go
package main

import "fmt"

func main() {

	val := 123
	ptr := &val
	fmt.Println(<missing code>)

}
```

> *ptr