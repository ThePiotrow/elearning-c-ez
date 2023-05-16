# GO 

## QCM - Getting Started with Go: HTML Forms & ResponseWriter in Go
<br>
<br>


### **Question** : Which Go method(s) can be used to set the content type of an HTTP response?

> `ResponseWriter.Header().Set`

> `ResponseWriter.WriteHeader`


#
### **Question** : What is the name of the HTTP header used to request a specific content type from the server?

> `Accept`


#
### **Question** : Match the Go ResponseWriter methods to their descriptions. Go ResponseWriter methods may be used more than once.

<br>

Write: 
> `May determine content type based on 512 bytes`

> `Writes to the response content body`

WriteHeader:
> `Sets the status code to 200 OK by default`

Header: 
> `Writes any header value to the response`


#
### **Question** : Which Go method(s) can be used to write a HTTP response’s content type?

> `ResponseWriter.Header`


#
### **Question** :  What are the characteristic(s) of JSON data encoding in Go?

> `Keys must be strings`

> `Function types cannot be encoded`


#
### **Question** : Which Go method defines custom JSON marshaling for a struct?

> `MarshalJSON`


#
### **Question** : Which Go method returns two maps?

> `ResponseWriter.ParseMultipartForm`


#
### **Question** : Which net/http Go library attribute(s) give information about name/value pairs from the request’s content body?

> `Form`

> `PostForm`

> `MultipartForm`