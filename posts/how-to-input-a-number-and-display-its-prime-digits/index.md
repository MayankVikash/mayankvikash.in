---
title: How to input a number and display its prime digits?
description: Program in java to input a number and display its prime digits.

---



![How to input a number and display its prime digits?](https://dev.mayankvikash.ml/_next/image?url=https%3A%2F%2Fcdn.hashnode.com%2Fres%2Fhashnode%2Fimage%2Fupload%2Fv1663434277253%2F0VzaTz-zi.png%3Fw%3D1600%26h%3D840%26fit%3Dcrop%26crop%3Dentropy%26auto%3Dcompress%2Cformat%26format%3Dwebp&w=3840&q=75)

[Mayank Vikash](https://twitter.com/MayankVikash1)

·Sep 17, 2022·

### TABLE OF CONTENTS

-   [Let's try thinking of the logic.](#lets-try-thinking-of-the-logic)
-   [Code](#code)
-   [Source Code](#source-code)
-   [Output](#output)

A few days ago, I had a computer test and I got this program which you can read in the title. I don't know how I solved this that time. So, when I returned home I searched on Google for the solution but couldn't find anything.

So, I tried solving that program again myself and after removing some logical errors, I finally made it. In this article, I am going to share how I made the program with you.

![Screenshot of the program](https://cdn.hashnode.com/res/hashnode/image/upload/v1663378405618/wzSjJFy1d.jpeg?auto=compress,format&format=webp)

### Let's try thinking of the logic.

Okay great, let's see how will the program work.

I have to  **take a number as input and print the digits which are prime**.

> A number is called prime, when it has only two factors, 1 and the number itself.

A digit of a number is between 0-9. So between that, we get:

-   0 is not a prime number
    
-   1 is also not a prime number
    
-   2 is a prime number
    
-   3 is also a prime number
    
-   4 is not a prime number
    
-   5 is a prime number
    
-   6 is not a prime number
    
-   7 is a prime number
    
-   8 is not a prime number
    
-   9 is a prime number
    

So between 0 and 9, we have five prime numbers, which are 2, 3, 5, 7, and 9.

Well this makes the logic so easy, I just have to extract the digits and check with an if-else if the digits match one of these five numbers, then I have to print it.

### Code

First, I have initialized the variables which are going to be used in the program.



```java
 int n, d;
```

Then, ask the user to enter a number.


```java
System.out.println("Enter a number");
n = in.nextInt();
```

Starting the while loop
```java
while(condition){
// body
}
```

Condition in the while loop.

```java
while(n>0)
```

Extracting the digits



```java
d = n%10;

```

The modulus operator will divide the number by 10 and store the remainder in the variable d. For example, 77 % of 10 will divide by 77 by 10 and the result will be the remainder, which is 7.

Then, check if the digit is prime or not and display if it is prime.



```java
if ( d==2 || d==3 || d==5 || d ==7 || d ==9)
     System.out.println(d);

```

After this, dividing the number by 10

```java
n = n/10;
```

If the number is 89 then, 89/10 will result in 8 which will be now stored in the variable 'n'.

###  Source Code



```java
import java.utril.*;
public class PrimeDigit{
  public static void main(String args[]){
    Scanner in = new Scanner(System.in);
       int n, d;
            System.out.println("Enter a number");
            n = in.nextInt();
            while (n>0) {
                d = n%10;
                if ( d==2 || d==3 || d==5 || d ==7 || d ==9)
                    System.out.println(d);
                n = n/10;
            }
      }
}

```

### Output

![Program output](https://cdn.hashnode.com/res/hashnode/image/upload/v1663430508544/pkH95Flbc.jpeg?auto=compress,format&format=webp)


