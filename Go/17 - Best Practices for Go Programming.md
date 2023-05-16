# GO 

## QCM - Getting Started with Go: Creating a Go Web Server
<br>
<br>


### **Question** : As a best practice, what should be used instead of long sequences of if-else statements to handle special cases in Go?

> Type switching


#
### **Question** : Complete the TestSubTable table-driven test so it runs correctly and tests all three scenarios specified in the data slice of struct.

```go
func TestSubTable(t *testing.T) {
	data := []struct {
		x        int
		y        int
		expected int
	}{
		{x: 2, y: 1, expected: 1},
		{x: 2, y: 2, expected: 0},
		{x: 2, y: 3, expected: -1},
	}

	for _, val := range data {
		got := calc.Sub(val.x, val.y)
		if got != <missing code> {
			t.Errorf("expected: %v got: %v", val.expected, got)
		}
	}
}
```

> val.expected


#
### **Question** : Which are considered Go syntax best practices?

> Never declare a variable or import a package that will not be used in the program

> As a workaround, use the blank identifier "_" when importing packages that won't be used


#
### **Question** : Which do we use to signal to the parent process that the goroutines have completed their work and the parent process can now safely carry on?

> WaitGroups


#
### **Question** : Which value reduces the risk from setting too high an idle database connection pool by setting the maximum time that a connection may be reused?
> ConnMaxLifetime


#
### **Question** : Which function in package fmt from the standard library supports generating formatted strings for error reporting?

> Errorf


#
### **Question** : Which statement runs an instance of godoc server locally over port 8080?

> godoc -http=localhost:8080


#
### **Question** : Complete the code snippet that will signal to the main goroutine to stop blocking on the done channel.

```go
package main

import "fmt"

func main() {
	msg := make(chan int, 10)
	done := make(chan bool)

	go func() {
		for {
			i, work := <-msg
			if work {
				fmt.Printf("Message %v processed!\n", i)
			} else {
				fmt.Println("All messages processed!")
				<missing code>
				return
			}
		}
	}()

	for i := 1; i <= 5; i++ {
		msg <- i
		fmt.Printf("Message %v sent to be processed.\n", i)
	}
	close(msg)
	fmt.Println("Processing completed!")

	<-done
}
```

> done <- true


#
### **Question** : Which are common methods for organizing a directory structure for Go projects?

> Modularized approach

> Flat approach



#
### **Question** : Which statements accurately describe the defer, panic and recovery process?

> Panic stops normal execution of the current goroutine

> Recover must be invoked within a deferred function call


#
### **Question** : Which are benefits related to using an InitDB function to initialize a database connection pool?

> All the database-related code is contained in one package

> InitDB() function can be used to initialize a test database connection pool


#
### **Question** : When testing our programs, how can we effectively write tests focused on the interface exposed to the client?

> Use a separate package for storing tests