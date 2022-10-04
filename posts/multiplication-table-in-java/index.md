---

title: Multiplication Table in Java

description: Java program to display the multiplication of the input number from 1 to 10.

---

![Multiplication Table in Java](https://mayankvikash.in/posts/multiplication-table-in-java/multiplication-tables-in-java.webp)

 - Written by Mayank Vikash
 - Published on 4 October, 2022
 - Last updated Oct 4, 2022

In this post, I am going to show you how to take input from the user to calculate and display the multiplication table of the given number from 1 to 10.

This program can be solved by 2 methods, first one is long and time-consuming whereas the second one needs fewer lines of code but it is not beginners friendly.

Let us first start with the tough one then we will move towards the easy method.

As always, start with the importing statement.

```java
import java.util.Scanner;
```

Public class and public static...
```java
public  class  MultiplicationTable {
public  static  void  main(String[] args) {
```
Making Scanner object.

```java
Scanner in = new Scanner(System.in);
```

Declaring the variable that we are going to use:
```java
int n;
```

Asking the user to input the number.
```java
System.out.println("Enter the number which multiplication table to display");
```
Taking input.
```java
n = in.nextInt();
```
Just a mathematical operation for 10 times with an increment.
```java
System.out.println(n*1);
System.out.println(n*2);
System.out.println(n*3);
System.out.println(n*4);
System.out.println(n*5);
System.out.println(n*6);
System.out.println(n*7);
System.out.println(n*8);
System.out.println(n*9);
System.out.println(n*10);
```

It will do the same thing, with just some more effort of writing so many lines of code.

## Whole source code:
```java
import  java.util.Scanner;
public  class  MultiplicationTable {
public  static  void  main(String[] args) {
Scanner  in = new  Scanner(System.in);
int n;
System.out.println("Enter the number which multiplication table to display");
n = in.nextInt();
System.out.println(n*1);
System.out.println(n*2);
System.out.println(n*3);
System.out.println(n*4);
System.out.println(n*5);
System.out.println(n*6);
System.out.println(n*7);
System.out.println(n*8);
System.out.println(n*9);
System.out.println(n*10);
	} 
}
```
Note: `System.out.println(n);` and `System.out.println(n*1);` is the same things, since a number itself gets printed if you multiply it by 1.

## Output from the first method:
![Output from the first method](https://mayankvikash.in/posts/multiplication-table-in-java/multiplication-table-first-method-output.webp)

I guess you have noticed it the first number is getting printed two times. I don't know why, probably there is something wrong with the compiler. I have commented out `System.out.println(n);` so that the first number does not get printed two times,

Now, let's make the program with the second and easier method.

Note: The second method requires basic knowledge of the while loop. it is recommended to learn about the [while loop](https://www.w3schools.com/js/js_loop_while.asp) before proceeding.

Everything is the same I am just modifying the 10 `System.out.println`.
```java
	while (i<=10) {
	i++; // i++ is below because the first number is getting print 2 times
	System.out.println(n*i);
}

```
Yeah, that's it. While loop makes life so easy.

You may also have noticed that usually the increment `i++` is at the end of the program then why it is above the printing statement? 

The reason is that the first number which is the number itself. is getting printed 2 times so to avoid that, the upgradation statement before the printing statement.

![The first number is getting printed two times](https://mayankvikash.in/posts/multiplication-table-in-java/multiplication-table-first-number-getting-printed-two-times.webp)

## Source code:
```java
import  java.util.Scanner;

public  class  MultiplicationTable {

public  static  void  main(String[] args) {

Scanner  in = new  Scanner(System.in);

int  n, i=1;

System.out.println("Enter the number which multiplication table to display");

n = in.nextInt();

while (i<=10) {

i++; // i++ is below because the first number is getting print 2 times

System.out.println(n*i);

}

}

}

```
## Screenshot of the program
![Screenshot of the program](https://mayankvikash.in/posts/multiplication-table-in-java/screenshot-muiltiplication-table-print-in-java.webp)

## Let's write the program with for loop.

```java

import  java.util.Scanner;

public  class  MultiplicationTable {

public  static  void  main(String[] args) {

Scanner  in = new  Scanner(System.in);

int  n, i;

System.out.println("Enter the number which multiplication table to display");

n = in.nextInt();

for (i = 1; i<=10; i++){
    System.out.println(n*i);
}


}

}

```

## With Do while loop

```java

import  java.util.Scanner;

public  class  MultiplicationTable {

public  static  void  main(String[] args) {

Scanner  in = new  Scanner(System.in);

int  n, i=1;

System.out.println("Enter the number which multiplication table to display");

n = in.nextInt();

    
do{
    
    System.out.println(n*i);
    i++;
}while(i<=10);


}

}

```
Thanks for reading. If you have learned something. Let me know [@MayankVikash1](https://twitter.com/MayankVikash1)













