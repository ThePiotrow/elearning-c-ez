# GO 

## QCM - Getting Started with Go: Error & File Handling
<br>
<br>


### **Question**: Complete the if statement that would result in the err value being printed to the terminal if the file named "myFile.txt" does not exist.

```go
func main() {

    // signature: func Open(name string) (file *File, err error)
    f, err := os.Open("myFile.txt")
    defer f.Close()
    if <missing code> {
        log.Println(err)
        return
    }
    fmt.Println("file successfully opened:", f.Name())
}
```

> err != nil



#
### **Question** : You are writing a Go program to read the files and folders in a directory. Complete the code snippet that would result in reading and printing each directory listing's name and whether it is a directory.

```go	
// ReadDir List files
func main() {
	// formerly ioutil.ReadDir()
	// func ReadDir(name string) ([]DirEntry, error)
	<missing code> := os.ReadDir("../demo")
	if err != nil {
		log.Fatal(err)
	}
	for _, f := range ls {
		fmt.Println(f.Name(), f.IsDir())
	}
}
```

> ls, err


#
### **Question** : Given that the signature for Go's built-in panic() function is func panic(v interface{}), what types of values can be passed to panic()?

> Any data type


#
### **Question** : Assuming "myFile.txt" does not exist, which function from package os may be used in the code snippet to complete the inner if statement, causing the program to output "file does not exist"?

```go
func main() {

    if _, err := os.Open("myFile.txt"); err != nil {
        if errors.<missing code>(err, os.ErrNotExist) {
            log.Println("file does not exist")
	  } else {
		log.Println(err)
	  }
	  return
    }
    fmt.Println("file successfully opened")
}
```

> Is


#
### **Question** : Which statements accurately describe error handling in Go?


> Functions may return error values

> Errors in Go are simple values


#
### **Question** : What type of runtime error occurs when a program attempts to access memory that it is not allowed to?


> Segmentation fault



#
### **Question** : Assuming "file.txt" exists, complete the code snippet that would result in file.txt being read line by line.


```go 
func main() {

	f, err := os.Open("file.txt")
	defer f.Close()
	if err != nil {
		log.Fatal(err)
	}

	// func NewScanner(r io.Reader) *Scanner
	s := bufio.NewScanner(f)
	for <missing code> {

		fmt.Println(s.Text())
	}

	if err := s.Err(); err != nil {

		log.Fatal(err)
	}

}
```

> s.Scan()

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

> os.Stat


#
### **Question** : What is the signature of the ReadFile function from package os?


> func ReadFile(name string) ([]byte, error)


#
### **Question** : What is the signature of the New() function from package errors?


> func New(text string) error