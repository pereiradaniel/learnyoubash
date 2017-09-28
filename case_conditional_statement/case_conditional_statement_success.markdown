## CASE CONDITIONAL STATEMENT (Exercise 8 of 11)

 Here's the official solution in case you want to compare notes:


    #!/usr/bin/env bash
    
    case "$1" in
      ("jpg"|"jpeg")
        echo "It is jpeg."
      ;;
      "png")
        echo "It is png."
      ;;
      "gif")
        echo "It is gif."
      ;;
      *)
        echo "$1 is not an image!"
      ;;
    esac


# Cool!

 As you have seen, using case is much more convenient when you are
 confronted with a couple of different cases.

 In this problem you were checking extensions. But how do we actually
 access a directory or filename?

 We already know about pwd command that return full path to current
 directory. However there are also other similar commands, like basename
 and dirname.

 The basename command strips the directory and suffix from filenames such
 as:

    basename path/to/file.ext  #> file

 The dirname command strips the last component from a file name, like
 this:

    dirname /path/to/file.ext  #> path/to

 Run man basename and man dirname to learn more about these cool commands.

 In the next exercise you will take a look at loops in bash.

