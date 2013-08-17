**About kv-bash**

 - key/value dabatase for bash script
 - database store in HOME directory
 - each user has 1 database

**Requirements**

unix-like environement, no dependencies

**Usage**
```
$ source ./kv-bash         # import kv-bash functions
$ kvset <key> <value>      # create or change value of key
$ kvget <key>              # get value of key
$ kvdel <key>              # delete by key
$ kvlist                   # list all current key/value pairs
$ kvclear                  # clear database
```
**Examples**
``` 
$ source ./kv-bash
$ kvset user damphat
$ kvset pass abc@123
$ kvlist
user damphat
pass abc@123
$ kvget user
damphat
$ kvget pass
abc@123
$ kvdel pass
$ kvget pass

$ kvclear
```
