# GO 

## QCM - Go Web Programming Literacy (Beginner Level)
<br>
<br>


### **Question**: Which Go library allows you to read the body of a response as a collection of bytes?

> `io/ioutil`


#
### **Question** : Which are the best practice(s) for writing code in Go?

> `Utilize commenting`

> `Avoid excessive nesting`

> `Resist repetition`

> `Ensure maintainability`


#
### **Question** : A http.Handler object is wrapped by Handler wrappers in the following order: Wrapper A, Wrapper B, Wrapper C. Wrapper A and Wrapper C call the ServeHTTP method of their input http.Handler object, but Wrapper B does not.
### Which combination represents the order of execution of the wrappers when the ServeHTTP method is called on the wrapped object?

> `Wrapper C, Wrapper B`


#
### **Question** : Which method contains custom handler logic in an http.Handler implementation?

> `ServeHTTP`


#
### **Question** : What are the advantages of the Go httprouter library?

> `Compatible with API architectures`

> `High performing`

> `Handles errors without crashing`


#
### **Question** : Match the Go ResponseWriter methods to their descriptions. Go ResponseWriter methods may be used more than once.

<br>

Write: 
> May determine content type based on 512 bytes

> `Writes to the response content body`

WriteHeader:
> Sets the status code to 200 OK by default

Header: 
> Writes any header value to the response


#
### **Question** :  What are the characteristic(s) of JSON data encoding in Go?

> `Keys must be strings`

> `Function types cannot be encoded`


#
### **Question** : Which template engine feature allows dynamic template content to be translated differently as HTML or JavaScript?

> `Context sensitivity`


#
### **Question** : Which Go template range action are grammatically correct?

> `{{ range $a := . }}`


#
### **Question** : What are the characteristics of the built-in template functions in Go?

> `Can be used as arguments`

> `Predefined by Go`


#
### **Question** : Which Go method translates binary data to struct data?

> `Decode`


#
### **Question** : Which Go method copies query results to a struct?

> `Scan`


#
### **Question** : Which Go method sets the status of an HTTP response?

> `WriteHeader`


#
### **Question** : In Go, which statement will convert JSON, called jsonData, to a struct instance called instance?

> `json.Unmarshal(jsonData, &instance)`


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