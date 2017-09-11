# Learn Bash

## ARRAYS (Exercise 4 of 11)

 Here's the official solution in case you want to compare notes:


    #!/usr/bin/env bash
    
    epithets=(I am "${@:2:2}" and "${@:4:1}")
    
    echo "${epithets[*]}"


# Awesome!

 Now you know how to deal with arrays in Bash. They are handy for storing
 collections of data. For example, you may use arrays for saving the list
 of enabled plugins or commands which must be executed.

 In previous exercises you have learned how to get your current directory
 using the pwd command. You may want to change the current directory. You
 can do this using the cd command like so:

    cd ~/Projects/my-awesome-project

 If you try to execute this command you will change your current directory
 to ~/Projects/my-awesome-project if this directory exists.

 Run man cd to get to know more about this useful command.

 In the next exercise we will take a look at shell expansions.

