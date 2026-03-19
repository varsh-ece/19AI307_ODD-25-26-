# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program using method overloading to print student details. Create a class Student with:

- print(String name)

- print(String name, int age)

- print(String name, int age, String dept)

## AIM:
To write a Java program that demonstrates method overloading by printing student details using three versions of the `print()` method with different parameter lists.

## ALGORITHM :
1. Create a class `Student` with three overloaded static methods:
   - `print(String name)`
   - `print(String name, int age)`
   - `print(String name, int age, String dept)`
2. In the `main` method:
   - Create a `Scanner` object to read input.
   - Read a name and call `print(name)`.
   - Read a name and age, then call `print(name, age)`.
   - Read a name, age, and department, then call `print(name, age, dept)`.
3. Each method prints the student details according to the parameters provided.
4. End the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: VARSHINI  M
RegisterNumber:  212224060293
*/
```

## SOURCE CODE:
```
import java.util.*;
class Student
{
    void print(String name)
    {
        System.out.println("Name: "+name);
    }
    void print(String name,int age)
    {
        System.out.println("Name: "+name+", Age: "+age);
    }
    void print(String name,int age,String dept)
    {
        System.out.println("Name: "+name+", Age: "+age+", Dept: "+dept);
    }
}
public class main
{
    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);
        Student obj = new Student();
        String n1=sc.nextLine();
        String n2=sc.nextLine();
        int a1=sc.nextInt();
        sc.nextLine();
        String n3=sc.nextLine();
        int a2=sc.nextInt();
        sc.nextLine();
        String dept=sc.nextLine();
        obj.print(n1);
        obj.print(n2,a1);
        obj.print(n3,a2,dept);
    }
}
```

## OUTPUT:
<img width="850" height="603" alt="image" src="https://github.com/user-attachments/assets/a78d9cb1-9f34-4ec6-a285-fc784d35ee62" />


## RESULT:
The program successfully demonstrates method overloading by printing student details using three different method signatures based on the number of arguments passed.
