---

layout: default

title: Expansion Formulas in Java

description: A simple java program to take the input a and b and display the output based on the formula selected by the user.

---
![Expansions Formulae Program in Java](https://mayankvikash.ml/posts/Expansion-Formulas-in-Java/exp-frmula-java.webp)
I was practising Maths and a thought came up to my mind that I should make a program in Java that could take the input in variables 'a' and 'b' and then it will ask the user which formulae of expansion they want to perform.
![Asking users which formulae they want to use](https://mayankvikash.ml/posts/Expansion-Formulas-in-Java/java-console-expansion-in-java-ask.webp)
Something like this.
Currently, it has only 5 formulas because I am lazy to add more.

## Code
I started with displaying the formulas this program can execute in the console
```java
    System.out.println("Choose the Formula");
    System.out.println("Enter 1 for (a+b)^2");
    System.out.println("Enter 2 for (a-b)^2");
    System.out.println("Enter 3 for (a^2 - b^2)");
    System.out.println("Enter 4 for (a+b)^3");
    System.out.println("Enter 5 for (a-b)^3");
```
So, this program will work for the following formulas:

 - (a+b)²
 - (a-b)²
 - (a² - b²)
 - (a+b)³
 - (a-b)³

I took the input of the choice in a variable **ip** (Don't know why I chose this name 😅) which is of integer data type.    
```java
    int  ip = sc.nextInt();
```
    
I also took the value of 'a' and 'b' as input, because they are common variables (Common variables are the variables which are repeatedly used in every conditional statement, it is preferred to take the common variable's value input before the conditional statements start.)

```java
    System.out.println("Enter the value of a and b");
    double  a = sc.nextDouble();
    double  b = sc.nextDouble();
```
The variables a and b will contain the values, input by the user.

(Note: variable a and b are of the double datatype, because the user may want to enter a decimal number.)

Now, when you have got the values, you just have to put the formula and solve it. This will work for Maths but in Java, you have to do a little bit more work.

First, there is a condition, which will execute the formulae which the user has entered.
![Condition Statement](https://mayankvikash.ml/posts/Expansion-Formulas-in-Java/exp-formula-java-condition.webp)

For example, if the user entered choice 1,  the program will calculate (a+b)² from the given values of a and b.

Similarly, if the user entered choice 5,  the program will calculate (a-b)³.

If the user enters any other choice, he will get the output: "Wrong Choice".

This is the block of statements that will execute if the user enters choice 1:
```java
ans = a*a + 2*a*b + b*b;
System.out.println("Working:");
System.out.println("a*a + 2*a*b + b*b");
System.out.println(ans);
```

 Note: (a+b)² = a² + b² + 2ab but, in Java this expression will be written as,
 ```java
 a*a + 2*a*b + b*b
 ```
 Similarly, expressions for the  rest of the formulas:

 - (a-b)²

 ```java
 a*a - 2*a*b + b*b
```

 - a²-b²
 ```java
 (a+b) * (a-b)
 ```

- (a+b)³
```java
a*a*a + b*b*b + 3*a*b *(a+b)
```
 - (a-b)³
 ```java
 a*a*a - b*b*b - 3*a*b *(a-b)
 ```
Pretty easy, right? Let me know on Twitter [@MayankVikash1](https://twitter.com/MayankVikash1) 
Made by: [Mayank Vikash](https://mayankvikash.ml/)

## Source Code
```java
import  java.util.*;

public  class  ExpansionFormulas {

public  static  void  main(String[] args) {

Scanner  sc = new  Scanner(System.in);

double  ans;

System.out.println("Choose the Formula");

System.out.println("Enter 1 for (a+b)^2");

System.out.println("Enter 2 for (a-b)^2");

System.out.println("Enter 3 for (a^2 - b^2)");

System.out.println("Enter 4 for (a+b)^3");

System.out.println("Enter 5 for (a-b)^3");

int  ip = sc.nextInt();

System.out.println("Enter the value of a and b");

double  a = sc.nextDouble();

double  b = sc.nextDouble();

if (ip ==1){

ans = a*a + 2*a*b + b*b;

System.out.println("Working:");

System.out.println("a*a + 2*a*b + b*b");

System.out.println(ans);

}

else  if (ip == 2){

ans = a*a - 2*a*b + b*b;

System.out.println("Working:");

System.out.println("a*a - 2*a*b + b*b");

System.out.println(ans);

}

else  if (ip ==3){

ans = (a+b) * (a-b);

System.out.println("Working:");

System.out.println("(a+b) * (a-b)");

System.out.println(ans);

}

else  if (ip == 4){

ans = a*a*a + b*b*b + 3*a*b *(a+b);

System.out.println("Working:");

System.out.println("a*a*a + b*b*b + 3*a*b *(a+b)");

System.out.println(ans);

}

else  if (ip == 5){

ans = a*a*a - b*b*b - 3*a*b *(a-b);

System.out.println("Working:");

System.out.println("a*a*a - b*b*b - 3*a*b *(a-b)");

System.out.println(ans);

}

else{

System.out.println("Wrong Choice");

}

}

  
  

}
```

## Output
### Image

![Output](https://mayankvikash.ml/posts/Expansion-Formulas-in-Java/exp-formula-in0java-output.webp)

Check out [Simple Report Card in Java](https://mayankvikash.ml/posts/simple-report-card-in-java)

Read other [posts](https://mayankvikash.ml/posts/)

[Sitemap](https://mayankvikash.ml/sitemap.xml)

### Video
<iframe src="https://mayankvikash.ml/posts/Expansion-Formulas-in-Java/exp-formula-java-output.webm" allowfullscreen>





