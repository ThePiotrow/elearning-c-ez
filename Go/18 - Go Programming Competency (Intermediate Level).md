# GO 

## QCM - Go Programming Competency (Intermediate Level)
<br>
<br>


### **Question**: Complete the code to print the average of a slice of values named vals by calling the Avg function from the stats nest package.

> `stats.Avg(vals)`


#
### **Question** : Which statement defines a new release version v0.2.6 for a module that you are uploading to Git Hub source code repository?

> `git tag v0.2.6`


#
### **Question** : Which function from the WaitGroup type does the main goroutine call to tell Go the number of goroutines to wait for?

> `Add()`


#
### **Question** : Which statement initializes a variable named ‘cores’ to the number of CPU cores on a device?

> `cores := runtime.NumCPU()`

#
### **Question** : Complete the code snippet that will run the function g1( ) as a goroutine.

> `go g1()`


#
### **Question** : Complete the code snippet to implement WaitGroups with goroutines.

```go
func main() {
	var wg sync.WaitGroup

	for i := 1; i <= 5; i++ {
		wg.Add(1)
		<missing code>
	}
	wg.Wait()
	fmt.Println("Each goroutine has run to completion!")
}

func myfunc(wg *sync.WaitGroup, i int) {
	defer wg.Done()
	fmt.Println("Finished executing iteration", i)
}
```

> `go myfunc(&wg, i)`


#
### **Question** : Since Go v1.1, how can the race detector be used when running a Go program?

> `By specifying the -race flag at the command line`


#
### **Question** : Complete the receive() function to have it print out the values from the channel ch that were.

```go
func receive(ch chan string) {
	for i := 0; i < 3; i++ {
		fmt.Printf("received: %v\n",<missing code>)
		fmt.Printf("channel length: %v\n", len(ch))
	}
}
```

> `<-ch`


#
### **Question** : You are combining channels and weight groups with goroutines but your program results in a deadlock. Which statement in func main is responsible for the deadlock condition?

```go
func main() {
	var wg sync.WaitGroup
	ch := make(chan int)

	wg.Add(2)

	go func() {
		wg.Wait() // wait for the goroutines to complete
		close(ch) // close the channel when finished
	}()

	go func() {
		defer wg.Done() // decrement wg counter by 1
		ch <- 1
	}()

	go func() {
		defer wg.Done() // decrement wg counter by 1
		ch <- 2
	}()

	wg.Wait() // wait for the program to complete
	for val := range ch {
		fmt.Printf("value received: %v\n", val)
	}
	val, ok := <-ch
	fmt.Println(val, ok)
}
```

> `wg.Wait() // wait for the program to complete`


#
### **Question** : Complete the code snippet so that the pipeline for this program can leverage the fanout fan in approach while processing the data using channels.

```go
func main() {
    vals := []int{100, 50, 20, 90}
    in := gen(vals)

    // fan-out
    fo1 := square(in)
    fo2 := square(in)

    // fan-in
    fi := merge(<missing code>)
    for res := range fi {
        fmt.Println(res)
    }
}
```

> `fo1, fo2`


#
### **Question** : Complete the statement to generate a prepared statement to be used in a SQL query in Go against a MySQL database.

> `stmt, err := db.Prepare("SELECT * FROM users WHERE id=?")`


#
### **Question** : Which variable type can be used to handle a varchar database column that is nullable?

> `sql.NullString`


#
### **Question** : Complete the TestAdd function to report a failed test but allow the test to complete.

```go
func TestAdd(t *testing.T) {
	got := calc.Add(2, 1)
	expected := 3

	if got != expected {
		<missing code> ("got: %v expected: %v", got, expected)
	}
}
```

> `t.Errorf`


#
### **Question** : You are using the Heroku CLI to deploy a Go application to Heroku. Assuming that you are signed into Heroku from a terminal session, which command may be used to deploy an app named main to Heroku?

> `git push heroku main`


#
### **Question** : As a best practice, what should be used instead of long sequences of if-else statements to handle special cases in Go?

> `Type switching`