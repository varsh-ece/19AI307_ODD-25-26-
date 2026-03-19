# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the index of a given element in an array

## AIM:


## ALGORITHM :
1.	Start the program.
   
2.	Import the necessary package 'java.util'
   
3. Read the element x whose index needs to be found.

4. Traverse the array from index 0 to n-1:

     If a[i] == x, print the index i and terminate the program.

5. If the loop finishes without a match, print "Element not found".

6. End the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: VARSHINI M
RegisterNumber:  212224060293
*/
```

## SOURCE CODE:
```
import java.util.*;
public class main
{
    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int[] arr=new int[n];
        for(int i=0;i<n;i++)
        {
            arr[i]=sc.nextInt();
        }
        int num=sc.nextInt();
        int index=-1;
        for(int i=0;i<n;i++)
        {
            if(arr[i]==num)
            {
                index=i;
                break;
            }
        }
        if(index==-1)
        {
            System.out.println("Element not found");
        }
        else
        {
            System.out.println(index);
        }
    }
}
```

## OUTPUT:
<img width="558" height="590" alt="image" src="https://github.com/user-attachments/assets/0d53717f-affe-4aaf-b448-35ef728bee48" />


## RESULT:
Therefore the program successfully searches the array for the given element.
