# GO 

## QCM - Getting Started with Go: Concurrency
<br>
<br>


### **Question** : Which are problems attributed to sequential programming technique?

> Most real-world scenarios not sequential

> Cannot handle multiple events


#
### **Question** : Multithreaded processes are implemented as which two types of threads?

> Kernel-level threads

> User-level threads


#
### **Question** : Which type of confinement sees each stage of a pipeline avoid accessing a confined variable or field after it has sent it on to the next stage?

> Serial


#
### **Question** : Which statements accurately describe concurrency and parallelism?

> Parallelism supports multiple actions executing at the same time

> Concurrency only supports progress of multiple tasks simultaneously


#
### **Question** : Which function from the WaitGroup type does the main goroutine call to tell Go the number of goroutines to wait for?

> Add()


#
### **Question** : What is the initial stack size of a Goroutine?

> 2 KB


#
### **Question** : Which concurrency level makes explicit use of atomic operations?

> Low-level concurrency


#
### **Question** : Which pattern can be used when we need to combine multiple done channels into a single done channel?

> Or-channel pattern


#
### **Question** : Which statement initializes a variable named ‘cores’ to the number of CPU cores on a device?

> cores := runtime.NumCPU()