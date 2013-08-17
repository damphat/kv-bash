**About kv-bash**
 - language bash script
 - key/value dabatase
 - database store in HOME directory
 - each user has 1 database
 - 1 bash file, that contain 5 APIs
 
**Requirements**

unix-like environement, no dependencies

**Usage**

import all database functions

```
$ source ./kv-bash         # import kv-bash functions
```

no need to create database, just use the default one

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

**Run tests**

```
git clone https://github.com/damphat/kv-bash.git
cd kv-bash
./kv-test
```

Result should be:
```
RUN ALL TEST CASES:
===================
  1 get unset var should return empty                 [  OK  ]
  2 set then get a variable                           [  OK  ]
  3 set again with different value                    [  OK  ]
  4 del variable should be empty                      [  OK  ]
  5 del non existing valriable is no-error            [  OK  ]
  6 set without param return error                    [  OK  ]
  7 get without param return error                    [  OK  ]
  8 del without param return error                    [  OK  ]
  9 set 3 keys/value; list => line count = 3          [  OK  ]
 10 clear => line count = 0                           [  OK  ]
 11 empty value => error code != 0                    [  OK  ]
```