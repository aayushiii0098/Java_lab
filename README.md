[Program -1 Wap for calculator](#assi-1)

[Program -2 Wap demonstrating forloop](#assi-2)

[Program -3 Wap for Calculation using methods and additional classes](#assi-3)

[Program -4 Wap to add two distances where each distance is given in m,cm and mm](#assi-4)

[Program -5 Wap to add two distances where each distance is given in m and cm](#assi-5)

[Program -6 Wap to add two times where each time is given in hrs,mins and secs](#assi-6)

[Program -7 Wap to add two times where each time is given in hrs and mins](#assi-7)

[Program -8 Wap to do reverse of 1D array](#assi-8)

[Program -9 Wap to demonsrate all 3 types of inheritance with minimum code](#assi-9)

[Program -10 Wap to collect the code from the internet for any five programs of c language (Fact,armstrong,palindrome,fibonacci,pattern](#assi-10)


## assi-1
```
public class Code {
    public static void main(String[] args)
    {
        int a = Integer.parseInt(args[0]);
        int b = Integer.parseInt(args[1]);
        add(a,b);
        multiply(a,b);
        divide(a,b);
        subtract(a,b);
        modulus(a,b);
    }
    //Addition of numbers
    public static void add(int a,int b)
    {
        System.out.print("The addition of the numbers is:");
        System.out.println(a+b);
    }
    //Multiplication of numbers
    public static void multiply(int a,int b)
    {
        System.out.print("The multiplication of the numbers is:");
        System.out.println(a*b);
    }
    //Division of numbers
    public static void divide(int a,int b)
    {
        System.out.print("The division of the numbers is:");
        System.out.println(a/b);
    }
    //Subtraction of numbers
    public static void subtract(int a,int b)
    {
        System.out.print("The subtraction of the numbers is:");
        System.out.println(a-b);
    }
    //Modulus of numbers
    public static void modulus(int a,int b)
    {
        System.out.print("The modulus of the numbers is:");
        System.out.println(a%b);
    }
}
```

<img width="391" height="152" alt="image" src="https://github.com/user-attachments/assets/8fecea76-4e40-43ca-bd6b-82a8088b606c" />



## assi-2
```
public class forloop {
    public static void main(String[] args)
    {
    int n = 5;
    for(int i=0;i<n;i++)
    {
        for(int j=0;j<=i;j++)
        {
            System.out.print("*");
        }
        System.out.println("\n");
    }
    
}
}
```


<img width="326" height="201" alt="image" src="https://github.com/user-attachments/assets/f0e50219-4c4c-4305-8f87-27fb6d3c4e29" />

## assi-3
```

// Additional class
class Calculator {

    // Method for addition
    int add(int a, int b) {
        return a + b;
    }

    // Method for subtraction
    int subtract(int a, int b) {
        return a - b;
    }

    // Method for multiplication
    int multiply(int a, int b) {
        return a * b;
    }

    // Method for division
    int divide(int a, int b) {
        return a / b;
    }
}

// Main class
public class ArithmeticOperations {
    public static void main(String[] args) {

        Calculator calc = new Calculator();

        int a = 20;
        int b = 10;

        System.out.println("Addition = " + calc.add(a, b));
        System.out.println("Subtraction = " + calc.subtract(a, b));
        System.out.println("Multiplication = " + calc.multiply(a, b));
        System.out.println("Division = " + calc.divide(a, b));
    }
}
```
<img width="276" height="88" alt="image" src="https://github.com/user-attachments/assets/58aa9e03-4d7b-41bc-9394-f9a6b1a68692" />


## assi-4
```
class Distance
{
    int m, cm, mm;

    void input(int meter, int centi, int milli)
    {
        m = meter;
        cm = centi;
        mm = milli;
    }

    void add(Distance d1, Distance d2)
    {
        mm = d1.mm + d2.mm;
        cm = d1.cm + d2.cm;
        m = d1.m + d2.m;

        if(mm >= 10)
        {
            cm = cm + mm/10;
            mm = mm % 10;
        }

        if(cm >= 100)
        {
            m = m + cm/100;
            cm = cm % 100;
        }
    }

    void display()
    {
        System.out.println(m + " m " + cm + " cm " + mm + " mm");
    }
}

public class AddDistance
{
    public static void main(String args[])
    {
        Distance d1 = new Distance();
        Distance d2 = new Distance();
        Distance d3 = new Distance();

        d1.input(2,50,8);
        d2.input(3,60,7);

        d3.add(d1,d2);

        System.out.print("Total Distance = ");
        d3.display();
    }
}
```
<img width="258" height="26" alt="image" src="https://github.com/user-attachments/assets/05e24990-7fea-4e41-a2f0-18c2385b3231" />

## assi-5

```
class Distance
{
    int m, cm;
}

public class AddDistance
{
    public static void main(String args[])
    {
        Distance d1 = new Distance();
        Distance d2 = new Distance();
        Distance sum = new Distance();

        d1.m = 3;
        d1.cm = 70;

        d2.m = 2;
        d2.cm = 50;

        sum.m = d1.m + d2.m;
        sum.cm = d1.cm + d2.cm;

        if(sum.cm >= 100)
        {
            sum.m = sum.m + 1;
            sum.cm = sum.cm - 100;
        }

        System.out.println("Total Distance = " + sum.m + " m " + sum.cm + " cm");
    }
}
```
<img width="235" height="20" alt="image" src="https://github.com/user-attachments/assets/1fbc1843-951c-48f7-a93c-9717b49d7e5c" />


## assi-6
```
class Time
{
    int hr, min, sec;
}

public class AddTime
{
    public static void main(String args[])
    {
        Time t1 = new Time();
        Time t2 = new Time();
        Time sum = new Time();

        t1.hr = 2;
        t1.min = 45;
        t1.sec = 50;

        t2.hr = 3;
        t2.min = 20;
        t2.sec = 30;

        sum.sec = t1.sec + t2.sec;
        sum.min = t1.min + t2.min;
        sum.hr = t1.hr + t2.hr;

        if(sum.sec >= 60)
        {
            sum.min = sum.min + 1;
            sum.sec = sum.sec - 60;
        }

        if(sum.min >= 60)
        {
            sum.hr = sum.hr + 1;
            sum.min = sum.min - 60;
        }

        System.out.println("Total Time = " + sum.hr + " hr " + sum.min + " min " + sum.sec + " sec");
    }
}

```
<img width="279" height="26" alt="image" src="https://github.com/user-attachments/assets/7189f6e3-dd79-450f-a3fc-69d008d55c44" />

## assi-7
```
class Time
{
int hr,min;
}

public class AddTime
{
public static void main(String[] args)
{
Time t1=new Time();
Time t2=new Time();
Time sum=new Time();

t1.hr=2;
t1.min=45;
t2.hr=5;
t2.min=56;
sum.min=t1.min+t2.min;
sum.hr=t1.hr+t2.hr;

if(sum.min>=60)
{
sum.hr+=1;
sum.min-=60;
}

System.out.println("Total time =" +sum.hr +"hr"+sum.min+"min");
}
}
```
<img width="226" height="21" alt="image" src="https://github.com/user-attachments/assets/1f85042b-7b98-4362-ae7e-a6d7dcc946dd" />

## assi-8
```
class ArrayRev {

    int arr[] = {1, 2, 3, 4, 5};

    void reverse() {
        for(int i = arr.length - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
    }
}

public class ReverseDemo {

    public static void main(String[] args) {

        ArrayRev obj = new ArrayRev();

        System.out.print("Reversed array: ");
        obj.reverse();
    }
}
```
<img width="204" height="35" alt="image" src="https://github.com/user-attachments/assets/4b479d93-a031-4347-9458-e20cc09e5779" />

## assi-9
```
// Parent class
class Vehicle {
    void showVehicle() {
        System.out.println("This is a Vehicle");
    }
}

// Single inheritance (TwoWheeler inherits Vehicle)
class TwoWheeler extends Vehicle {
    void showTwoWheeler() {
        System.out.println("This is a Two Wheeler");
    }
}

// Multilevel inheritance (Scooty inherits TwoWheeler → Vehicle)
class Scooty extends TwoWheeler {
    void showScooty() {
        System.out.println("This is a Scooty");
    }
}

// Hierarchical inheritance (Car also inherits Vehicle)
class Car extends Vehicle {
    void showCar() {
        System.out.println("This is a Car");
    }
}

// Main class
public class InheritanceDemo {
    public static void main(String[] args) {

        Scooty s = new Scooty();   // multilevel
        s.showVehicle();
        s.showTwoWheeler();
        s.showScooty();

        Car c = new Car();         // hierarchical
        c.showVehicle();
        c.showCar();
    }
}
```
<img width="286" height="94" alt="image" src="https://github.com/user-attachments/assets/8945ffcf-e651-40a9-9a37-5f09242fdde1" />

##  assi-10
```
import java.util.Scanner;

public class AllPrograms {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number for factorial: ");
        int n = sc.nextInt();
        int fact = 1;

        for (int i = 1; i <= n; i++) {
            fact *= i;
        }
        System.out.println("Factorial = " + fact);

        System.out.print("\nEnter number to check Armstrong: ");
        int num = sc.nextInt();
        int temp = num, sum = 0;

        while (temp > 0) {
            int digit = temp % 10;
            sum += digit * digit * digit;
            temp /= 10;
        }

        if (sum == num)
            System.out.println("Armstrong Number");
        else
            System.out.println("Not Armstrong");

        System.out.print("\nEnter number to check Palindrome: ");
        int p = sc.nextInt();
        int rev = 0, original = p;

        while (p > 0) {
            int digit = p % 10;
            rev = rev * 10 + digit;
            p /= 10;
        }

        if (rev == original)
            System.out.println("Palindrome");
        else
            System.out.println("Not Palindrome");

        System.out.print("\nEnter number of terms for Fibonacci: ");
        int terms = sc.nextInt();
        int a = 0, b = 1;

        System.out.print("Fibonacci Series: ");
        for (int i = 1; i <= terms; i++) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
        }

        System.out.print("\n\nEnter rows for pattern: ");
        int rows = sc.nextInt();

        for (int i = 1; i <= rows; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }

        sc.close();
    }
}
```
<img width="299" height="274" alt="image" src="https://github.com/user-attachments/assets/7f8422f0-3352-4854-bf27-3c65b65c0b74" />





    
