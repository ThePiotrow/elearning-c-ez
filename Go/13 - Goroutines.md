# GO 

## QCM - Getting Started with Go: Goroutines
<br>
<br>


### **Question** : Complete the code snippet to successfully implement a mutex in the critical section of the anonymous function for inc.

```go
func main() {
runtime.GOMAXPROCS(runtime.NumCPU())

var counter int
var wg sync.WaitGroup
var mu sync.Mutex

inc := func() {
<missing code>
defer mu.Unlock()
counter++
fmt.Println("increment counter = ", counter)
}

for i := 0; i < 1000; i++ {
wg.Add(1)
go func() {
defer wg.Done()
inc()
}()
}

wg.Wait()
fmt.Println("final value of counter", counter)
}
```

> mu.Lock()


#
### **Question** : Complete the code snippet that will run the function g1( ) as a goroutine.

```go
func main() {
	fmt.Println("running in main routine")
	<missing code>
	time.Sleep(10 * time.Millisecond)
	fmt.Println("exited from main routine")
}

func g1() {
	fmt.Println("running in goroutine g1")
}
```

> go g1()


#
### **Question** : Since Go v1.1, how can the race detector be used when running a Go program?

> By specifying the -race flag at the command line


#
### **Question** : Complete the closure in the code snippet so that each closure gets its own isolated value of the variable i.

```go
func main() {
	for i := 0; i < 5; i++ {
		go func(i int) {
			fmt.Println("i = ", i)
		}<missing code>
	}
	time.Sleep(10 * time.Millisecond)
}
```

> (i)


#
### **Question** : Complete the inc() function to have it return an anonymous function that only returns an int value and takes no arguments.

```go
func inc() func() int {
	var j int
	return <missing code> {
		j++
		return j
	}
}
```

> func() int


#
### **Question** : Which are legal ways to implement the Go race detector at the command line with a program named main.go?

> go build -race main.go

> go run -race main.go


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

> go myfunc(&wg, i)


#
### **Question** : Which are three methods used to implement WaitGroups in goroutines?

> Add()

> Done()

> Wait()


#
### **Question** : Complete the code snippet in order to avoid race condition.

```go
func main() {
	runtime.GOMAXPROCS(runtime.NumCPU())

	var counter uint64
	var wg sync.WaitGroup
	var mu sync.Mutex

	inc := func() {
		mu.Lock()
		<missing code>
		for i := 0; i < 1000; i++ {
			counter++
		}
	}

	for i := 0; i < 1000; i++ {
		wg.Add(1)
		go func() {
			defer wg.Done()
			inc()
		}()
	}
	wg.Wait()
	fmt.Println("counter: ", counter)
}
```

> defer mu.Unlock()

#
### **Question** : Which are sync primitives?

> sync.Mutex

> sync.Once

> sync.RWMutex


#
### **Question** : What causes race conditions in Go programs?

> Unsynchronized access to shared memory

#
### **Question** : Complete the code snippet to successfully implement concurrency safe incrementing using an atomic operation.

```go
func main() {
runtime.GOMAXPROCS(runtime.NumCPU())

var counter uint64
var wg sync.WaitGroup

for i := 0; i < 1000; i++ {
wg.Add(1)
go func() {
defer wg.Done()
for j := 0; j < 1000; j++ {
<missing code>
}
}()
}
wg.Wait()
fmt.Println("counter: ", counter)
}
```

> atomic.AddUint64(&counter, 1)


#
### **Question** : The code for this program experiences a race condition. What will be the final value of the variable named counter in this program?

```go
func main() {
	runtime.GOMAXPROCS(runtime.NumCPU())

	var counter int
	var wg sync.WaitGroup

	inc := func() {
		counter++
		fmt.Println("increment counter = ", counter)
	}

	dec := func() {
		counter--
		fmt.Println("decrement counter = ", counter)
	}

	for i := 0; i < 1000; i++ {
		wg.Add(1)
		go func() {
			defer wg.Done()
			inc()
		}()
	}

	for i := 0; i < 1000; i++ {
		wg.Add(1)
		go func() {
			defer wg.Done()
			dec()
		}()
	}

	wg.Wait()
	fmt.Println("final value of counter", counter)
}
```

> An int value from -1000 to 1000

