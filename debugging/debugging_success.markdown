## DEBUGGING (Exercise 11 of 11)

 Here's the official solution in case you want to compare notes:


    #!/usr/bin/env bash
    
    set -vn
    echo $@
    touch $@
    mkdir ./folder
    mv file* ./folder
    cd ./folder
    ls
    set +vn


# You are awesome!

 You've finished all of the exercises! That means you are awesome!

 You learned what Bash is and how to write your first script. But, to be
 honest, that doesn't mean that you completely mastered Bash. There are a
 lot of other things you still have to learn.

 Here's a small list of other literature covering Bash:

  » [bash-handbook](https://github.com/denysdovhan/bash-handbook) is a                                                                         
    handbook which was used to build this workshopper.                       
  » Bash man page. In many environments that you can run Bash, the help                                                                         
    system man can display information about Bash, by running the command                                                                         
    man bash.                                                                
  » ["Bourne-Again SHell                                                                         
    manual"](https://www.gnu.org/software/bash/manual/) in many formats,                                                                         
    including HTML, Info, TeX, PDF, and Texinfo.  Hosted at                                                                         
    <https://www.gnu.org/>. As of 2016/01, this covers version 4.3, last                                                                         
    updated 2015/02/02.                                                      
  » [Bash 3.2 Man                                                                         
    page](https://developer.apple.com/library/mac/documentation/Darwin/Ref   
    erence/ManPages/man1/bash.1.html) hosted at Apple's Mac Developer                                                                         
    Library site. As of 2016/01, this covers version 3.2, last updated                                                                         
    2006/09/28. 
