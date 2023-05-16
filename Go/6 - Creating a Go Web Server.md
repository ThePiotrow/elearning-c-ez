# GO 

## QCM - Getting Started with Go: Creating a Go Web Server
<br>
<br>


### **Question** : Which NET/HTTP object type(s) direct requests to the proper handler?

> ServeMux


#
### **Question** : Which NET/HTTP type does a handler wrapper function return?

> Handler


#
### **Question** : Which method contains custom handler logic in an http.Handler implementation?

> ServeHTTP


#
### **Question** : Which NET/HTTP method accepts an http.Dir object as input?

> FileServer


#
### **Question** : Which NET/HTTP method writes data to a ResponseWriter object?

> ServeFile



#
### **Question** : Which Go NET/HTTP request type is best for requesting that the server store an image file?

> POST


#
### **Question** : Which method accepts a ResponseWriter object in an http.Handler implementation?

> ServeHTTP


#
### **Question** : What is the input parameter signature for a ServeHTTP method?

> (http.ResponseWriter, *http.Request)


#
### **Question** : What are the advantages of the Go httprouter library?

> Compatible with API architectures

> High performing

> Handles errors without crashing


#
### **Question** : Assuming an httprouter object called router and a HandlerFunc function called Handler exist, which Go statement is a valid GET request?

> router.GET("url", Handler)


#
### **Question** : Which Go function returns an object that can be used as an http.ResponseWriter object?

> httptest.NewRecorder


#
### **Question** : The code that interacts directly with a database should be included in which layer of a Model-View-Controller architecture?

> Repository


#
### **Question** : Which HTTP/2 feature allows clients to get responses from the server without a request?

> Server push

