[Program -1 Wap for calculator](#assi-1)

[Program -2 Wap demonstrating forloop](#assi-2)



##assi-1
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



##assi-2
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


    
