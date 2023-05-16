# GO 

## QCM - Getting Started with Go: Testing & Deploying Go Programs
<br>
<br>


### **Question** : You've created a coverage report file cover.out using the go test -coverprofile command. Which command can you use to analyze cover.out and provide a web-based graphical coverage report?

> go tool cover -html cover.out


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

> t.Errorf


#
### **Question** : Which methods called on the *testing.T object may include formatted strings in the output when reporting test failures?

> Errorf()

> Fatalf()


#
### **Question** : Which command is used on a Windows-based machine to build a Go application and write it to an executable binary named app.exe?

> go build -o app.exe


#
### **Question** : Which command is issued at the command line to use delve to debug a Go application?

> dlv debug


#
### **Question** : You are using the Heroku CLI to deploy a Go application to Heroku. Assuming that you are signed into Heroku from a terminal session, which command may be used to deploy an app named main to Heroku?

> git push heroku main


#
### **Question** : While debugging with delve, which command issued at the dlv prompt indicates the type of value a variable holds?

> whatis


#
### **Question** : Assuming that you are using cloud shell, which command creates an app engine app on Google Cloud Platform?

> gcloud app create