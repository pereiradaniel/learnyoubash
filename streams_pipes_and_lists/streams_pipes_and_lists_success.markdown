# Learn Bash

## STREAMS PIPES AND LISTS (Exercise 6 of 11)

 Here's the official solution in case you want to compare notes:


    #!/usr/bin/env bash
    
    $1 || echo "First parameter is false."
    
    $2 && pwd
    
    $3 && ls || echo "Third parameter is false."


# Great!

 Streams and pipes are useful to create logs and to transfer data from one
 command to another. Lists of commands give you the opportunity to change
 the result of the execution of your script.

 You are already familiar with the ls command. But what if you need to
 list all files with a specific extension in the current directory?

 Meet the grep command! The grep command prints lines matching a pattern.
 Now, using grep we can solve the problem like so:

    ls | grep .md$

 The pipeline above will print only files with .md extension.

 Learn more about grep using man grep.

 In the next exercise you will learn how to use if conditional statements.

 You have 5 challenges left.

 Type 'learnyoubash' to show the menu.

