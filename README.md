[Program -1 Wap for calculator](#assi-1)

[Program -2 Wap demonstrating forloop](#assi-2)

[Program -3 Wap for Calculation using methods and additional classes](#assi-3)

[Program -4 Wap to add two distances where each distance is given in m,cm and mm](#assi-4)

[Program -5 Wap to add two distances where each distance is given in m and cm](#assi-5)

[Program -6 Wap to add two times where each time is given in hrs,mins and secs](#assi-6)

[Program -7 Wap to add two times where each time is given in hrs and mins](#assi-7)

[Program -8 Wap to do reverse of 1D array](#assi-8)

[Program -9 Wap to demonsrate all 3 types of inheritance with minimum code](#assi-9)

[Program -10 Wap to collect the code from the internet for any five programs of c language (Fact,armstrong,palindrome,fibonacci,pattern)](#assi-10)

[Program -11 Wap a class with multiple methods to perform matrix operations (tranpose,addition,sum of rows, sum of columns,sum of diagonal)](#assi-11)



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

## assi-11
```
import java.util.Scanner;

public class MatrixOperations {

    public static void transpose(int[][] a, int r, int c) {
        int[][] t = new int[c][r];
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                t[j][i] = a[i][j];
            }
        }

        System.out.println("Transpose:");
        for (int i = 0; i < c; i++) {
            for (int j = 0; j < r; j++) {
                System.out.print(t[i][j] + " ");
            }
            System.out.println();
        }
    }

    public static void addition(int[][] a, int[][] b, int r, int c) {
        int[][] sum = new int[r][c];
        System.out.println("Addition:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                sum[i][j] = a[i][j] + b[i][j];
                System.out.print(sum[i][j] + " ");
            }
            System.out.println();
        }
    }

    public static void sumRows(int[][] a, int r, int c) {
        for (int i = 0; i < r; i++) {
            int sum = 0;
            for (int j = 0; j < c; j++) {
                sum += a[i][j];
            }
            System.out.println("Sum of row " + (i + 1) + " = " + sum);
        }
    }

    public static void sumCols(int[][] a, int r, int c) {
        for (int j = 0; j < c; j++) {
            int sum = 0;
            for (int i = 0; i < r; i++) {
                sum += a[i][j];
            }
            System.out.println("Sum of column " + (j + 1) + " = " + sum);
        }
    }

    public static void sumDiagonal(int[][] a, int n) {
        int primary = 0, secondary = 0;

        for (int i = 0; i < n; i++) {
            primary += a[i][i];
            secondary += a[i][n - i - 1];
        }

        System.out.println("Primary Diagonal Sum = " + primary);
        System.out.println("Secondary Diagonal Sum = " + secondary);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter rows and columns: ");
        int r = sc.nextInt();
        int c = sc.nextInt();

        int[][] a = new int[r][c];
        int[][] b = new int[r][c];

        System.out.println("Enter elements of Matrix A:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                a[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter elements of Matrix B:");
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {
                b[i][j] = sc.nextInt();
            }
        }

        transpose(a, r, c);
        addition(a, b, r, c);
        sumRows(a, r, c);
        sumCols(a, r, c);

        if (r == c) {
            sumDiagonal(a, r);
        } else {
            System.out.println("Diagonal sum only for square matrix");
        }

        sc.close();
    }
}
```
<img width="304" height="425" alt="image" src="https://github.com/user-attachments/assets/e169e275-1a81-4f7f-969d-62b02c35080f" />

## assi-12
Without thread
```
class A {
    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A: " + i);
        }
    }
}

class B {
    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B: " + i);
        }
    }
}

class C {
    void print() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C: " + i);
        }
    }
}

public class WithoutThread {
    public static void main(String[] args) {
        A a = new A();
        B b = new B();
        C c = new C();

        a.print();
        b.print();
        c.print();
    }
}
```
<img width="1042" height="616" alt="image" src="https://github.com/user-attachments/assets/1724f506-5f4d-4faa-bb16-5687dc1f8f8d" />

With Thread
```
class A extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A: " + i);
        }
    }
}

class B extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B: " + i);
        }
    }
}

class C extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C: " + i);
        }
    }
}

public class WithThread {
    public static void main(String[] args) {
        A a = new A();
        B b = new B();
        C c = new C();

        a.start();
        b.start();
        c.start();
    }
}
```
<img width="1055" height="551" alt="image" src="https://github.com/user-attachments/assets/a7e0a600-a5a9-44f0-a6f8-ce2cec034d80" />

Runnable Interface
```
class A implements Runnable {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A: " + i);
        }
    }
}

class B implements Runnable {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B: " + i);
        }
    }
}

class C implements Runnable {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C: " + i);
        }
    }
}

public class RunnableDemo {
    public static void main(String[] args) {
        Thread t1 = new Thread(new A());
        Thread t2 = new Thread(new B());
        Thread t3 = new Thread(new C());

        t1.start();
        t2.start();
        t3.start();
    }
}
```
<img width="1076" height="569" alt="image" src="https://github.com/user-attachments/assets/f6ff5b47-0fe4-49d8-aa30-00b4c19def01" />

## assi-13
```
class A extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("A: " + i);
        }
    }
}

class B extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("B: " + i);
        }
    }
}

class C extends Thread {
    public void run() {
        for (int i = 1; i <= 100; i++) {
            System.out.println("C: " + i);
        }
    }
}

public class JoinDemo {
    public static void main(String[] args) throws InterruptedException {
        A t1 = new A();
        B t2 = new B();
        C t3 = new C();

        t1.start();
        t1.join();

        t2.start();
        t2.join();

        t3.start();
    }
}
```
join() method is used to achieve synchronization by making one thread wait for another thread to finish execution.

<img width="1006" height="709" alt="image" src="https://github.com/user-attachments/assets/8aa3fb7b-4a5b-4dbf-ace8-06ba04c6e28f" />
<img width="1216" height="704" alt="image" src="https://github.com/user-attachments/assets/2d3e7d8e-378a-4ca3-b595-cb5719c91f63" />
<img width="1279" height="708" alt="image" src="https://github.com/user-attachments/assets/63fc6813-2d8e-4a6b-96e2-c46db6d2167b" />

## assi-14
```
import javax.swing.*;
import java.awt.event.*;

public class AddSwing {
    public static void main(String[] args) {

        JFrame f = new JFrame("Addition");

        JLabel l1 = new JLabel("Enter First Number:");
        l1.setBounds(30, 30, 150, 30);

        JTextField t1 = new JTextField();
        t1.setBounds(180, 30, 100, 30);

        JLabel l2 = new JLabel("Enter Second Number:");
        l2.setBounds(30, 70, 150, 30);

        JTextField t2 = new JTextField();
        t2.setBounds(180, 70, 100, 30);

        JButton b = new JButton("Add");
        b.setBounds(100, 120, 80, 30);

        JLabel result = new JLabel("Result:");
        result.setBounds(30, 170, 200, 30);

        b.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                int a = Integer.parseInt(t1.getText());
                int b = Integer.parseInt(t2.getText());
                int sum = a + b;
                result.setText("Result: " + sum);
            }
        });

        f.add(l1);
        f.add(t1);
        f.add(l2);
        f.add(t2);
        f.add(b);
        f.add(result);

        f.setSize(350, 300);
        f.setLayout(null);
        f.setVisible(true);
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}
```
<img width="341" height="292" alt="image" src="https://github.com/user-attachments/assets/4ff180f6-10f6-4f8e-b00d-9283fe41e415" />









    
