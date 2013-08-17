!/bin/bash
 Description: 
    key/value dabatase for bash, write in bash
    database store in HOME directory, so each user have 1 database
    APIS:
        $ set <key> <value>      assign value to key
        $ get <key>              get value of key
        $ del <key>              delete by key
        $ list                   list all current key/value pairs
        $ clear                  clear database

 Requirements: unix like environement without any dependencies

 Author: damphat
 Usage: 
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
