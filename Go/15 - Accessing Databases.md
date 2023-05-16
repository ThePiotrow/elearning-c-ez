# GO 

## QCM - Getting Started with Go: Accessing Databases
<br>
<br>


### **Question** : On the MySQL installer window service page, which options are available for configuring MySQL server?

> Start the MySQL server at system start-up

> Configure MySQL server as a Windows service


#
### **Question** : Which method should normally be used when performing a data manipulation operation in Go?

> Exec()


#
### **Question** : Complete the statement to generate a prepared statement to be used in a SQL query in Go against a MySQL database.

> stmt, err := db.Prepare("INSERT INTO employees(name) VALUES(?)")


#
### **Question** : Which variable type can be used to handle a varchar database column that is nullable?

> sql.NullString


#
### **Question** : Which are methods used on a transaction type (*sql.Tx) in Go?

> Rollback()

> Commit()

> Begin()


#
### **Question** : Which command successfully installs the MySQL database driver?

> go get -u github.com/go-sql-driver/mysql


#
### **Question** : You are using MySQL Workbench for the first time after installation. Since you have not added any schemas to the MySQL server, which database or schema appears in the SCHEMAS pane in MySQL Workbench?

> sys


#
### **Question** : Which statement correctly imports the MySQL database driver for Go?

> import _ "github.com/go-sql-driver/mysql"


#
### **Question** : How many rows may be returned using the QueryRow() method?

> 1 row

> 0 rows