[Program -1 Wap for calculator](#assi-1)

[Program -2 Wap demonstrating forloop](#assi-2)

[Program -3 Wap for Calculation using methods and additional classes](#assi-3)

[Program -4 Wap to add two distances where each distance is given in m,cm and mm](#assi-4)

[Program -5 Wap to add two distances where each distance is given in m and cm](#assi-5)

[Program -6 Wap to add two times where each time is given in hrs,mins and secs](#assi-6)

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





    
