# Learn Bash

## VARIABLES (Exercise 2 of 11)

 Here's the official solution in case you want to compare notes:


    #!/usr/bin/env bash
    
    echo "User $USER in directory $PWD."


# Awesome!

 Okay, you've done this!

 Variables are a very important part of any programming language and now
 you know how they work in Bash.

 In this exercise you used the $PWD variable. In addition, there is also
 the pwd command which returns the same thing as the $PWD variable, the
 present working directory. So remember, when you need to get the current
 directory name, use either the pwd command or the $PWD variable:

    pwd        #> /Users/username/learnyoubash/variables/
    echo $PWD  #> /Users/username/learnyoubash/variables/

 Above you may notice special strings which start with the # sign. Do you
 know what they are? They're comments.

 Comments are special statements ignored by the shell interpreter. They
 begin with a # symbol and continue on to the end of the line.

 For example:

    #!/bin/bash
    # This script will print your username.
    whoami

 Use comments to explain what your script does and why.

 In the next exercise we will use positional parameters. We will learn how
 to handle the arguments which may be passed to your program.

 You have 9 challenges left.

 Type 'learnyoubash' to show the menu.

