# GO 

## QCM - Getting Started with Go: Working with Templates in Go
<br>
<br>


### **Question** : Which template engine feature allows dynamic template content to be translated differently as HTML or JavaScript?

> `Context sensitivity`


#
### **Question** : What is the scope of a variable in a Go template?

> `The enclosing action`


#
### **Question** : What are the characteristics of the built-in template functions in Go?

> `Can be used as arguments`

> `Predefined by Go`


#
### **Question** : A Go program parses a command-line flag called message and stores it in a variable called msgFlag.
### Which command-line command will populate the msgFlag variable with the string “Hello world”?

> `go run . -message “Hello world”`


#
### **Question** : Match the Go features with their characteristics.

Arguments:
> `Automatically indirects pointers`

Variables:
> `Can represent the current element of a range`

Pipelines:
> `Outputs two values`


#
### **Question** : A Go template contains the following custom functions: rev that reverses a string, rem3 that removes the first three characters of a string, and addq that adds the letter ‘q’ to the end of a string.
### If $string contains the string “Hello world”, which pipeline command would resolve to the string “row olleH”?

> `{{ $string | addq | rev | rem3 }}`


#
### **Question** : Match the Go template actions with their descriptions.

Conditional:
> `Evaluates one of several code blocks`

Iterator:
> `Applies the dot value to multiple elements`

Set: 
> `Sets the dot value for a section of code`

Include:
> `Allows template nesting`


#
### **Question** : What are the characteristics of custom template functions in Go?

> `Defined in a FuncMap`

> `May have two output values`

> `Can be used as arguments`


#
### **Question** : Which Go template activity would be best for displaying the rows of a table if the number of rows were unknown until run-time?

> `Loop`


#
### **Question** : Which Go template range action are grammatically correct?

> `{{ range $a := . }}`


#
### **Question** : Which Go method combines a template with its model data?

> `Execute`


#
### **Question** : What are the limitations of command-line arguments in Go?

> `They are order-sensitive`

> `Your code must know how many there are`
