# GO 

## QCM - Getting Started with Go: Deep Dive into Packages
<br>
<br>


### **Question** : The two files math.go and stats.go are stored on the file system under the directory named math. What is the most appropriate choice for the first line of executable code in stats.go?

> package math


#
### **Question** : Which are considered best practice when working with packages that comprise multiple files?

> Create a separate doc.go file with full package documentation

> Separate source code and associated test files into different files


#
### **Question** : Which statements accurately describes the init() function in Go?

> You may not pass any arguments to an init() function

> Each source file may have multiple init() functions


#
### **Question** : Assuming you have already installed the package godoc, which command issued at the terminal starts a http server over port 8080 to display documentation for a locally developed package math?

> godoc -http=localhost:8080


#
### **Question** : Complete the code snippet in order to blank import package strings.

```go
package main

import (
	"fmt"
	<missing code>

	"example.local/calc/math"
)

func main() {
	fmt.Println(math.Add(10, 20))
}
```

> _ "strings"


#
### **Question** : Complete the code to print the average of a slice of values named vals by calling the Avg function from the stats nest package.

```go
package main

import (
	"example.local/calc/math"
	"example.local/calc/math/stats"

	"fmt"
)

func main() {
	vals := []float64{1, 10, 100, 1000}
	fmt.Println(math.Add(10, 20))
	fmt.Println(<missing code>)
}
```

> stats.Avg(vals)


#
### **Question** : Which command when issued on the first line of a file named mypackage will declare a package named volume?

> package volume


#
### **Question** : You are creating a package for manipulating epoch data. Which is the best name according to best practice naming considerations?

> epoch


#
### **Question** : How do we make members from packages available to external packages?

> Their names must begin with an uppercase letter


#
### **Question** : Which statement defines a new release version v0.2.6 for a module that you are uploading to Git Hub source code repository?

> git tag v0.2.6


#
### **Question** : Complete the code snippet to print the average of a slice of values using the custom package math.

```go
package main

import (
	f "fmt"
	"math"
	. "os"
	_ "strings"

	m "example.local/calc/math"
)

func main() {
	vals := []float64{1, 10, 100, 1000}
	f.Println(<missing code>(vals))
	f.Println(math.Pi)
	f.Fprintln(Stdout, "Hello")
}
```

> m.Avg