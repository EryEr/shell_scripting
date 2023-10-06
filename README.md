# shell_scripting
Basic Shell Scripting<br>
Open a shell terminal and try the commands below.<br><be>

**Comparison Operators**<br>
**For numerical values**<br>
`-eq`: equal<br>
`-ne`: not equal<br>
`-gt`: greater than<br>
`-ge`: greater or equal<br>
`-lt`: less than<br>
`-le`: less of equal<br>
<br>
**for string values**<br>
<br>
`=`: equals<br>
`!`=: not equal<br>
`<`: less than (in alphabetical order)<br>
`>`: greater than (in alphabetical order)<br>
<br>
**Logical Operators**:<br>
`!`: NOT<br>
`-a`: AND<br>
`-o`: OR<br>
<br>
<be>
**Example** <br>
`if [ "$a" -eq "$b" ]; then`<br>
    `echo "a is equal to b"`<br>
`fi`<br>
<br>
`if [ "$a" != "$b" ]; then`<br>
    `echo "a is not equal to b"`<br>
`fi`<br>
<br>
`if [ "$a" -lt "$b" -a "$c" -gt "$d" ]; then`<br>
    `echo "a is less than b AND c is greater than d"`<br>
`fi`<br>
<br>
<br>

**File Comparisons**:<br>
There are also operators in Bash to gather information about files.<br>
<br>
`-e`: Does the file exist?<br>
`-f`: Is it a regular file?<br>
`-d`: Is it a directory?<br>
`-s`: Is the file empty?<br>
`-r`: Is the file readable?<br>
`-w`: Is the file writable?<br>
`-x`: Is the file executable?<br>
<br>
**Example** <br>
`if [ -e "/path/to/file" ]; then`<br>
    `echo "File exists"`<br>
`fi`<br>
<br>




**Using Variables**<br><br>
<img width="653" alt="Screenshot 2023-08-04 at 23 34 29" src="https://github.com/EryEr/shell_scripting/assets/138815393/71bc2dd3-c1e2-44f5-9645-93e8cf84040c"><br><br>

```
#!/bin/bash

# Example script to check if a number is multiple of 3, multiple of 5, or multiple of 15.
name="Ben"
echo "My name is " $name

if [ -z "$1" ]; then
  echo "Enter a number, please:"
  exit 1
fi

number=$1

if [ $((number % 3)) -eq 0 ] && [ $((number % 5)) -eq 0 ]; then
  echo "$number, is multiple of 15."
elif [ $((number % 3)) -eq 0 ]; then
  echo "$number, is multiple of 3."
elif [ $((number % 5)) -eq 0 ]; then
  echo "$number, is multiple of 5."
else
  echo "$number, is not a multiple of 3 or 5."
fi
```
<br><br>
need to call this script like the below in the terminal.<br><br>
<br>
<img width="542" alt="Screenshot 2023-08-05 at 00 34 36" src="https://github.com/EryEr/shell_scripting/assets/138815393/9d5b084e-0454-4f22-92a7-632d32377e83"><br><br>

`bash script_name.sh number_to_check`<br>
<img width="263" alt="Screenshot 2023-08-05 at 00 37 27" src="https://github.com/EryEr/shell_scripting/assets/138815393/831b3b7e-0fce-4b10-a620-8886eb80f1ea"><br>


