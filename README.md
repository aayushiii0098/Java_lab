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

[Program-12 Wap using three classes to print 1-100,1-100,1-100 with and without thread and analyse the output and repeat the same program using runnable interface.](#assi-12)

[Program-13 Using the concept of multithreading the output of all three threads must be synchronised (use join method)](#assi-13)

[Program-14 Additon of 2 numbers using swing](#assi-14)

[Program-15 Make a registration form with 10 elements and send data into database (use jdbc connectivity](#assi-15)

[Program-16 Make one calculator in swing](#assi-16)

[Program-17 Matrix additon using swing class](#assi-17)

[Program-18 Create one jframe apply 10 buttons on that after clicking on each button a new structure is created.(Circle,oval,rectangle,etc..](#assi-18)

[Program-19 Just using mouse Event create a frame like paint brush with selection of colour and width](#assi-19)

[Program-20 Create a package of any 5 classes of your chocie and import it](#assi-20)

[Program-21 Create one package and one subpackage import and test it](#assi-21)

[Program-22 Create one small array of size 5 and apply array out of bound exception using try catch and give a proper message in catch and demonstrate the exception exactly in the same faishon demonstrate arithmetic exception](#assi-22)

[Program-23 To test the range of age of one student. wap using user defined exception](#assi-23)

[Program-24 File handling programs(given in ppt)](#assi-24)

[Program-25 Inheritance program using interface and abstract classes](#assi-25)



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

## assi-15
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.sql.*;

public class RegistrationForm extends JFrame implements ActionListener {

    JTextField t1,t2,t3,t4,t5,t6,t7,t8,t9,t10;
    JButton b;

    RegistrationForm() {
        setLayout(new GridLayout(11,2));

        t1=new JTextField();
        t2=new JTextField();
        t3=new JTextField();
        t4=new JTextField();
        t5=new JTextField();
        t6=new JTextField();
        t7=new JTextField();
        t8=new JTextField();
        t9=new JTextField();
        t10=new JTextField();

        add(new JLabel("Name")); add(t1);
        add(new JLabel("Email")); add(t2);
        add(new JLabel("Phone")); add(t3);
        add(new JLabel("Address")); add(t4);
        add(new JLabel("City")); add(t5);
        add(new JLabel("State")); add(t6);
        add(new JLabel("Country")); add(t7);
        add(new JLabel("Username")); add(t8);
        add(new JLabel("Password")); add(t9);
        add(new JLabel("Age")); add(t10);

        b=new JButton("Register");
        add(b);

        b.addActionListener(this);

        setSize(400,400);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        try {
            Class.forName("oracle.jdbc.driver.OracleDriver");

            Connection con = DriverManager.getConnection(
                "jdbc:oracle:thin:@localhost:1521:xe", "swing", "swing123");

            PreparedStatement ps = con.prepareStatement(
                "insert into users values(?,?,?,?,?,?,?,?,?,?)");

            ps.setString(1, t1.getText());
            ps.setString(2, t2.getText());
            ps.setString(3, t3.getText());
            ps.setString(4, t4.getText());
            ps.setString(5, t5.getText());
            ps.setString(6, t6.getText());
            ps.setString(7, t7.getText());
            ps.setString(8, t8.getText());
            ps.setString(9, t9.getText());
            ps.setString(10, t10.getText());

            int x = ps.executeUpdate();

            JOptionPane.showMessageDialog(this, "Inserted: " + x);

            con.close();

        } catch (Exception ex) {
            ex.printStackTrace();
        }
    }

    public static void main(String[] args) {
        new RegistrationForm();
    }
}

```
<img width="1001" height="422" alt="image" src="https://github.com/user-attachments/assets/a4d9912e-8354-4b04-963e-553b7ff1469f" />

<img width="384" height="381" alt="image" src="https://github.com/user-attachments/assets/784e4d7e-f138-4380-8d58-842e4d329313" />


## assi-16
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class CalculatorSwing extends JFrame implements ActionListener {

    JTextField display;
    JButton[] numberButtons = new JButton[10];
    JButton addButton, subButton, mulButton, divButton;
    JButton equalButton, clearButton, deleteButton, dotButton;

    JPanel panel;

    Font myFont = new Font("Arial", Font.BOLD, 22);

    double num1 = 0, num2 = 0, result = 0;
    char operator;

    CalculatorSwing() {
        setTitle("Calculator");
        setSize(420, 550);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLocationRelativeTo(null);
        setLayout(null);
        getContentPane().setBackground(new Color(245, 245, 245));

        display = new JTextField();
        display.setBounds(30, 30, 340, 60);
        display.setFont(new Font("Arial", Font.BOLD, 28));
        display.setEditable(false);
        display.setHorizontalAlignment(JTextField.RIGHT);
        display.setBackground(Color.WHITE);
        display.setForeground(Color.BLACK);
        display.setBorder(BorderFactory.createLineBorder(Color.GRAY, 2));
        add(display);

        addButton = new JButton("+");
        subButton = new JButton("-");
        mulButton = new JButton("*");
        divButton = new JButton("/");
        equalButton = new JButton("=");
        clearButton = new JButton("C");
        deleteButton = new JButton("Del");
        dotButton = new JButton(".");

        JButton[] functionButtons = {
            addButton, subButton, mulButton, divButton,
            equalButton, clearButton, deleteButton, dotButton
        };

        for (int i = 0; i < 10; i++) {
            numberButtons[i] = new JButton(String.valueOf(i));
            numberButtons[i].setFont(myFont);
            numberButtons[i].setFocusable(false);
            numberButtons[i].setBackground(new Color(255, 255, 255));
            numberButtons[i].addActionListener(this);
        }

        for (JButton button : functionButtons) {
            button.setFont(myFont);
            button.setFocusable(false);
            button.setBackground(new Color(220, 220, 220));
            button.addActionListener(this);
        }

        clearButton.setBackground(new Color(255, 153, 153));
        deleteButton.setBackground(new Color(255, 204, 153));
        equalButton.setBackground(new Color(153, 255, 153));
        addButton.setBackground(new Color(204, 229, 255));
        subButton.setBackground(new Color(204, 229, 255));
        mulButton.setBackground(new Color(204, 229, 255));
        divButton.setBackground(new Color(204, 229, 255));

        panel = new JPanel();
        panel.setBounds(30, 120, 340, 320);
        panel.setLayout(new GridLayout(4, 4, 10, 10));
        panel.setBackground(new Color(245, 245, 245));

        panel.add(numberButtons[1]);
        panel.add(numberButtons[2]);
        panel.add(numberButtons[3]);
        panel.add(addButton);

        panel.add(numberButtons[4]);
        panel.add(numberButtons[5]);
        panel.add(numberButtons[6]);
        panel.add(subButton);

        panel.add(numberButtons[7]);
        panel.add(numberButtons[8]);
        panel.add(numberButtons[9]);
        panel.add(mulButton);

        panel.add(dotButton);
        panel.add(numberButtons[0]);
        panel.add(equalButton);
        panel.add(divButton);

        add(panel);

        clearButton.setBounds(30, 460, 160, 40);
        deleteButton.setBounds(210, 460, 160, 40);

        add(clearButton);
        add(deleteButton);

        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {

        for (int i = 0; i < 10; i++) {
            if (e.getSource() == numberButtons[i]) {
                display.setText(display.getText().concat(String.valueOf(i)));
            }
        }

        if (e.getSource() == dotButton) {
            if (!display.getText().contains(".")) {
                display.setText(display.getText().concat("."));
            }
        }

        if (e.getSource() == addButton) {
            if (!display.getText().isEmpty()) {
                num1 = Double.parseDouble(display.getText());
                operator = '+';
                display.setText("");
            }
        }

        if (e.getSource() == subButton) {
            if (!display.getText().isEmpty()) {
                num1 = Double.parseDouble(display.getText());
                operator = '-';
                display.setText("");
            }
        }

        if (e.getSource() == mulButton) {
            if (!display.getText().isEmpty()) {
                num1 = Double.parseDouble(display.getText());
                operator = '*';
                display.setText("");
            }
        }

        if (e.getSource() == divButton) {
            if (!display.getText().isEmpty()) {
                num1 = Double.parseDouble(display.getText());
                operator = '/';
                display.setText("");
            }
        }

        if (e.getSource() == equalButton) {
            if (!display.getText().isEmpty()) {
                num2 = Double.parseDouble(display.getText());

                switch (operator) {
                    case '+':
                        result = num1 + num2;
                        break;
                    case '-':
                        result = num1 - num2;
                        break;
                    case '*':
                        result = num1 * num2;
                        break;
                    case '/':
                        if (num2 == 0) {
                            JOptionPane.showMessageDialog(this, "Cannot divide by zero");
                            display.setText("");
                            return;
                        }
                        result = num1 / num2;
                        break;
                }

                if (result == (int) result) {
                    display.setText(String.valueOf((int) result));
                } else {
                    display.setText(String.valueOf(result));
                }

                num1 = result;
            }
        }

        if (e.getSource() == clearButton) {
            display.setText("");
            num1 = 0;
            num2 = 0;
            result = 0;
        }

        if (e.getSource() == deleteButton) {
            String text = display.getText();
            if (!text.isEmpty()) {
                display.setText(text.substring(0, text.length() - 1));
            }
        }
    }

    public static void main(String[] args) {
        new CalculatorSwing();
    }
}
```
<img width="312" height="421" alt="image" src="https://github.com/user-attachments/assets/77e274a7-e126-443e-a852-cfc7a0038821" />

## assi-17
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class MatrixAdditionSwing extends JFrame implements ActionListener {

    JTextField[][] matrixA = new JTextField[3][3];
    JTextField[][] matrixB = new JTextField[3][3];
    JTextField[][] resultMatrix = new JTextField[3][3];

    JButton addButton, clearButton;
    JLabel titleLabel, labelA, labelB, labelResult;

    Font titleFont = new Font("Arial", Font.BOLD, 24);
    Font labelFont = new Font("Arial", Font.BOLD, 18);
    Font fieldFont = new Font("Arial", Font.PLAIN, 18);

    MatrixAdditionSwing() {
        setTitle("Matrix Addition Using Swing");
        setSize(850, 600);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLocationRelativeTo(null);
        setLayout(null);
        getContentPane().setBackground(new Color(245, 248, 255));

        titleLabel = new JLabel("Matrix Addition Calculator");
        titleLabel.setFont(titleFont);
        titleLabel.setBounds(260, 20, 350, 40);
        titleLabel.setForeground(new Color(30, 60, 120));
        add(titleLabel);

        labelA = new JLabel("Matrix A");
        labelA.setFont(labelFont);
        labelA.setBounds(120, 80, 120, 30);
        add(labelA);

        labelB = new JLabel("Matrix B");
        labelB.setFont(labelFont);
        labelB.setBounds(360, 80, 120, 30);
        add(labelB);

        labelResult = new JLabel("Result Matrix");
        labelResult.setFont(labelFont);
        labelResult.setBounds(600, 80, 150, 30);
        add(labelResult);

        createMatrix(matrixA, 70, 130);
        createMatrix(matrixB, 320, 130);
        createResultMatrix(resultMatrix, 570, 130);

        addButton = new JButton("Add Matrices");
        addButton.setBounds(250, 420, 150, 45);
        addButton.setFont(new Font("Arial", Font.BOLD, 16));
        addButton.setBackground(new Color(153, 255, 153));
        addButton.addActionListener(this);
        add(addButton);

        clearButton = new JButton("Clear");
        clearButton.setBounds(430, 420, 150, 45);
        clearButton.setFont(new Font("Arial", Font.BOLD, 16));
        clearButton.setBackground(new Color(255, 204, 153));
        clearButton.addActionListener(this);
        add(clearButton);

        JLabel note = new JLabel("Enter integer values in both matrices and click Add Matrices.");
        note.setFont(new Font("Arial", Font.ITALIC, 15));
        note.setBounds(180, 490, 500, 30);
        note.setForeground(Color.DARK_GRAY);
        add(note);

        setVisible(true);
    }

    void createMatrix(JTextField[][] matrix, int startX, int startY) {
        int width = 50;
        int height = 40;
        int gap = 10;

        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                matrix[i][j] = new JTextField();
                matrix[i][j].setBounds(startX + j * (width + gap), startY + i * (height + gap), width, height);
                matrix[i][j].setFont(fieldFont);
                matrix[i][j].setHorizontalAlignment(JTextField.CENTER);
                matrix[i][j].setBackground(Color.WHITE);
                matrix[i][j].setBorder(BorderFactory.createLineBorder(new Color(100, 100, 100), 2));
                add(matrix[i][j]);
            }
        }
    }

    void createResultMatrix(JTextField[][] matrix, int startX, int startY) {
        int width = 50;
        int height = 40;
        int gap = 10;

        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                matrix[i][j] = new JTextField();
                matrix[i][j].setBounds(startX + j * (width + gap), startY + i * (height + gap), width, height);
                matrix[i][j].setFont(fieldFont);
                matrix[i][j].setHorizontalAlignment(JTextField.CENTER);
                matrix[i][j].setEditable(false);
                matrix[i][j].setBackground(new Color(230, 255, 230));
                matrix[i][j].setBorder(BorderFactory.createLineBorder(new Color(0, 128, 0), 2));
                add(matrix[i][j]);
            }
        }
    }

    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == addButton) {
            try {
                for (int i = 0; i < 3; i++) {
                    for (int j = 0; j < 3; j++) {
                        int a = Integer.parseInt(matrixA[i][j].getText());
                        int b = Integer.parseInt(matrixB[i][j].getText());
                        int sum = a + b;
                        resultMatrix[i][j].setText(String.valueOf(sum));
                    }
                }
            } catch (NumberFormatException ex) {
                JOptionPane.showMessageDialog(this, "Please enter valid integer values in all boxes.");
            }
        }

        if (e.getSource() == clearButton) {
            for (int i = 0; i < 3; i++) {
                for (int j = 0; j < 3; j++) {
                    matrixA[i][j].setText("");
                    matrixB[i][j].setText("");
                    resultMatrix[i][j].setText("");
                }
            }
        }
    }

    public static void main(String[] args) {
        new MatrixAdditionSwing();
    }
}
```
<img width="623" height="465" alt="image" src="https://github.com/user-attachments/assets/dae5ed82-bd96-4820-ba20-f5214fe26c5a" />

## assi-18
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class ShapeButtonsFrame extends JFrame implements ActionListener {

    JButton circleBtn, ovalBtn, rectBtn, squareBtn, lineBtn;
    JButton arcBtn, triangleBtn, diamondBtn, polygonBtn, fillOvalBtn;

    DrawingPanel drawingPanel;
    String currentShape = "";

    Font btnFont = new Font("Arial", Font.BOLD, 14);

    ShapeButtonsFrame() {
        setTitle("Shape Drawing Using 10 Buttons");
        setSize(900, 600);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLocationRelativeTo(null);
        setLayout(new BorderLayout());

        JPanel topPanel = new JPanel();
        topPanel.setLayout(new GridLayout(2, 5, 10, 10));
        topPanel.setBackground(new Color(240, 248, 255));
        topPanel.setBorder(BorderFactory.createEmptyBorder(15, 15, 15, 15));

        circleBtn = createButton("Circle", new Color(255, 204, 204));
        ovalBtn = createButton("Oval", new Color(255, 229, 204));
        rectBtn = createButton("Rectangle", new Color(255, 255, 204));
        squareBtn = createButton("Square", new Color(204, 255, 204));
        lineBtn = createButton("Line", new Color(204, 255, 255));
        arcBtn = createButton("Arc", new Color(204, 229, 255));
        triangleBtn = createButton("Triangle", new Color(229, 204, 255));
        diamondBtn = createButton("Diamond", new Color(255, 204, 229));
        polygonBtn = createButton("Polygon", new Color(220, 220, 220));
        fillOvalBtn = createButton("Fill Oval", new Color(255, 180, 180));

        topPanel.add(circleBtn);
        topPanel.add(ovalBtn);
        topPanel.add(rectBtn);
        topPanel.add(squareBtn);
        topPanel.add(lineBtn);
        topPanel.add(arcBtn);
        topPanel.add(triangleBtn);
        topPanel.add(diamondBtn);
        topPanel.add(polygonBtn);
        topPanel.add(fillOvalBtn);

        drawingPanel = new DrawingPanel();
        drawingPanel.setBackground(Color.WHITE);

        JLabel heading = new JLabel("Click any button to draw a shape", JLabel.CENTER);
        heading.setFont(new Font("Arial", Font.BOLD, 24));
        heading.setForeground(new Color(40, 40, 120));
        heading.setBorder(BorderFactory.createEmptyBorder(10, 10, 10, 10));

        add(heading, BorderLayout.NORTH);
        add(topPanel, BorderLayout.SOUTH);
        add(drawingPanel, BorderLayout.CENTER);

        setVisible(true);
    }

    JButton createButton(String text, Color color) {
        JButton btn = new JButton(text);
        btn.setFont(btnFont);
        btn.setBackground(color);
        btn.setFocusable(false);
        btn.addActionListener(this);
        return btn;
    }

    public void actionPerformed(ActionEvent e) {
        currentShape = e.getActionCommand();
        drawingPanel.repaint();
    }

    class DrawingPanel extends JPanel {
        protected void paintComponent(Graphics g) {
            super.paintComponent(g);

            Graphics2D g2 = (Graphics2D) g;
            g2.setStroke(new BasicStroke(3));
            g2.setColor(new Color(50, 50, 50));

            if (currentShape.equals("Circle")) {
                g2.drawOval(320, 120, 150, 150);
            }
            else if (currentShape.equals("Oval")) {
                g2.drawOval(280, 140, 220, 120);
            }
            else if (currentShape.equals("Rectangle")) {
                g2.drawRect(280, 140, 220, 120);
            }
            else if (currentShape.equals("Square")) {
                g2.drawRect(320, 120, 150, 150);
            }
            else if (currentShape.equals("Line")) {
                g2.drawLine(250, 100, 550, 250);
            }
            else if (currentShape.equals("Arc")) {
                g2.drawArc(280, 120, 220, 150, 0, 180);
            }
            else if (currentShape.equals("Triangle")) {
                int[] x = {390, 300, 480};
                int[] y = {100, 250, 250};
                g2.drawPolygon(x, y, 3);
            }
            else if (currentShape.equals("Diamond")) {
                int[] x = {390, 320, 390, 460};
                int[] y = {100, 180, 260, 180};
                g2.drawPolygon(x, y, 4);
            }
            else if (currentShape.equals("Polygon")) {
                int[] x = {330, 380, 450, 430, 350, 300};
                int[] y = {120, 90, 130, 210, 240, 180};
                g2.drawPolygon(x, y, 6);
            }
            else if (currentShape.equals("Fill Oval")) {
                g2.setColor(new Color(255, 120, 120));
                g2.fillOval(300, 130, 200, 120);
            }
        }
    }

    public static void main(String[] args) {
        new ShapeButtonsFrame();
    }
}
```
<img width="664" height="443" alt="image" src="https://github.com/user-attachments/assets/6d63966f-0c9c-4e9c-8240-3ce02614a7f8" />


## assi-19
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.util.ArrayList;

public class PaintBrushApp extends JFrame {

    JComboBox<String> colorBox;
    JComboBox<Integer> sizeBox;
    JButton clearButton;

    DrawPanel drawPanel;

    Color selectedColor = Color.BLACK;
    int brushSize = 5;

    ArrayList<BrushPoint> points = new ArrayList<>();

    PaintBrushApp() {
        setTitle("Paint Brush Using Mouse Events");
        setSize(900, 600);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLocationRelativeTo(null);
        setLayout(new BorderLayout());

        JPanel topPanel = new JPanel();
        topPanel.setBackground(new Color(230, 240, 255));
        topPanel.setLayout(new FlowLayout(FlowLayout.LEFT, 20, 10));

        JLabel titleLabel = new JLabel("Simple Paint Brush");
        titleLabel.setFont(new Font("Arial", Font.BOLD, 22));
        titleLabel.setForeground(new Color(30, 60, 120));

        JLabel colorLabel = new JLabel("Select Color:");
        colorLabel.setFont(new Font("Arial", Font.BOLD, 16));

        String[] colors = {"Black", "Red", "Blue", "Green", "Pink", "Orange"};
        colorBox = new JComboBox<>(colors);
        colorBox.setFont(new Font("Arial", Font.PLAIN, 15));

        JLabel sizeLabel = new JLabel("Brush Width:");
        sizeLabel.setFont(new Font("Arial", Font.BOLD, 16));

        Integer[] sizes = {2, 4, 6, 8, 10, 12, 15, 20};
        sizeBox = new JComboBox<>(sizes);
        sizeBox.setFont(new Font("Arial", Font.PLAIN, 15));

        clearButton = new JButton("Clear");
        clearButton.setFont(new Font("Arial", Font.BOLD, 15));
        clearButton.setBackground(new Color(255, 180, 180));

        topPanel.add(titleLabel);
        topPanel.add(colorLabel);
        topPanel.add(colorBox);
        topPanel.add(sizeLabel);
        topPanel.add(sizeBox);
        topPanel.add(clearButton);

        drawPanel = new DrawPanel();
        drawPanel.setBackground(Color.WHITE);

        add(topPanel, BorderLayout.NORTH);
        add(drawPanel, BorderLayout.CENTER);

        colorBox.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String colorName = (String) colorBox.getSelectedItem();

                if (colorName.equals("Black")) {
                    selectedColor = Color.BLACK;
                } else if (colorName.equals("Red")) {
                    selectedColor = Color.RED;
                } else if (colorName.equals("Blue")) {
                    selectedColor = Color.BLUE;
                } else if (colorName.equals("Green")) {
                    selectedColor = Color.GREEN;
                } else if (colorName.equals("Pink")) {
                    selectedColor = Color.PINK;
                } else if (colorName.equals("Orange")) {
                    selectedColor = Color.ORANGE;
                }
            }
        });

        sizeBox.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                brushSize = (Integer) sizeBox.getSelectedItem();
            }
        });

        clearButton.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                points.clear();
                drawPanel.repaint();
            }
        });

        setVisible(true);
    }

    class BrushPoint {
        int x, y, size;
        Color color;

        BrushPoint(int x, int y, Color color, int size) {
            this.x = x;
            this.y = y;
            this.color = color;
            this.size = size;
        }
    }

    class DrawPanel extends JPanel implements MouseMotionListener, MouseListener {

        DrawPanel() {
            addMouseMotionListener(this);
            addMouseListener(this);
        }

        public void mouseDragged(MouseEvent e) {
            points.add(new BrushPoint(e.getX(), e.getY(), selectedColor, brushSize));
            repaint();
        }

        public void paintComponent(Graphics g) {
            super.paintComponent(g);

            for (BrushPoint p : points) {
                g.setColor(p.color);
                g.fillOval(p.x, p.y, p.size, p.size);
            }
        }

        public void mouseMoved(MouseEvent e) { }
        public void mouseClicked(MouseEvent e) { }
        public void mousePressed(MouseEvent e) { }
        public void mouseReleased(MouseEvent e) { }
        public void mouseEntered(MouseEvent e) { }
        public void mouseExited(MouseEvent e) { }
    }

    public static void main(String[] args) {
        new PaintBrushApp();
    }
}
```
<img width="885" height="590" alt="image" src="https://github.com/user-attachments/assets/0c147ef9-96de-4ff3-87c4-9bb6cbdc2475" />


## assi-20
```
package mypack;

public class Addition {
    public int add(int a, int b) {
        return a + b;
    }
}

package mypack;

public class Subtraction {
    public int subtract(int a, int b) {
        return a - b;
    }
}

package mypack;

public class Multiplication {
    public int multiply(int a, int b) {
        return a * b;
    }
}

package mypack;

public class Division {
    public int divide(int a, int b) {
        return a / b;
    }
}
import mypack.Addition;
import mypack.Subtraction;
import mypack.Multiplication;
import mypack.Division;
import mypack.Message;

public class TestPackage {
    public static void main(String[] args) {
        Addition a = new Addition();
        Subtraction s = new Subtraction();
        Multiplication m = new Multiplication();
        Division d = new Division();
        Message msg = new Message();

        System.out.println("Addition = " + a.add(20, 10));
        System.out.println("Subtraction = " + s.subtract(20, 10));
        System.out.println("Multiplication = " + m.multiply(20, 10));
        System.out.println("Division = " + d.divide(20, 10));
        msg.showMessage();
    }
}
```
<img width="304" height="79" alt="image" src="https://github.com/user-attachments/assets/37e5d39b-4148-4176-be6e-b8295eaa1787" />


## assi-21
```
// in package folder
package college;

public class Student {
    public void showStudent() {
        System.out.println("This is Student class from main package.");
    }
}
//  in info folder
package college.info;

public class Address {
    public void showAddress() {
        System.out.println("This is Address class from sub-package.");
    }
}
// in java lab folder
import college.Student;
import college.info.Address;

public class TestSubPackage {
    public static void main(String[] args) {
        Student s = new Student();
        Address a = new Address();

        s.showStudent();
        a.showAddress();
    }
}
```
<img width="324" height="46" alt="image" src="https://github.com/user-attachments/assets/ddb816ab-b65f-4476-8313-c6e36fa494d9" />


## assi-22
```

public class ExceptionDemo {
    public static void main(String[] args) {

        // ArrayIndexOutOfBoundsException demonstration
        try {
            int[] arr = new int[5];

            arr[0] = 10;
            arr[1] = 20;
            arr[2] = 30;
            arr[3] = 40;
            arr[4] = 50;

            System.out.println("Trying to access 6th element...");
            System.out.println(arr[5]);   // invalid index
        }
        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("ArrayIndexOutOfBoundsException caught!");
            System.out.println("Message: Array index is out of range.");
        }

        System.out.println();

        // ArithmeticException demonstration
        try {
            int a = 10;
            int b = 0;
            int c = a / b;

            System.out.println("Result = " + c);
        }
        catch (ArithmeticException e) {
            System.out.println("ArithmeticException caught!");
            System.out.println("Message: Division by zero is not allowed.");
        }

        System.out.println();
        System.out.println("Program ended successfully after handling exceptions.");
    }
}
```
<img width="258" height="91" alt="image" src="https://github.com/user-attachments/assets/8ad1cfc1-464c-411c-a0a5-891956b9fcf9" />


## assi-23
```
import java.util.Scanner;
class InvalidAgeException extends Exception {

    public InvalidAgeException(String message) {
        super(message);
    }
}

public class StudentAgeTest {

    // method to check age
    static void checkAge(int age) throws InvalidAgeException {
        if (age < 5 || age > 25) {
            throw new InvalidAgeException("Invalid Age! Age must be between 5 and 25.");
        } else {
            System.out.println("Valid student age.");
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            System.out.print("Enter student age: ");
            int age = sc.nextInt();

            checkAge(age);   // calling method

        } catch (InvalidAgeException e) {
            System.out.println("User Defined Exception Caught!");
            System.out.println("Message: " + e.getMessage());
        } catch (Exception e) {
            System.out.println("Please enter a valid number.");
        }

        sc.close();
    }
}
```
<img width="272" height="44" alt="image" src="https://github.com/user-attachments/assets/bf492864-d64c-4e07-867d-e97e80c685fe" />


## assi-24
```
import java.io.*;

public class ByteStreamDemo {
    public static void main(String[] args) {
        try {
            FileOutputStream fos = new FileOutputStream("bytefile.txt");
            fos.write("Hello Byte Stream".getBytes());
            fos.close();

            FileInputStream fis = new FileInputStream("bytefile.txt");

            int b;
            System.out.println("Data from file:");

            while ((b = fis.read()) != -1) {
                System.out.print((char) b);
            }

            fis.close();
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
<img width="415" height="43" alt="image" src="https://github.com/user-attachments/assets/187836cb-4cbf-4ced-8ac7-b92e768e9240" />


```
import java.io.*;

public class PrimitiveStreamDemo {
    public static void main(String[] args) {
        try {
            DataOutputStream dos = new DataOutputStream(new FileOutputStream("student.dat"));

            dos.writeInt(101);
            dos.writeUTF("Aayushi");
            dos.writeDouble(95.5);
            dos.writeBoolean(true);

            dos.close();

            DataInputStream dis = new DataInputStream(new FileInputStream("student.dat"));

            int rollNo = dis.readInt();
            String name = dis.readUTF();
            double marks = dis.readDouble();
            boolean passed = dis.readBoolean();

            dis.close();

            System.out.println("Roll No: " + rollNo);
            System.out.println("Name: " + name);
            System.out.println("Marks: " + marks);
            System.out.println("Passed: " + passed);

        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
<img width="236" height="67" alt="image" src="https://github.com/user-attachments/assets/1c86936b-7625-4395-a786-ec7193f2fb1d" />


```
import java.io.*;

public class CharacterStreamDemo {
    public static void main(String[] args) {
        try {
            FileWriter fw = new FileWriter("charfile.txt");
            fw.write("Hello Java File Handling");
            fw.close();

            FileReader fr = new FileReader("charfile.txt");

            int ch;
            System.out.println("Data from file:");

            while ((ch = fr.read()) != -1) {
                System.out.print((char) ch);
            }

            fr.close();
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
<img width="220" height="41" alt="image" src="https://github.com/user-attachments/assets/4b3da561-a3f8-468e-8c84-2390874c2a5d" />


```
import java.io.*;

public class CharFileCopy {
    public static void main(String[] args) {
        try {
            FileReader fr = new FileReader("source.txt");
            FileWriter fw = new FileWriter("dest_char.txt");

            int ch;

            while ((ch = fr.read()) != -1) {
                fw.write(ch);
            }

            fr.close();
            fw.close();

            System.out.println("File copied using character stream.");

        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
<img width="713" height="29" alt="image" src="https://github.com/user-attachments/assets/1730d944-b4c7-4a1e-9668-c8f1075c9d19" />


```
import java.io.*;

public class ByteFileCopy {
    public static void main(String[] args) {
        try {
            FileInputStream fis = new FileInputStream("source.txt");
            FileOutputStream fos = new FileOutputStream("dest_byte.txt");

            int b;

            while ((b = fis.read()) != -1) {
                fos.write(b);
            }

            fis.close();
            fos.close();

            System.out.println("File copied using byte stream.");

        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
<img width="750" height="26" alt="image" src="https://github.com/user-attachments/assets/125f9ba1-56f0-401b-a297-741af10187ab" />


## assi-25
```
interface Printable {
    void print();
}

abstract class Shape {
    abstract void draw();

    void message() {
        System.out.println("This is an abstract class.");
    }
}

class Animal {
    void eat() {
        System.out.println("Animal eats food.");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks.");
    }
}

class Document implements Printable {
    public void print() {
        System.out.println("Printing document using interface.");
    }
}

class Circle extends Shape {
    void draw() {
        System.out.println("Drawing a circle.");
    }
}


public class ConceptDemo {
    public static void main(String[] args) {

        System.out.println("---- INHERITANCE ----");
        Dog d = new Dog();
        d.eat();
        d.bark();

        System.out.println();

        System.out.println("---- INTERFACE ----");
        Document doc = new Document();
        doc.print();

        System.out.println();

        System.out.println("---- ABSTRACT CLASS ----");
        Circle c = new Circle();
        c.draw();
        c.message();
    }
}
```
<img width="237" height="107" alt="image" src="https://github.com/user-attachments/assets/a2979360-5c8c-410c-9ea8-4e5eb9a3eec4" />










    
