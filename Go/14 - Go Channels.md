# GO 

## QCM - Getting Started with Go: Go Channels
<br>
<br>


### **Question** : Question: What is the last stage in the pipeline commonly referred to as?

> `Sink`

> `Consumer`


#
### **Question** : What will be the first line of output when this program runs?

```go
func main() {
	ch1 := make(chan int)
	ch2 := make(chan int)

	go func() {
		for i := 1; i < 4; i++ {
			time.Sleep(3 * time.Second)
			ch1 <- i
			time.Sleep(1 * time.Second)
			ch2 <- i
		}
	}()

	for i := 1; i < 5; i++ {
		select {
		case val := <-ch1:
			fmt.Printf("received from ch1: %v\n", val)
		case val := <-ch2:
			fmt.Printf("received from ch2: %v\n", val)
		default:
			fmt.Println("no data received...")
		}
		time.Sleep(2 * time.Second)
	}
}
```

> `no data received...`


#
### **Question** : Complete the code snippet to implement a timeout case that will timeout after 5 seconds.

```go
for i := 0; i < 3; i++ {
select {
	case val1 := <-ch1:
		fmt.Printf("value received from ch1: %v\n", val1)
	case val2 := <-ch2:
		fmt.Printf("value received from ch2: %v\n", val2)
	case val3 := <-ch3:
		fmt.Printf("value received from ch3: %v\n", val3)
	case to := <missing code>:
	 	fmt.Printf("timed out after 5 seconds at %v\n", to)
	 	return
	}
}
```

> `<-time.After(5 * time.Second)`


#
### **Question** : Complete the code snippet so that the anonymous function returns its result by sending it to the channel ch.

```go
func main() {
	ch := make(chan int)
	mult := func(x, y int) {
		res := x * y
		<missing code>
	}
	go mult(10, 10)
	val, ok := <-ch
	fmt.Printf("type of value of ch is: %T\n", ch)
	fmt.Printf("the value of ch is: %v\n", ch)
	fmt.Printf("the resulting value from the goroutine is: %v\n", val)
	fmt.Printf("the value of ok is: %v\n", ok)
}
```

> `ch <- res`


#
### **Question** : Complete func main() so that it can use range() to range over the values in the channel ch and print them to stdout.

```go
func main() {
	ch := make(chan string, 2)

	go func(ch chan string) {
		defer close(ch)
		for i := 1; i <= 5; i++ {
			msg := "message" + strconv.Itoa(i)
			ch <- msg
			fmt.Printf("SEND goroutine: %v\n", msg)
		}
	}(ch)

	go func(ch chan string) {
		<missing code> {
			fmt.Printf("RECV goroutine: %v\n", val)
		}
	}(ch)

	fmt.Println("MAIN goroutine: sleeping!")
	time.Sleep(time.Millisecond * 100)
	val, ok := <-ch
	fmt.Printf("values returned: %q, %v\n", val, ok)
	fmt.Println("MAIN goroutine: done!")
}
```

> `for val := range ch`


#
### **Question** : Complete the code snippet to create a buffered channel of integer values with the capacity of 25.

```go
ch := make(<missing code>)
```

> `chan int, 25`


#
### **Question** : How can we implement nonblocking sends and receives with a SELECT statement

> `By including a default clause`


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
### **Question** : Which Go function returns an object that can be used as an http.ResponseWriter object?

> `httptest.NewRecorder`


#
### **Question** : The code that interacts directly with a database should be included in which layer of a Model-View-Controller architecture?

> `Repository`


#
### **Question** : Which HTTP/2 feature allows clients to get responses from the server without a request?

> `Server push`

