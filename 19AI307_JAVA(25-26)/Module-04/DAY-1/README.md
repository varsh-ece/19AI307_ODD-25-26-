# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?


## AIM:
To read a string input from the user, convert it to uppercase, and handle the situation where the string is null using exception handling.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Start the program
Create a Scanner object to read input
Read a string s from the user
Check if the input string is "null"
If yes, assign s = null (actual null value, not text)
Use a try block:
Attempt to convert the string to uppercase using s.toUpperCase()
Print the result
Use a catch block:
Catch NullPointerException
Print "Null element"
End the program





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: VARSHINI M
RegisterNumber:  212224060293
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        String s=sc.nextLine();
        if(s.equals("null"))
        {
            s=null;
        }
        try
        {
            System.out.print(s.toUpperCase());
            
        }
        catch(NullPointerException e)
        {
        System.out.print("Null element");
        }
    }
}
```





## OUTPUT:
<img width="734" height="255" alt="image" src="https://github.com/user-attachments/assets/1c01ab31-d588-4002-a812-37d97f7c89b2" />



## RESULT:

Thus, the program demonstrates handling of null values using exception handling while performing string operations.
