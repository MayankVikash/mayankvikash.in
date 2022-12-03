---
title: An easy approach to check in Java whether a number is Automorphic or not

description: Java program to check whether a number is Automorphic or not.

cover: https://mayankvikash.in/posts/an-easy-approach-to-check-in-java-whether-a-number-is-automorphic-or-not/Automorphic-number-in-java.webp

---
![Automorphic Number in Java Cover](https://mayankvikash.in/posts/an-easy-approach-to-check-in-java-whether-a-number-is-automorphic-or-not/Automorphic-number-in-java.webp)

There are several articles on "how to check in Java whether a number is Automorphic or not?" which you can find on the Internet including some from popular websites like GeeksforGeeks and JavaTpoint. But they all have a similar problem. They are not beginners friendly.


In this article, I will show you a beginner-friendly approach to find whether a number is Automorphic or not in Java.


## What is an Automorphic Number?

An Automorphic Number is a number whose square has the exact number as its last digit. For example, 25 which is the square of 5 contains 5 as its last digit. An example of a two-digit number is 5776 which is the square of 76 and ends with 76. Some other examples are 625 which is the square of 25 and ends with 25.

## Approach to Solve the Program

Let's take a look at the easy approach to solving the problem first.

*   Input number from the user
    
*   Assign it to another variable (here the variable is p)
    
*   Store the square of the number in a variable (here sq)
    
*   With a loop check if the last digits of both numbers are the same or not
    
*   Whether the last digits are the same or not can be checked with a simple condition `(n % 10 == sq % 10)`
    
*   With the help of a counter variable (here c) take a record of how many last digits are similar
    
*   Outside the loop, check with an if-else condition whether the counter variable is greater than 0 or not (counter variable c is initialized 0).
    

![Screenshot of the Automorphic Number Program in Java](https://mayankvikash.in/posts/an-easy-approach-to-check-in-java-whether-a-number-is-automorphic-or-not/automorphic-number-screenshot-of-the-code.webp)

## Code

```java
import java.util.Scanner;
class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int i, n, sq, c=0;
        
       System.out.println("Enter a number to check for Automorphic Number");
                n = in.nextInt();
                sq = n * n;

                for (i = n; n > 0; n = n / 10) {
                    if (n % 10 == sq % 10)
                        c++;
                    sq = sq / 10;

                }

                if (c > 0)
                    System.out.println("Automorphic Number");
                else
                    System.out.println("Not an Automorphic Number");
    }
}
```

### Got a problem with For Loop? Here it is solved with While Loop

```java
import java.util.Scanner;
class Main
{
  public static void main (String[]args)
  {
    Scanner in = new Scanner (System.in);
    int n, sq, p, c = 0;

      System.out.println ("Enter a number to check for Automorphic Number");
      n = in.nextInt();
      p = n;
      sq = n * n;

    while (n > 0)
      {
	if (n % 10 == sq % 10)
	  c++;
	n = n / 10;
	sq = sq / 10;

      }

    if (c > 0)
        System.out.println ("Automorphic Number");
    else
      System.out.println ("Not an Automorphic Number");
  }
}
```

## Code Explanation

The program is simple. We just have to check if the last digits of a number's square are equal to the number or not.

I have taken five variables:

*   i - this variable is kind of useless
    
*   n - to store the number input by the user
    
*   sq - to store the square of the number
    
*   p - to store the number for verification at last as the variable n will become 0 after the control exits from the loop
    
*   c - it is a counter variable used here to check whether the number comes at the end of its square or not
    

for (i = n; n &gt; 0; n = n / 10) { if (n % 10 == sq % 10) c++; sq = sq / 10;

The For Loop condition 'i=n' can be replaced with a semi-colon (;).

```java
for (; n > 0; n = n / 10)
```

The condition inside the for loop is used to check whether the last digit of the variable n is equal to the last digit of variable sq or not. At the last of the loop, both the variables sq and n are divided by 10.

In While Loop, n = n / 10 is at the last with sq = sq / 10.

This loop continues till the value of n becomes 0. This is why previously the value of n is stored in the variable p.

Edit: **There is no need for the variable p**.

If the last digit of both the variables is the same, the counter variable c will be increased by 1.

After the loop is completed and n has become 0, the control will move outside the loop and then with an if-else condition we will check if the counter variable c is greater than 0 or not. If it is then the sq contains n as its last digit.

So This is how you can solve a complicated problem like this with an easy and simple approach.

- Written by Mayank Vikash
- Published on 3rd December 2022
- Last updated Dec 4, 2022
