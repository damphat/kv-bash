**About db-bash**

 - key/value dabatase for bash script
 - database store in HOME directory
 - each user has 1 database

**Requirements**

unix-like environement, no dependencies

**Usage**
```
$ source db-bash         # import db-bash functions
$ set <key> <value>      # create or change value of key
$ get <key>              # get value of key
$ del <key>              # delete by key
$ list                   # list all current key/value pairs
$ clear                  # clear database
```
**Examples**
``` 
$ source db-bash
$ set user damphat
$ set pass abc@123
$ list
user damphat
pass abc@123
$ get user
damphat
$ get pass
abc@123
$ del pass
$ get pass

$ clear
```