---

title: How to check in Java whether a Triangle is right-angled or not?
description: A simple program in Java to check whether a triangle is right-angled or not.

---

- Written by Mayank Vikash
- Published on 21st October 2022
- Last Updated Oct 21, 2022

A right-angled triangle is a triangle with one of its interior angles equal to 90 degrees or any one angle is a right angle.

There are several properties of a right-angled triangle; one of them is that the square of the hypotenuse is equal to the sum of the square of the perpendicular and base of a triangle. This is called the Pythagoras Theorem.

The hypotenuse is the longest side of a triangle.

Fun Fact: Pythagoras’s Theorem was invented in India, long before Pythagoras was even born.

The theorem is mentioned in the Baudhayana Sulba-sutra of India, which was written between 800 and 400 BCE.

## Program’s Logic

According to the theorem, the squared of Hypotenuse is equal to the sum of the squared of the other two sides. So, we have to take the input of the two sides of a triangle and a hypotenuse. Calculate the sum of squares of the other two sides and if the sum is equal to the square of the hypotenuse, the triangle is right-angled.

Program’s Screenshot

![Screenshot of the program](https://mayankvikash.in/posts/How-to-check-in-Java-whether-a-Triangle-is-right-angled-or-not/right-angled-triangle-program-screenshot.webp)

Screenshot of the program

## Let’s write the program

Basic program structure.

```java
import java.util*;
public class RightAngledTriangle{
  public static void main(String args[]){
    Scanner in = new Scanner(System.in);
    // code
  }
}

```

Declaring variables.

```java
int h, p, b;

```

Asking the user for input.

```java
System.out.println("Enter the Hypotenuse");
h = in.nextInt();
System.out.println("Enter the Perpendicular");
p = in.nextInt();
System.out.println("Enter the Base");
b = in.nextInt();

```

The simple way to check if the squared of the hypotenuse is equal to the sum of the squared of the perpendicular and base is to use if-else.

If-else condition.

```java
if (h*h==(p*p)+(b*b)){
    System.out.println("Right Angled Triangle");
}
else{
    System.out.println("Not a right angled Traingle");
}

```

## Code

```java
import java.util.*;
public class RightAngledTriangle {

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int h, p, b;
        System.out.println("Enter the Hypotenuse");
        h = in.nextInt();
        System.out.println("Enter the Perpendicular");
        p = in.nextInt();
        System.out.println("Enter the Base");
        b = in.nextInt();

        if (h*h==(p*p)+(b*b)){
            System.out.println("Right Angled Triangle");
        }
        else{
            System.out.println("Not a right angled Traingle");
        }

    }
}

```

## Output

![Not a right-angled triangle output screenshot](https://mayankvikash.in/posts/How-to-check-in-Java-whether-a-Triangle-is-right-angled-or-not/right-angled-triangle-output-not-a-right-angled-triangle-screenshot.webp)

![Right-angled triangle output screenshot](https://mayankvikash.in/posts/How-to-check-in-Java-whether-a-Triangle-is-right-angled-or-not/Right-Angled-Triangle-command-line-output-screenshot.webp)
