## SHELL EXPANSIONS (Exercise 5 of 11)

 Here's the official solution in case you want to compare notes:


    #!/usr/bin/env bash
    
    R=$(( ($3 + $2) * $1))
    echo project-$R/{src,dest,test}/{index,util}.js


# Nice job!

 You just output the folder structure, but actually you can easily create
 this tree in the same way. Say hello to the mkdir and touch commands.

 The mkdir command create an empty folder with a given name. The touch
 command make an empty file with a given name.

 So now, knowing about these commands, we can do something like this:

    mkdir -p project/{src,dest,test}/
    touch project/{src,dest,test}/{index,util}.js

 Above we use the -p flag with the mkdir command to make parent
 directories as needed.

