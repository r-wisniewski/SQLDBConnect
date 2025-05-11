# SQL DB Connect
# Purpose
The purpose of this class is to create a context manager to handle the connection and I/O from a SQL DB
# Usage
Using the SQL DB connect class as a context manager, begin by using the following code block:
```
import SQLDBConnect

with SQLDBconnect.SQLDBconnect(usr=db_user, pwd=db_pwd, db_name=db_name, port="5432", host="127.0.0.1") as (connection, cursor):
```
Within the context manager, a user may choose to create a new table, insert into a table or drop and create a table in one go. Functions can be expanded upon to accomplish whatever a user desires. The functions included initially are meant to perform some basic functionality I found useful. 

## Loading credentials and parameters
Users may choose to use environment variables to store and then load credentials into variables which can be passed to the context manager.
```
import os

# Load sql db credentials from environment variables
db_user = os.getenv("DB_USER")
db_pwd = os.getenv("DB_PWD")
db_name = os.getenv("DB_NAME")
```

# Contact
Robin Wisniewski – [LinkedIn](https://www.linkedin.com/in/robin-wisniewski/) –  [wisniewski.ro@gmail.com](mailto:wisniewski.ro@gmail.com)
