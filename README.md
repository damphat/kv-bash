kv-bash [![Build Status](https://travis-ci.org/damphat/kv-bash.png?branch=master)](https://travis-ci.org/damphat/kv-bash)
=====================
**About**
 - tiny key/value dabatase
 - database store in home directory
 - each user has 1 database
 - usage by importing 5 bash functions via ```$ source ./kv-bash```
 
**Requirements**

unix-like environement, no dependencies

**Usage**

import all database functions

```
$ source ./kv-bash         # import kv-bash functions
```

use database functions

```
$ kvset <key> <value>      # create or change value of key
$ kvget <key>              # get value of key
$ kvdel <key>              # delete by key
$ kvlist                   # list all current key/value pairs
$ kvclear                  # clear database
```

**Examples**

``` 
$ source ./kv-bash
$ kvset user mr.bob
$ kvset pass abc@123
$ kvlist
user mr.bob
pass abc@123
$ kvget user
mr.bob
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

test result

```
RUN ALL TEST CASES:
===================
  1 call kvget for non-exist key should return empty  [  OK  ]
  2 kvset then kvget a variable                       [  OK  ]
  3 kvset then kvset again with different value       [  OK  ]
  4 deleted variable should be empty                  [  OK  ]
  5 kvdel non exist should be OK                      [  OK  ]
  6 kvset without param return error                  [  OK  ]
  7 kvget without param return error                  [  OK  ]
  8 kvdel without param return error                  [  OK  ]
  9 kvset 3 keys/value; kvlist => line count = 3      [  OK  ]
 10 non-exist-var => empty value => line count = 1    [  OK  ]
 11 kvclear; kvlist => line count = 0                 [  OK  ]
 12 kvget return empty value => error code != 0       [  OK  ]
 13 spaces in value                                   [  OK  ]
```
