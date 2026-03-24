# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types.

## AIM:
To implement the **Abstract Factory Design Pattern** in Java by creating UI components (Buttons and Checkboxes) for two different themes—Dark and Light.  
Based on user input, the appropriate factory should generate the correct themed UI elements.

## ALGORITHM :
1. Define two interfaces:
   - `Button` with method `render()`
   - `Checkbox` with method `render()`
2. Create concrete classes for **Dark** and **Light** themes:
   - `DarkButton`, `LightButton`
   - `DarkCheckbox`, `LightCheckbox`
3. Define the `UIFactory` interface with:
   - `createButton()`
   - `createCheckbox()`
4. Create concrete factories:
   - `DarkThemeFactory` implements `UIFactory`
     - Returns dark-themed button and checkbox
   - `LightThemeFactory` implements `UIFactory`
     - Returns light-themed button and checkbox
5. In the `main` method:
   - Read the theme name from user input.
   - If theme is `"dark"` → use `DarkThemeFactory`
   - If theme is `"light"` → use `LightThemeFactory`
   - Otherwise print `"Invalid theme"` and exit.
6. Use the chosen factory to:
   - Create a button and render it.
   - Create a checkbox and render it.
7. End the program.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: VARSHINI M
RegisterNumber:  212224060293
*/
```

## SOURCE CODE:
```
import java.util.*;
interface Button
{
    void display();
}
class Dark implements Button
{
    public void display()
    {
        System.out.println("Dark Button created");
        System.out.println("Dark Checkbox created");
    }
}
class Light implements Button
{
    public void display()
    {
        System.out.println("Light Button created");
        System.out.println("Light Checkbox created");
    }
}
public class main
{
    public static void main(String[] args)
    {
        Scanner input=new Scanner(System.in);
        String s=input.nextLine();
        if(s.equals("dark"))
        {
            Dark d=new Dark();
            d.display();
        }
        else if(s.equals("light"))
        {
            Light l=new Light();
            l.display();
        }
        else
        {
            System.out.println("Invalid theme");
        }
    }
}
```
## OUTPUT:
<img width="692" height="278" alt="image" src="https://github.com/user-attachments/assets/cd0411f1-afc3-48cb-a31d-b10a027d9ae3" />


## RESULT:
The program successfully demonstrates the **Abstract Factory Pattern** by creating theme-specific UI components.  
Based on user input, the correct factory is selected, and it generates:

- A *Dark Button* and *Dark Checkbox* **or**
- A *Light Button* and *Light Checkbox*

Both components are rendered in the output according to the selected theme.
