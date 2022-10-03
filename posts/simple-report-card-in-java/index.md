---

layout: default
title: Simple Report Card in Java
description: Java Project to take input of marks of 2 subjects and display Total, Percentage, Highest Marks, Average, and Remarks.

---





## A Simple Report Card in Java

![Report-Card-in-Java-Screenshot](https://blogger.googleusercontent.com/img/a/AVvXsEgQeRUV4FpooVIL5vqyZUzNT6_B-Naze4bBRE1pmOeVvIeeL2JMXs4wtaw1FPK0qcllEn1Lj46xeD7snqj-s4WcglcSmqPeCvvLgFYsnAsL6AL8na9He_TkYPBGmlFZFOoInkAcLxwa0GG3NQUuEPfr3Lxu_7xYGsggEX-JAG3uRb3Jepu7g3UU1vFW)

I learned Java last semester, so I thought I should make a project.  
I searched on Google for Java projects and I found:

**Write a program to take marks of 2 subjects from the user and display the Total, Percentage, Highest Marks, Average, and Remarks.**

It was not that tough, so this is how I made it.

First, I imported this library for taking input from users:

```
import  java.util.Scanner;

```

Then, I created the file named ‘marks’. I know this file name doesn’t make sense but it’s ok.

Java starting Template:

```
public  class  marks {
public  static  void  main(String  args[]) { 
    // Code Here
    }
}

```

Starting with my code, I defined  [Scanner Class](https://www.w3schools.com/java/java_user_input.asp)  a variable ‘sc’ to make it easy to get input from the user

```
try (Scanner  sc = new  Scanner(System.in)) {
	// Code Here
}

```

I put the above variable in ‘try’ because Visual Studio was giving errors.

Next, I displayed in the console what I want from them:

```
System.out.println("Enter the marks of 2 subjects (out of 100)");

```

Then, I asked the two inputs from the user

```
System.out.println("Enter the marks of subject 1:");  
int  sub1 = sc.nextInt();

System.out.println("Enter the marks of subject 2:");
int  sub2 = sc.nextInt();

```

‘sc’ is the variable name that I declared above and  `nextInt()`  is the function for accepting the values in an integer which will be stored in the variable ‘sub1’ and ‘sub2’ respectively.

Okay, here comes the important step, as you know you can’t score more than 100 in a subject, doesn’t matter how brilliant you are. So, I have to make sure that, the user can’t add numbers greater than 100.

This condition makes sure that the entered value is less than or equal to 100.

```
if (sub1 <= 100 && sub2 <= 100) {
    // This code will be executed if the condition is true
} else{
    // This code will be executed if the condition if false
}

```

Wow, great! All the measures are taken, users also can’t give any other input except number, if they try, they will get an error.

Now time for the real code:

```
int  total = sub1 + sub2;
System.out.println("Total = " + total);

```

This will add the two values and print the Total.

This code will find the percentage, just take the total, divide it by 200 (because there are 2 subjects so total marks will be 200) then, multiply it by 100. Simple.

Note: ‘float’ is used because the answer may be in decimal and it is also multiplied by ‘float’ to covert it into float datatype. How to convert  [Integer into Float.](https://www.c-sharpcorner.com/article/the-complete-java-type-casting-tutorial/)

```
float  percent = (float) total / 200 * 100;
System.out.println("Percentage = " + percent);

```

Then, a simple if-else statement to get the highest number:

```
if (sub1 > sub2) {
System.out.println("Highest marks scored is " + sub1);
} else {
System.out.println("Highest marks scored is " + sub2);
}

```

For finding the average, just take the total and divide it by 2:

```
float  avg = (float) total / 2;
System.out.println("Average is " + avg);

```

Then, again an if-else to display remarks. If the mark is 50 or less than that, then it will display ‘You need to work hard!’. If the marks are above 80 or equal and less than 90 then it will show ‘Good Marks’, if it is above 90 then it will show ‘Excellent’. Pretty Simple.

```
if (percent <= 50) {
System.out.println("Remarks: You need to work hard!");
} else  if (percent >= 80 && percent <= 90) {
System.out.println("Remarks: Good Marks :)");
} else  if (percent >= 90) {
System.out.println("Remarks: Excellent");
} else {
System.out.println("Remarks: Good");
}

```

So, that’s how I made it. It was really fun. By the way, thanks for visiting and reading :)

### Source Code:

```
import  java.util.Scanner;

  

public  class  marks {

public  static  void  main(String  args[]) {

  

try (Scanner  sc = new  Scanner(System.in)) {

  

System.out.println("Enter the marks of 2 subjects (out of 100)");

  

System.out.println("Enter the marks of subject 1:");

int  sub1 = sc.nextInt();

  

System.out.println("Enter the marks of subject 2:");

int  sub2 = sc.nextInt();

  

if (sub1 <= 100 && sub2 <= 100) {

  

// Total

  

int  total = sub1 + sub2;

System.out.println("Total = " + total);

  

// Percentage

  

float  percent = (float) total / 200 * 100;

System.out.println("Percentage = " + percent);

  

// Highest Marks

  

if (sub1 > sub2) {

System.out.println("Highest marks scored is " + sub1);

} else {

System.out.println("Highest marks scored is " + sub2);

}

  

// Average

  

float  avg = (float) total / 2;

System.out.println("Average is " + avg);

  

// Remarks

if (percent <= 50) {

System.out.println("Remarks: You need to work hard!");

} else  if (percent >= 80 && percent <= 90) {

System.out.println("Remarks: Good Marks :)");

} else  if (percent >= 90) {

System.out.println("Remarks: Excellent");

} else {

System.out.println("Remarks: Good");

}

  

} else {

System.out.println("Values are Greator!");

}

  

}

  

}

  

}

```

### Output:  
![java-project-simple-report-card-output](https://blogger.googleusercontent.com/img/a/AVvXsEixfYXxVm0gV3VqAYWBnwnczcyyAtf9bd51h7VSmhlwV0anGdBp6NfC5k5wothsN1EXmyhN1m4gh6Jqx36GTJFp_j6jX0lbbriHyTrsbiduug1kqlyDkJ8sPf-hBKIZR-VggoLZ_lmqNJj9Vs7XbSgpY4uyg9Jp1DqJ2nhJXmhlO-hx47dPSH5eyw6s)

Wow great! I am able to make it but it's look little bit easy, let's add some complex things.

### Write a program to take marks of 15 subjects from the user and display the Total, Percentage, Highest Marks, Average, and Remarks. It should also work if the number of subjects is less than 15 .

Well. looks good. So, starting with formating the old code.
![commented-out-old-code](https://blogger.googleusercontent.com/img/a/AVvXsEgMuboHvKJxqRxYpcHT4CYemehQTUmRjW5zykTEMXCVbdcuC0HLwtIJsUd3tGj7YVEC_mw6SLGTxdaJWTKS6QsAh0wTzHiUOCSpcjRdEvxm0y94yHpu1IBIBMz6bVLrPZho45HpZQXIpHGxP6hURsURB_5F63vQQPKr8CByLZLGVeYIJa6crWXruD67)

Then, I took a variable and asked how many subject are there in total:

    System.out.println("How many subjects do you have? (Maximum 15, minimum 2)");
    
    int  sub_count = sc.nextInt();

A simple condition to make sure the minimum number of subjects should be 2:

    if (sub_count == 1) {

    System.out.println("Atleast 2 subjects required");

    }

Similarly, I made a else condition which will be executed when the number of is more than 15 or less than 2 (also for negative integers, ex- -15, -27):

    else {
    System.out.println("Error: Number of subjects should not be more than 15 or not less than 0");
    }
I added more 14 condition for different inputs, for ex if the number of subjects is 2, this code will be executed:


    else  if (sub_count == 2) {
    
      
    
    System.out.println("Enter the marks of 2 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2;
    
    System.out.println("Total = " + total + "/200");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 200 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    if (sub1 > sub2) {
    
    System.out.println("Highest marks scored is " + sub1);
    
    } else {
    
    System.out.println("Highest marks scored is " + sub2);
    
    }
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 2;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    }

I repeated the same code with some minor changes like, if the no. of subjects is 3 I made one more variable for that and stored the value in it:

    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();

I added this variable in this condition so that the value should not be greater than 100:

    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100) {
    	// Code
    }
Added the third variable in total:

    int  total = sub1 + sub2 + sub3;
    
    System.out.println("Total = " + total + "/300");

Same in Percentage:

    float  percent = (float) total / 300 * 100;
    
    System.out.println("Percentage = " + percent + "%");

And for the highest marks first I compared the marks of first two subjects and added the grester on to another variable then, compared the greater of the two with the marks of third subject:

    int  max1 = Math.max(sub1,  sub2);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max1,  sub3));

Same thing with Average:

    float  avg = (float) total / 3;
    
    System.out.println("Average is " + avg);

Nothing more is changed, the most important in the highest marks, if the no. of subjects is 4 then this how the code of Highest marks will look:

    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
   
    System.out.println("Highest Marks = " + Math.max(max2,  sub4));

Compared the first 2, stored greater one in a variable, compared the variable with subject 3, stored the greator one in `max2` and compared it with the fourth subject. Check out this question on stackoverflow to learn more: https://stackoverflow.com/questions/4982210/find-the-max-of-3-numbers-in-java-with-different-data-types

This is how the code looks like if the total subjcts are 15:

    else  if (sub_count == 15) {
    
      
    
    System.out.println("Enter the marks of 10 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 7");
    
    int  sub7 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 8");
    
    int  sub8 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 9");
    
    int  sub9 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 10");
    
    int  sub10 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 11");
    
    int  sub11 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 12");
    
    int  sub12 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 13");
    
    int  sub13 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 14");
    
    int  sub14 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 15");
    
    int  sub15 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100
    
    && sub7 <= 100 && sub8 <= 100 && sub9 <= 100 && sub10 <= 100 && sub11 <= 100 && sub12 <= 100
    
    && sub13 <= 100 && sub14 <= 100 && sub15 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6 + sub7 + sub8 + sub9 + sub10 + sub11 + sub12
    
    + sub13 + sub14 + sub15;
    
    System.out.println("Total = " + total + "/1500");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 1500 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
    int  max5 = Math.max(max4,  sub6);
    
    int  max6 = Math.max(max5,  sub7);
    
    int  max7 = Math.max(max6,  sub8);
    
    int  max8 = Math.max(max7,  sub9);
    
    int  max9 = Math.max(max8,  sub10);
    
    int  max10 = Math.max(max9,  sub11);
    
    int  max11 = Math.max(max10,  sub12);
    
    int  max12 = Math.max(max11,  sub13);
    
    int  max13 = Math.max(max12,  sub14);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max13,  sub15));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 15;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    }


### Source code for 15 subjects

    import  java.util.Scanner;
    
      
    
    public  class  marks {
    
    public  static  void  main(String  args[]) {
    
      
    
    try (Scanner  sc = new  Scanner(System.in)) {
    
      
    
    System.out.println("How many subjects do you have? (Maximum 15, minimum 2)");
    
    int  sub_count = sc.nextInt();
    
      
    
    if (sub_count == 1) {
    
      
    
    System.out.println("Atleast 2 subjects required");
    
      
    
    }
    
      
    
    else  if (sub_count == 2) {
    
      
    
    System.out.println("Enter the marks of 2 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2;
    
    System.out.println("Total = " + total + "/200");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 200 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    if (sub1 > sub2) {
    
    System.out.println("Highest marks scored is " + sub1);
    
    } else {
    
    System.out.println("Highest marks scored is " + sub2);
    
    }
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 2;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    }
    
      
    
    // 3 Subjects
    
      
    
    else  if (sub_count == 3) {
    
      
    
    System.out.println("Enter the marks of 3 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3;
    
    System.out.println("Total = " + total + "/300");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 300 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max1,  sub3));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 3;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    }
    
      
    
    // 4 Subjects
    
      
    
    else  if (sub_count == 4) {
    
      
    
    System.out.println("Enter the marks of 4 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4;
    
    System.out.println("Total = " + total + "/400");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 400 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max2,  sub4));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 4;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // Subject 5
    
      
    
    } else  if (sub_count == 5) {
    
      
    
    System.out.println("Enter the marks of 5 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5;
    
    System.out.println("Total = " + total + "/500");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 500 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max3,  sub5));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 5;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // Subject 6
    
      
    
    } else  if (sub_count == 6) {
    
    System.out.println("Enter the marks of 6 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6;
    
    System.out.println("Total = " + total + "/600");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 600 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max4,  sub6));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 6;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // Subject 7
    
      
    
    } else  if (sub_count == 7) {
    
    System.out.println("Enter the marks of 7 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 7");
    
    int  sub7 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100
    
    && sub7 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6 + sub7;
    
    System.out.println("Total = " + total + "/700");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 700 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
    int  max5 = Math.max(max4,  sub6);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max5,  sub7));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 7;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // subject 8
    
      
    
    } else  if (sub_count == 8) {
    
      
    
    System.out.println("Enter the marks of 8 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 7");
    
    int  sub7 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 8");
    
    int  sub8 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100
    
    && sub7 <= 100 && sub8 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6 + sub7 + sub8;
    
    System.out.println("Total = " + total + "/800");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 800 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
    int  max5 = Math.max(max4,  sub6);
    
    int  max6 = Math.max(max5,  sub7);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max6,  sub8));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 8;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // subject 9
    
      
    
    } else  if (sub_count == 9) {
    
      
    
    System.out.println("Enter the marks of 9 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 7");
    
    int  sub7 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 8");
    
    int  sub8 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 9");
    
    int  sub9 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100
    
    && sub7 <= 100 && sub8 <= 100 && sub9 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6 + sub7 + sub8 + sub9;
    
    System.out.println("Total = " + total + "/900");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 900 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
    int  max5 = Math.max(max4,  sub6);
    
    int  max6 = Math.max(max5,  sub7);
    
    int  max7 = Math.max(max6,  sub8);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max7,  sub9));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 8;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // subject 10
    
      
    
    } else  if (sub_count == 10) {
    
      
    
    System.out.println("Enter the marks of 10 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 7");
    
    int  sub7 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 8");
    
    int  sub8 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 9");
    
    int  sub9 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 10");
    
    int  sub10 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100
    
    && sub7 <= 100 && sub8 <= 100 && sub9 <= 100 && sub10 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6 + sub7 + sub8 + sub9 + sub10;
    
    System.out.println("Total = " + total + "/1000");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 1000 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
    int  max5 = Math.max(max4,  sub6);
    
    int  max6 = Math.max(max5,  sub7);
    
    int  max7 = Math.max(max6,  sub8);
    
    int  max8 = Math.max(max7,  sub9);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max8,  sub10));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 10;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // subject 11
    
      
    
    } else  if (sub_count == 11) {
    
      
    
    System.out.println("Enter the marks of 10 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 7");
    
    int  sub7 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 8");
    
    int  sub8 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 9");
    
    int  sub9 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 10");
    
    int  sub10 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 11");
    
    int  sub11 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100
    
    && sub7 <= 100 && sub8 <= 100 && sub9 <= 100 && sub10 <= 100 && sub11 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6 + sub7 + sub8 + sub9 + sub10 + sub11;
    
    System.out.println("Total = " + total + "/1100");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 1100 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
    int  max5 = Math.max(max4,  sub6);
    
    int  max6 = Math.max(max5,  sub7);
    
    int  max7 = Math.max(max6,  sub8);
    
    int  max8 = Math.max(max7,  sub9);
    
    int  max9 = Math.max(max8,  sub10);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max9,  sub11));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 11;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // subject 12
    
    } else  if (sub_count == 12) {
    
      
    
    System.out.println("Enter the marks of 10 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 7");
    
    int  sub7 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 8");
    
    int  sub8 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 9");
    
    int  sub9 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 10");
    
    int  sub10 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 11");
    
    int  sub11 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 12");
    
    int  sub12 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100
    
    && sub7 <= 100 && sub8 <= 100 && sub9 <= 100 && sub10 <= 100 && sub11 <= 100 && sub12 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6 + sub7 + sub8 + sub9 + sub10 + sub11 + sub12;
    
    System.out.println("Total = " + total + "/1200");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 1200 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
    int  max5 = Math.max(max4,  sub6);
    
    int  max6 = Math.max(max5,  sub7);
    
    int  max7 = Math.max(max6,  sub8);
    
    int  max8 = Math.max(max7,  sub9);
    
    int  max9 = Math.max(max8,  sub10);
    
    int  max10 = Math.max(max9,  sub11);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max10,  sub12));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 12;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // subject 13
    
      
    
    } else  if (sub_count == 13) {
    
      
    
    System.out.println("Enter the marks of 10 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 7");
    
    int  sub7 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 8");
    
    int  sub8 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 9");
    
    int  sub9 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 10");
    
    int  sub10 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 11");
    
    int  sub11 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 12");
    
    int  sub12 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 13");
    
    int  sub13 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100
    
    && sub7 <= 100 && sub8 <= 100 && sub9 <= 100 && sub10 <= 100 && sub11 <= 100 && sub12 <= 100
    
    && sub13 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6 + sub7 + sub8 + sub9 + sub10 + sub11 + sub12
    
    + sub13;
    
    System.out.println("Total = " + total + "/1300");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 1300 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
    int  max5 = Math.max(max4,  sub6);
    
    int  max6 = Math.max(max5,  sub7);
    
    int  max7 = Math.max(max6,  sub8);
    
    int  max8 = Math.max(max7,  sub9);
    
    int  max9 = Math.max(max8,  sub10);
    
    int  max10 = Math.max(max9,  sub11);
    
    int  max11 = Math.max(max10,  sub12);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max11,  sub13));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 13;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // subject 14
    
      
    
    } else  if (sub_count == 14) {
    
      
    
    System.out.println("Enter the marks of 10 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 7");
    
    int  sub7 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 8");
    
    int  sub8 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 9");
    
    int  sub9 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 10");
    
    int  sub10 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 11");
    
    int  sub11 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 12");
    
    int  sub12 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 13");
    
    int  sub13 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 14");
    
    int  sub14 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100
    
    && sub7 <= 100 && sub8 <= 100 && sub9 <= 100 && sub10 <= 100 && sub11 <= 100 && sub12 <= 100
    
    && sub13 <= 100 && sub14 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6 + sub7 + sub8 + sub9 + sub10 + sub11 + sub12
    
    + sub13 + sub14;
    
    System.out.println("Total = " + total + "/1400");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 1400 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
    int  max5 = Math.max(max4,  sub6);
    
    int  max6 = Math.max(max5,  sub7);
    
    int  max7 = Math.max(max6,  sub8);
    
    int  max8 = Math.max(max7,  sub9);
    
    int  max9 = Math.max(max8,  sub10);
    
    int  max10 = Math.max(max9,  sub11);
    
    int  max11 = Math.max(max10,  sub12);
    
    int  max12 = Math.max(max11,  sub13);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max12,  sub14));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 14;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    // subject 15
    
      
    
    } else  if (sub_count == 15) {
    
      
    
    System.out.println("Enter the marks of 10 subjects (out of 100)");
    
      
    
    System.out.println("Enter the marks of subject 1:");
    
    int  sub1 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 2:");
    
    int  sub2 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 3");
    
    int  sub3 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 4");
    
    int  sub4 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 5");
    
    int  sub5 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 6");
    
    int  sub6 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 7");
    
    int  sub7 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 8");
    
    int  sub8 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 9");
    
    int  sub9 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 10");
    
    int  sub10 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 11");
    
    int  sub11 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 12");
    
    int  sub12 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 13");
    
    int  sub13 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 14");
    
    int  sub14 = sc.nextInt();
    
      
    
    System.out.println("Enter the marks of subject 15");
    
    int  sub15 = sc.nextInt();
    
      
    
    if (sub1 <= 100 && sub2 <= 100 && sub3 <= 100 && sub4 <= 100 && sub5 <= 100 && sub6 <= 100
    
    && sub7 <= 100 && sub8 <= 100 && sub9 <= 100 && sub10 <= 100 && sub11 <= 100 && sub12 <= 100
    
    && sub13 <= 100 && sub14 <= 100 && sub15 <= 100) {
    
      
    
    // Total
    
      
    
    int  total = sub1 + sub2 + sub3 + sub4 + sub5 + sub6 + sub7 + sub8 + sub9 + sub10 + sub11 + sub12
    
    + sub13 + sub14 + sub15;
    
    System.out.println("Total = " + total + "/1500");
    
      
    
    // Percentage
    
      
    
    float  percent = (float) total / 1500 * 100;
    
    System.out.println("Percentage = " + percent + "%");
    
      
    
    // Highest Marks
    
      
    
    int  max1 = Math.max(sub1,  sub2);
    
    int  max2 = Math.max(max1,  sub3);
    
    int  max3 = Math.max(max2,  sub4);
    
    int  max4 = Math.max(max3,  sub5);
    
    int  max5 = Math.max(max4,  sub6);
    
    int  max6 = Math.max(max5,  sub7);
    
    int  max7 = Math.max(max6,  sub8);
    
    int  max8 = Math.max(max7,  sub9);
    
    int  max9 = Math.max(max8,  sub10);
    
    int  max10 = Math.max(max9,  sub11);
    
    int  max11 = Math.max(max10,  sub12);
    
    int  max12 = Math.max(max11,  sub13);
    
    int  max13 = Math.max(max12,  sub14);
    
      
    
    System.out.println("Highest Marks = " + Math.max(max13,  sub15));
    
      
    
    // Average
    
      
    
    float  avg = (float) total / 15;
    
    System.out.println("Average is " + avg);
    
      
    
    // Remarks
    
    if (percent <= 50) {
    
    System.out.println("Remarks: You need to work hard!");
    
    } else  if (percent >= 80 && percent <= 90) {
    
    System.out.println("Remarks: Good Marks :)");
    
    } else  if (percent >= 90) {
    
    System.out.println("Remarks: Excellent");
    
    } else {
    
    System.out.println("Remarks: Good");
    
    }
    
      
    
    } else {
    
    System.out.println("Values are Greator!");
    
    }
    
      
    
    }
    
      
    
    else {
    
    System.out.println("Error: Number of subjects should not be more than 15 or not less than 0");
    
    }
    
      
    
    // System.out.println("Enter the marks of 2 subjects (out of 100)");
    
      
    
    // System.out.println("Enter the marks of subject 1:");
    
    // int sub1 = sc.nextInt();
    
      
    
    // System.out.println("Enter the marks of subject 2:");
    
    // int sub2 = sc.nextInt();
    
      
    
    // if (sub1 <= 100 && sub2 <= 100) {
    
      
    
    // // Total
    
      
    
    // int total = sub1 + sub2;
    
    // System.out.println("Total = " + total);
    
      
    
    // // Percentage
    
      
    
    // float percent = (float) total / 200 * 100;
    
    // System.out.println("Percentage = " + percent);
    
      
    
    // // Highest Marks
    
      
    
    // if (sub1 > sub2) {
    
    // System.out.println("Highest marks scored is " + sub1);
    
    // } else {
    
    // System.out.println("Highest marks scored is " + sub2);
    
    // }
    
      
    
    // // Average
    
      
    
    // float avg = (float) total / 2;
    
    // System.out.println("Average is " + avg);
    
      
    
    // // Remarks
    
    // if (percent <= 50) {
    
    // System.out.println("Remarks: You need to work hard!");
    
    // } else if (percent >= 80 && percent <= 90) {
    
    // System.out.println("Remarks: Good Marks :)");
    
    // } else if (percent >= 90) {
    
    // System.out.println("Remarks: Excellent");
    
    // } else {
    
    // System.out.println("Remarks: Good");
    
    // }
    
      
    
    // } else {
    
    // System.out.println("Values are Greator!");
    
    // }
    
      
    
    }
    
      
    
    }
    
      
    
    }


### 15 Subjects Output

<iframe allowfullscreen="allowfullscreen" class="b-hbp-video b-uploaded" frameborder="0" height="266" id="BLOGGER-video-37370f584d770a3d-12958" mozallowfullscreen="mozallowfullscreen" src="https://www.blogger.com/video.g?token=AD6v5dwD6iubllHqPoMQMVMCJtvqvDPdP4lcZ3e2JgDQ119CmmdCcjAxnh2c2X7eupES6oxT__UDFgdPpT0Xft8eg6HoSEsj7lRq3GhGATBd1LMngjWySz0BC2ilV3klgxxSC3_q8wL6" webkitallowfullscreen="webkitallowfullscreen" width="320"></iframe>



[Originally Published](https://mayankvikash.ml/posts/simple-report-card-in-java.html)

[Check out other posts](https://mayankvikash.ml/posts/)

[Latest updates](https://mayankvikash.ml//news/)

[HTML Sitemap](https://mayankvikash.ml/sitemap.html)

[Sitemap](https://mayankvikash.ml/sitemap.xml)

Made by  [Mayank Vikash](https://mayankvikash.ml/)



