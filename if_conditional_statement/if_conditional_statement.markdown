F CONDITIONAL STATEMENT (Exercise 7 of 11)  
   
  Like in other languages, Bash conditionals let us decide whether to  
  perform an action or not.  The result is determined by evaluating an  
  expression, which should be enclosed in [[ ]].  
   
  Conditional expression may contain && and || operators, which are AND and  
  OR respectively. Beside this, there are many [other handy  
  expressions](https://github.com/denysdovhan/bash-handbook#primary-and-comb  
  ining-expressions).  
   
  Before we start, let's see what primaries are.  
   
 ### Primary and combining expressions  
   
  Expressions enclosed inside [[ ]] (or [ ] for sh) are called test commands  
  or primaries. These expressions help us to indicate results of a  
  conditional. In the tables below, we are using [ ], because it works for  
  sh too. Here is an answer about [the difference between double and single  
  square brackets in bash](http://serverfault.com/a/52050).  
   
  Working with the file system:  
   
       Primary       Meaning  
 ------------------- ---------------------------------------  
     [ -e FILE ]     True if FILE exists.  
     [ -d FILE ]     True if FILE exists and is a directory.  
     [ -r FILE ]     True if FILE exists and is readable.  
     [ -w FILE ]     True if FILE exists and is writable.  
     [ -x FILE ]     True if FILE exists and is executable.  
 [ FILE1 -nt FILE2 ] FILE1 is newer than FILE2.  
 [ FILE1 -ot FILE2 ] FILE1 is older than FILE2.  
   
  Working with strings:  
   
      Primary     Meaning  
 ---------------- ------------------------------------------  
    [ -z STR ]    STR is empty (the length is zero).  
    [ -n STR ]    STR is not empty (the length is non-zero).  
 [ STR1 == STR2 ] STR1 and STR2 are equal.  
 [ STR1 != STR2 ] STR1 and STR2 are not equal.  
   
  Arithmetic binary operators:  
   
      Primary      Meaning  
 ----------------- -----------------------------------  
 [ ARG1 -eq ARG2 ] ARG1 is equal to ARG2.  
 [ ARG1 -ne ARG2 ] ARG1 is not equal to ARG2.  
 [ ARG1 -lt ARG2 ] ARG1 is less than ARG2.  
 [ ARG1 -le ARG2 ] ARG1 is less than or equal to ARG2.  
 [ ARG1 -gt ARG2 ] ARG1 is greater than ARG2.  
 [ ARG1 -ge ARG2 ] ARG1 is greater or equal to ARG2.  
   
  Conditions may be combined using these combining expressions:  
   
      Operation     Effect  
 ------------------ ----------------------------------------------  
     [ ! EXPR ]     True if EXPR is false.  
     [ (EXPR) ]     Returns the value of EXPR.  
 [ EXPR1 -a EXPR2 ] Logical AND. True if EXPR1 and EXPR2 are true.  
 [ EXPR1 -o EXPR2 ] Logical OR. True if EXPR1 or EXPR2 are true.  
   
  Of course, there are more useful primaries and you can easily find them in  
  the [Bash man  
  pages](http://www.gnu.org/software/bash/manual/html_node/Bash-Conditional-  
  Expressions.html)  
   
 ### Using an if statement  
   
  if statements work the same as in other programming languages. If the  
  expression within the braces is true, the code between then and fi is  
  executed. fi indicates the end of the conditionally executed code.  
   
     # Single-line  
     if [[ 1 -eq 1 ]]; then echo "true"; fi  
       
     # Multi-line  
     if [[ 1 -eq 1 ]]; then  
       echo "true"  
     fi  
   
  Likewise, we could use an if..else statement such as:  
   
     # Single-line  
     if [[ 2 -ne 1 ]]; then echo "true"; else echo "false"; fi  
       
     # Multi-line  
     if [[ 2 -ne 1 ]]; then  
       echo "true"  
     else  
       echo "false"  
     fi  
   
  Sometimes if..else statements are not enough to do what we want to do. In  
  this case we shouldn't forget about the existence of if..elif..else  
  statements, which always come in handy.  
   
  Look at the example below:  
   
     if [[ `uname` == "Adam" ]]; then  
       echo "Do not eat an apple!"  
     elif [[ `uname` == "Eva" ]]; then  
       echo "Do not take an apple!"  
     else  
       echo "Apples are delicious!"  
     fi  
   
 ## THE CHALLENGE  
   
  Create a file named if.bash.  
   
  Using if statements and primaries, output Good morning! if the first  
  positional parameter is less than 12. Output Good afternoon! if it is  
  equal to/greater than 12 but less than 18. Otherwise, output Good evening!  
  if it is equal to/greater than 18. Take care about cases when the  
  positional argument is less than 0 and greater than 24 (print Error! in  
  these cases).  
   
  For example:  
   
     ./if.bash -5  
     ./if.bash 12  
     ./if.bash 21  
   
  Output:  
   
     Error!  
     Good afternoon!  
     Good evening!  

