LOOPING
Syntax:
do
statements
done
The while loop executes the statements as long as the condition remains true.
while [ condition ] do
statements
done
Armstrong Number Algorithm
Step 1 : Start
Step 2 : Read number
Step 3 : Initialize 0 to sum and number to num
Step 4 : Extract last digit by computing number modulo 10 Step 5 : Cube the lastdigitand add it to sum
Step 6 : Divide number by 10
Step 7: Repeat steps 4–6 until number > 0
Step 8 : If sum = number then Print “Armstrong number” Step 8.1 : else Print “Not an Armstrong number” Step 9 : Stop Program (armstrong.sh)
# Armstrong number using while loop echo -n "Enter a number : "
read n a=$n s=0 while [ $n -gt 0 ] do r=`expr $n % 10`
s=`expr $s + \( $r \* $r \* $r \)` n=`expr $n / 10` done
if [ $a -eq $s ] then
echo "Armstrong Number" else
echo -n "Not an Armstrong number" fi
OUTPUT:
[student@krce ~]$ sh armstrong.sh Enter a
number:370 Armstrong Number
