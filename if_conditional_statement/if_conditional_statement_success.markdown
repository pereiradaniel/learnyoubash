## IF CONDITIONAL STATEMENT (Exercise 7 of 11)

 Here's the official solution in case you want to compare notes:


    #!/usr/bin/env bash
    
    if [[ $1 -ge 0 && $1 -lt 12 ]]; then
      echo "Good morning!"
    elif [[ $1 -ge 12 && $1 -lt 18 ]]; then
      echo "Good afternoon!"
    elif [[ $1 -ge 18 && $1 -lt 24 ]]; then
      echo "Good evening!"
    else
      echo "Error!"
    fi


# Neat!

 You have made a simple script that greets us depending on the current
 time. But how can we get the current time?

 For those purposes we can use the date command that prints or sets the
 system date and time. So using this command we might solve this problem
 like this:

    # Get current hour
    HOUR=$(date +%H)
    
    if [[ $HOUR -lt 12 ]]; then
      echo "Good morning!"
    elif [[ $HOUR -ge 12 && $HOUR -lt 18 ]]; then
      echo "Good afternoon!"
    else
      echo "Good evening!"
    fi

 The +%H means that we want to output only the current hour in 00..23
 format. Use man date to find out more about the date command.

 In the next exercise you will master case conditional statements.

