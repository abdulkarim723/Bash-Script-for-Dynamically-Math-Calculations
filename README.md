# Bash Script for String Math Operations and Concatenation

This script concatenates, adds, substracts, divides or multiplies the passed parameters and prints the result to the stdout. The parameters can be passed from a pipe to it. The operation is specified depending on the control option passed to the script. Float numbers are supported.

## Syntax

```
./cal.sh <option> [parameter1 parameter2 ..] 
```

## Wokflow

- Clone the script to your PC.

```
git clone https://github.com/Abdsaddik/Bash-Script-for-Dynamically-Math-Calculations.git
```
- Go inside the the cloned folder:

```
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ cd Bash-Script-for-Dynamically-Math-Calculations
```

- Add execute permissions to the user as follows:

```
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ chmod u+x calc.sh
```

## Examples

### Addition and Substraction

- In this example the scripts returns the sum of the numbers 5, 10, 15 and 5 which results 35 to the stdout

```
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ ./calc.sh -add 5 10 15 5
35
```

- The same calculations can be achieved with the option **-sum** also

```
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ ./calc.sh -sum 5 10 15 5
30
```

- To Do substraction operation, just pass minus sign before the parameter you want

```
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ ./calc.sh -sum -10 10 10
10
```

### Multiplication

Multiplication is activated by the option **-mul** as follows:

```
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ ./calc.sh -mul 2.5 -2 -3
15.0
```

This multiplies the number 2.5 by -2 and -3 anr returns the result.

### Division

Similar to multiplication, the first parameter is devided on all followed passed parameters. The option needed is **-div**. Follows is an example:

```
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ ./calc.sh -div 80 10 2 2
2.000
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ seq 3 | ./calc.sh -div
.166
```

### String Concatenation

To cacatenate strings, the option **-con** is passed to the script

```
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ ./calc.sh -con hi there ':)'
hithere:)
```

### Pipe stdout to the script

Simply, stdout can be piped to the script as follows

```
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ seq 6 | ./calc.sh -add
21
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ seq 6 | ./calc.sh -mul
720
```

### Available options

Type the following command to show which options are available

```
user@mypc:~/Bash-Script-for-Dynamically-Math-Calculations$ ./calc -h
supported parameters are:
-add            calculate the value of adding the passed parameters
-mul            calculate the value of multiplying the passed parameters
-div            divide the first parameter to the rest of parameters
-con            concatenate the passed parameters together
-h or --help    print help command
```

