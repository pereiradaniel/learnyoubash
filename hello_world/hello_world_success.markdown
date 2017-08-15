# Learn Bash

## HELLO WORLD (Exercise 1 of 11)

 Here's the official solution in case you want to compare notes:


    #!/usr/bin/env bash
    
    echo "Hello, world!"


# You did it!

 Congratulations! You wrote your first bash script! Quite simple, isn't
 it?

 By the way, pay your attention to whoami command. This command prints
 your username. That means you can do something like this:

    #!/usr/bin/env bash
    
    echo "Hello, $(whoami)!"

 This script will greet you personally.

 Besides, if you have problems with any command, you always can read the
 manual about the command using the man command. This command works well
 with any Unix command and will be your handy guide in Bash world. For
 example:

    man pwd

 Additionally, almost every command has a --help flag, which shows a
 simple how-to message for you. Use this flag like this:

    pwd --help

 In the next exercise we will take a look at variables.

 You have 10 challenges left.

 Type 'learnyoubash' to show the menu.

