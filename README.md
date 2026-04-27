## INDEX

[PROGRAM-1 WRITE A PROGRAM FOR ADDITION, SUBTRACTION, MULTIPLICATION AND DIVISION USING CLASSES AND OBJECTS](#assi-1)

[PROGRAM-2 WRITE A PROGRAM FOR THE ADDITION OF 2 DISTANCE WHERE EACH DISTANCE IS GIVEN IN METER, CENTIMETER AND MILLIMETER](#assi-2)

[PROGRAM-3 WRITE A PROGRAM FOR THE ADDITION OF TWO TIMES WHERE EACH TIME IS GIVEN IN HOURS, MINUTES AND SECONDS USING CLASSES AND OBJECTS](#assi-3)

[PROGRAM-4 WRITE A PROGRAM FOR THE ADDITION OF TWO DISTANCES WHERE EACH DISTANCE IS GIVEN IN METER AND CENTIMETER](#assi-4)

[PROGRAM-5 WRITE A PROGRAM USING OBJECTS AND CLASSES TO DO REVERSE OF 1-D ARRAY](#assi-5)

[PROGRAM-6 WRITE A CLASS FOR IMPORTANT OPERATION OF MATRIX(3X3): TRANSPOSE, SUM, MULTUPLY, SUM OF ROWS, SUM OF COLUMNS AND SUM OF DIAGONALS](#assi-6)

[PROGRAM-7 COLLECT THE CODE OF C LANGUAGE OF ANY 5 OPERATION AND CONVERT THE LOGIC INTO JAVA OOPS FASHION](#assi-7)

[PROGRAM-8 DEMONSTRATE ALL THREE TYPES OF INHERITANCE WITH MINIMAL SIZE OF CODE](#assi-8)

[PROGRAM-9 WRITE A PROGRAM USING THREE CLASSES TO PRINT 1-100, 1-100, 1-100 WITH AND WITHOUT THREAD AND ANALYSE THE OUTPUT AND REPEAT THE SAME PROGRAM USING RUNNABLE INTERFACE.](#assi-9)

[PROGRAM-10 USING THE CONCEPT OF MULTITHREADING THE OUTPUT OF ALL THREE THREADS MUST BE SYNCHRONISED(USE JOIN METHOD)](#assi-10)

[PROGRAM-11 ADDITION OF 2 NUMBER USING SWING.](#assi-11)

[PROGRAM-12  MAKE A REGISTRATION FORM WITH 10 ELEMENTS AND SEND THE DATA INTO DATABASE(USE JDBC CONNECTIVITY)](#assi-12)

[PROGRAM-13 MAKE ONE CALCULATOR IN SWING.](#assi-13)

[PROGRAM-14 MATRIX ADDITION USING SWING CLASS.](#assi-14)

[PROGRAM-15 CREATE ONE JFRAME APPLY 10 BUTTONS ON THAT AFTER CLICKING ON EACH BUTTON A NEW STRUCTURE IS CREATED.(CIRCLE, OVAL RECTANGLE, ETC..)](#assi-15)

[PROGRAM-16 JUST USING MOUSE EVENT CREATE A FRAME LIKE PAINT BRUSH WITH SELECTION OF COLOUR AND WIDTH.](#assi-16)

[PROGRAM-17 CREATE A PACKAGE AND SUB PACKAGE IMPORT ANDNTEST IT.](#assi-17)

[PROGRAM-18 CREATE ONE PACKAGE AND SUB PACKAGE IMPORT AND TEST IT.](#assi-18)

[PROGRAM-19 CREATE ONE SMALL ARRAY OF SIZE 5 APPLY ARRAY OUT OF BOUNDS EXCEPTION USING TRY CATCH GIVE A PROPER MESSAGE IN CATCH AND DEMONSTRATE THE EXCEPTION EXACTLY IN THE SAME FASHION DEMONSTRATE ARITHMETIC EXCEPTION.](#assi-19)

[PROGRAM-20 TO TEST THE RANGE OF AGE OF ONE STUDENT. WRITE A PROGRAM USING USER DEFINED EXCEPTION.](#assi-20)

[PROGRAM-21 FILE HANDLING PROGRAM(GIVEN IN THE PPT).](#assi-21)

[PROGRAM-22 INHERITANCE PROGRAMS, USING INTERFACE AND ABSTRACT CLASSES.](#assi-22)

## assi-1
```import java.util.Scanner;
class Calculator {
    int add(int a, int b)
    {
        return a + b;
    }
    int subtract(int a, int b)
    {
        return a - b;
    }
    int multiply(int a, int b)
    {
        return a * b;
    }
    double divide(int a, int b)
    {
        return (double) a / b;
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Calculator obj = new Calculator();
        int a, b;
        System.out.print("Enter first number: ");
        a = sc.nextInt();
        System.out.print("Enter second number: ");
        b = sc.nextInt();
        System.out.println("Addition = " + obj.add(a, b));
        System.out.println("Subtraction = " + obj.subtract(a, b));
        System.out.println("Multiplication = " + obj.multiply(a, b));
        System.out.println("Division = " + obj.divide(a, b));
    }
}
```
<img width="885" height="262" alt="image" src="https://github.com/user-attachments/assets/d276f316-a796-4e0c-a7c4-d84b2b32d9e3" />


## assi-2
```import java.util.Scanner;
class Distance {
    int m, cm, mm;
    void add(Distance d1, Distance d2) {
        mm = d1.mm + d2.mm;
        cm = d1.cm + d2.cm + mm / 10;
        mm = mm % 10;
        m = d1.m + d2.m + cm / 100;
        cm = cm % 100;
    }
    void display() {
        System.out.println("Total Distance = " + m + " m " + cm + " cm " + mm + " mm");
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Distance d1 = new Distance();
        Distance d2 = new Distance();
        Distance d3 = new Distance();
        System.out.print("Enter first distance (m,cm,mm): ");
        d1.m = sc.nextInt();
        d1.cm = sc.nextInt();
        d1.mm = sc.nextInt();
        System.out.print("Enter second distance (m,cm,mm): ");
        d2.m = sc.nextInt();
        d2.cm = sc.nextInt();
        d2.mm = sc.nextInt();
        d3.add(d1, d2);
        d3.display();
    }
}
```
<img width="738" height="147" alt="image" src="https://github.com/user-attachments/assets/c1e9c1a2-a02b-4521-93da-702353028657" />

## assi-3
```import java.util.Scanner;
class Time {
    int h, m, s;
    void add(Time t1, Time t2) {
        s = t1.s + t2.s;
        m = t1.m + t2.m + s / 60;
        s = s % 60;
        h = t1.h + t2.h + m / 60;
        m = m % 60;
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Time t1 = new Time();
        Time t2 = new Time();
        Time result = new Time();
        System.out.print("Enter first time (h m s): ");
        t1.h = sc.nextInt();
        t1.m = sc.nextInt();
        t1.s = sc.nextInt();
        System.out.print("Enter second time (h m s): ");
        t2.h = sc.nextInt();
        t2.m = sc.nextInt();
        t2.s = sc.nextInt();
        result.add(t1, t2);
        System.out.println("Total Time = " + result.h + " hr " + result.m + " min " + result.s          + " sec");
    }
}
```
<img width="718" height="146" alt="image" src="https://github.com/user-attachments/assets/50a400c2-eb13-48c2-87bb-9ae37e786584" />

## assi-4
```import java.util.Scanner;
class Distance {
    int m, cm;

    void add(Distance d1, Distance d2) {
        cm = d1.cm + d2.cm;
        m = d1.m + d2.m + cm / 100;
        cm = cm % 100;
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Distance d1 = new Distance();
        Distance d2 = new Distance();
        Distance result = new Distance();
        System.out.print("Enter first distance (m cm): ");
        d1.m = sc.nextInt();
        d1.cm = sc.nextInt();
        System.out.print("Enter second distance (m cm): ");
        d2.m = sc.nextInt();
        d2.cm = sc.nextInt();
        result.add(d1, d2);
        System.out.println("Total Distance = " + result.m + " m " + result.cm + " cm");
    }
}
```
<img width="728" height="147" alt="image" src="https://github.com/user-attachments/assets/ae2454a1-2bcb-49bc-898a-d93781b04848" />

## assi-5
```import java.util.Scanner;
class ArrayReverse {
    void reverse(int arr[], int n) {
        for(int i = n-1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayReverse obj = new ArrayReverse();
        System.out.print("Enter size of array: ");
        int n = sc.nextInt();
        int arr[] = new int[n];
        System.out.println("Enter array elements:");
        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        System.out.println("Reversed array:");
        obj.reverse(arr, n);
    }
}
```
<img width="965" height="445" alt="image" src="https://github.com/user-attachments/assets/8cd00784-c7a4-49fd-92f8-7c90cb6f2eef" />

## assi-6
```import java.util.Scanner;
class Matrix {
    int a[][] = new int[3][3];
    // Input method
    void input() {
        Scanner sc = new Scanner(System.in);
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                a[i][j] = sc.nextInt();
            }
        }
    }
    // Output method
    void display() {
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                System.out.print(a[i][j] + " ");
            }
            System.out.println();
        }
    }
    // Transpose
    void transpose() {
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                System.out.print(a[j][i] + " ");
            }
            System.out.println();
        }
    }
    // Sum of matrices
    void sum(Matrix b) {
        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                System.out.print((a[i][j] + b.a[i][j]) + " ");
            }
            System.out.println();
        }
    }
    // Multiplication
    void multiply(Matrix b) {
        int c[][] = new int[3][3];

        for(int i=0;i<3;i++){
            for(int j=0;j<3;j++){
                for(int k=0;k<3;k++){
                    c[i][j] += a[i][k] * b.a[k][j];
                }
                System.out.print(c[i][j] + " ");
            }
            System.out.println();
        }
    }
    // Sum of rows
    void rowSum() {
        for(int i=0;i<3;i++){
            int sum = 0;
            for(int j=0;j<3;j++){
                sum += a[i][j];
            }
            System.out.println("Row " + (i+1) + " Sum = " + sum);
        }
    }
    // Sum of columns
    void columnSum() {
        for(int j=0;j<3;j++){
            int sum = 0;
            for(int i=0;i<3;i++){
                sum += a[i][j];
            }
            System.out.println("Column " + (j+1) + " Sum = " + sum);
        }
    }
    // Sum of diagonals
    void diagonalSum() {
        int d1=0, d2=0;
        for(int i=0;i<3;i++)
        {
            d1 += a[i][i];
            d2 += a[i][2-i];
        }
        System.out.println("Main Diagonal Sum = " + d1);
        System.out.println("Other Diagonal Sum = " + d2);
    }
}
public class Main {
    public static void main(String[] args) {
        Matrix m1 = new Matrix();
        Matrix m2 = new Matrix();
        System.out.println("Enter First Matrix (3x3):");
        m1.input();
        System.out.println("Enter Second Matrix (3x3):");
        m2.input();
        System.out.println("Matrix 1:");
        m1.display();
        System.out.println("Transpose:");
        m1.transpose();
        System.out.println("Sum of Matrices:");
        m1.sum(m2);
        System.out.println("Multiplication:");
        m1.multiply(m2);
        System.out.println("Row Sum:");
        m1.rowSum();
        System.out.println("Column Sum:");
        m1.columnSum();
        System.out.println("Diagonal Sum:");
        m1.diagonalSum();
    }
}
```
<img width="619" height="790" alt="image" src="https://github.com/user-attachments/assets/929fcd21-14e2-44e8-8e75-6828beaf5fb3" />

## assi-7
```import java.util.Scanner;
class Ops {
    void factorial(int n){
        int f=1;
        for(int i=1;i<=n;i++) f*=i;
        System.out.println("Factorial = "+f);
    }
    void fibonacci(int n){
        int a=0,b=1,c;
        System.out.print("Fibonacci: ");
        for(int i=1;i<=n;i++){
            System.out.print(a+" ");
            c=a+b; a=b; b=c;
        }
        System.out.println();
    }
    void palindrome(int n){
        int t=n,r,rev=0;
        while(n>0){
            r=n%10;
            rev=rev*10+r;
            n/=10;
        }
        if(t==rev) System.out.println("Palindrome");
        else System.out.println("Not Palindrome");
    }
    void armstrong(int n){
        int t=n,r,sum=0;
        while(n>0){
            r=n%10;
            sum+=r*r*r;
            n/=10;
        }
        if(sum==t) System.out.println("Armstrong");
        else System.out.println("Not Armstrong");
    }
    void pattern(int n){
        for(int i=1;i<=n;i++){
            for(int j=1;j<=i;j++)
                System.out.print("*");
            System.out.println();
        }
    }
}
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        Ops o1=new Ops();
        int n;
        System.out.print("Enter number for factorial: ");
        n=sc.nextInt();
        o1.factorial(n);
        System.out.print("Enter terms for fibonacci: ");
        n=sc.nextInt();
        o1.fibonacci(n);
        System.out.print("Enter number for palindrome check: ");
        n=sc.nextInt();
        o1.palindrome(n);
        System.out.print("Enter number for armstrong check: ");
        n=sc.nextInt();
        o1.armstrong(n);
        System.out.print("Enter rows for pattern: ");
        n=sc.nextInt();
        o1.pattern(n);
    }
}
```
<img width="754" height="394" alt="image" src="https://github.com/user-attachments/assets/218927bc-40f2-40f2-9e20-807547526632" />

## assi-8
```
class A {
    void showA() {
        System.out.println("Class A");
    }
}
// Single Inheritance
class B extends A {
    void showB() {
        System.out.println("Class B (Single Inheritance)");
    }
}
// Multiple Inheritance
class C extends B {
    void showC() {
        System.out.println("Class C (Acts like Multiple/Multilevel)");
    }
}
// Hierarchical Inheritance
class D extends A {
    void showD() {
        System.out.println("Class D (Hierarchical Inheritance)");
    }
}
public class Main {
    public static void main(String[] args) {
        // Single
        B obj1 = new B();
        obj1.showA();
        obj1.showB();
        // Multilevel
        C obj2 = new C();
        obj2.showA();
        obj2.showB();
        obj2.showC();
        // Hierarchical
        D obj3 = new D();
        obj3.showA();
        obj3.showD();
    }
}
```
<img width="790" height="260" alt="image" src="https://github.com/user-attachments/assets/b9c02b38-a32f-495e-98ee-e6f7650bbdf6" />

## assi-10
```
class MyThread extends Thread {

    String name;

    MyThread(String name) {
        this.name = name;
    }

    public void run() {
        for (int i = 1; i <= 5; i++) {
            System.out.println(name + " -> " + i);
            try {
                Thread.sleep(500); // delay for visibility
            } catch (Exception e) {
                System.out.println(e);
            }
        }
    }
}

public class ThreadJoinDemo {

    public static void main(String[] args) {

        MyThread t1 = new MyThread("Thread-1");
        MyThread t2 = new MyThread("Thread-2");
        MyThread t3 = new MyThread("Thread-3");

        try {
            t1.start();
            t1.join();   // wait for t1 to finish

            t2.start();
            t2.join();   // wait for t2 to finish

            t3.start();
            t3.join();   // wait for t3 to finish

        } catch (Exception e) {
            System.out.println(e);
        }

        System.out.println("All threads completed.");
    }
}
```
<img width="717" height="440" alt="image" src="https://github.com/user-attachments/assets/899e0b0f-ae68-4116-b5b0-d3410b8661ef" />

## assi-11

```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class AdditionGUI extends JFrame implements ActionListener {

    JTextField num1, num2, result;
    JButton addBtn;

    public AdditionGUI() {

        setTitle("Addition of Two Numbers");
        setSize(500, 250); 
        setLayout(new GridLayout(4, 2, 15, 15)); 
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        num1 = new JTextField();
        num2 = new JTextField();
        result = new JTextField();
        result.setEditable(false);

        addBtn = new JButton("Add");
        addBtn.setPreferredSize(new Dimension(120, 40));
        addBtn.addActionListener(this);

        add(new JLabel("Number 1:"));
        add(num1);

        add(new JLabel("Number 2:"));
        add(num2);

        add(new JLabel("Result:"));
        add(result);

        add(new JLabel(""));
        add(addBtn);

        setLocationRelativeTo(null); 
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        try {
            int a = Integer.parseInt(num1.getText());
            int b = Integer.parseInt(num2.getText());

            result.setText(String.valueOf(a + b));

        } catch (Exception ex) {
            JOptionPane.showMessageDialog(this, "Enter valid numbers!");
        }
    }

    public static void main(String[] args) {
        new AdditionGUI();
    }
}
```
<img width="476" height="236" alt="image" src="https://github.com/user-attachments/assets/09a6c9a9-829e-4c51-b663-3b3a76fd472c" />

## assi-12

```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.sql.*;

public class RegistrationForm extends JFrame implements ActionListener {

    JTextField firstNameField, lastNameField, ageField, emailField, phoneField, cityField;
    JTextArea addressArea;
    JRadioButton maleBtn, femaleBtn;
    JComboBox<String> courseBox, branchBox;
    JButton submitBtn, clearBtn;

    RegistrationForm() {
        setTitle("Student Registration Form");
        setSize(600, 650);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLocationRelativeTo(null);
        setLayout(null);
        getContentPane().setBackground(new Color(240, 248, 255));

        JLabel title = new JLabel("Student Registration Form");
        title.setFont(new Font("Arial", Font.BOLD, 24));
        title.setBounds(140, 20, 350, 40);
        add(title);

        JLabel firstNameLabel = new JLabel("First Name:");
        firstNameLabel.setBounds(80, 90, 120, 25);
        add(firstNameLabel);

        firstNameField = new JTextField();
        firstNameField.setBounds(220, 90, 250, 25);
        add(firstNameField);

        JLabel lastNameLabel = new JLabel("Last Name:");
        lastNameLabel.setBounds(80, 130, 120, 25);
        add(lastNameLabel);

        lastNameField = new JTextField();
        lastNameField.setBounds(220, 130, 250, 25);
        add(lastNameField);

        JLabel genderLabel = new JLabel("Gender:");
        genderLabel.setBounds(80, 170, 120, 25);
        add(genderLabel);

        maleBtn = new JRadioButton("Male");
        femaleBtn = new JRadioButton("Female");

        maleBtn.setBounds(220, 170, 80, 25);
        femaleBtn.setBounds(310, 170, 100, 25);

        maleBtn.setBackground(new Color(240, 248, 255));
        femaleBtn.setBackground(new Color(240, 248, 255));

        ButtonGroup genderGroup = new ButtonGroup();
        genderGroup.add(maleBtn);
        genderGroup.add(femaleBtn);

        add(maleBtn);
        add(femaleBtn);

        JLabel ageLabel = new JLabel("Age:");
        ageLabel.setBounds(80, 210, 120, 25);
        add(ageLabel);

        ageField = new JTextField();
        ageField.setBounds(220, 210, 250, 25);
        add(ageField);

        JLabel emailLabel = new JLabel("Email:");
        emailLabel.setBounds(80, 250, 120, 25);
        add(emailLabel);

        emailField = new JTextField();
        emailField.setBounds(220, 250, 250, 25);
        add(emailField);

        JLabel phoneLabel = new JLabel("Phone:");
        phoneLabel.setBounds(80, 290, 120, 25);
        add(phoneLabel);

        phoneField = new JTextField();
        phoneField.setBounds(220, 290, 250, 25);
        add(phoneField);

        JLabel courseLabel = new JLabel("Course:");
        courseLabel.setBounds(80, 330, 120, 25);
        add(courseLabel);

        String[] courses = {"B.Tech", "BCA", "MCA", "B.Sc", "M.Tech"};
        courseBox = new JComboBox<>(courses);
        courseBox.setBounds(220, 330, 250, 25);
        add(courseBox);

        JLabel branchLabel = new JLabel("Branch:");
        branchLabel.setBounds(80, 370, 120, 25);
        add(branchLabel);

        String[] branches = {"CSE", "IT", "ECE", "AI/ML", "Data Science"};
        branchBox = new JComboBox<>(branches);
        branchBox.setBounds(220, 370, 250, 25);
        add(branchBox);

        JLabel cityLabel = new JLabel("City:");
        cityLabel.setBounds(80, 410, 120, 25);
        add(cityLabel);

        cityField = new JTextField();
        cityField.setBounds(220, 410, 250, 25);
        add(cityField);

        JLabel addressLabel = new JLabel("Address:");
        addressLabel.setBounds(80, 450, 120, 25);
        add(addressLabel);

        addressArea = new JTextArea();
        addressArea.setBounds(220, 450, 250, 70);
        addressArea.setBorder(BorderFactory.createLineBorder(Color.GRAY));
        add(addressArea);

        submitBtn = new JButton("Submit");
        submitBtn.setBounds(160, 550, 120, 35);
        submitBtn.setBackground(new Color(144, 238, 144));
        submitBtn.addActionListener(this);
        add(submitBtn);

        clearBtn = new JButton("Clear");
        clearBtn.setBounds(310, 550, 120, 35);
        clearBtn.setBackground(new Color(255, 182, 193));
        clearBtn.addActionListener(this);
        add(clearBtn);

        setVisible(true);
    }

    public Connection getConnection() {
        Connection con = null;

        try {
            Class.forName("oracle.jdbc.OracleDriver");

            con = DriverManager.getConnection(
                "jdbc:oracle:thin:@localhost:1521:XE",
                "stress_user",
                "Stress123"
            );

        } catch (Exception e) {
            JOptionPane.showMessageDialog(this, "Database Connection Error: " + e.getMessage());
        }

        return con;
    }

    public void actionPerformed(ActionEvent e) {

        if (e.getSource() == submitBtn) {
            String firstName = firstNameField.getText();
            String lastName = lastNameField.getText();

            String gender = "";
            if (maleBtn.isSelected()) {
                gender = "Male";
            } else if (femaleBtn.isSelected()) {
                gender = "Female";
            }

            String age = ageField.getText();
            String email = emailField.getText();
            String phone = phoneField.getText();
            String course = courseBox.getSelectedItem().toString();
            String branch = branchBox.getSelectedItem().toString();
            String city = cityField.getText();
            String address = addressArea.getText();

            try {
                Connection con = getConnection();

                String query = "INSERT INTO registration " +
        "(id, first_name, last_name, gender, age, email, phone, course, branch, city, address) " +
        "VALUES (reg_seq.NEXTVAL, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?)";

               PreparedStatement pst = con.prepareStatement(query);

pst.setString(1, firstName);
pst.setString(2, lastName);
pst.setString(3, gender);
pst.setInt(4, Integer.parseInt(age));
pst.setString(5, email);
pst.setString(6, phone);
pst.setString(7, course);
pst.setString(8, branch);
pst.setString(9, city);
pst.setString(10, address);

pst.executeUpdate();
               
                JOptionPane.showMessageDialog(this, "Registration Successful!");

                con.close();

            } catch (Exception ex) {
                JOptionPane.showMessageDialog(this, "Error: " + ex.getMessage());
            }
        }

        if (e.getSource() == clearBtn) {
            firstNameField.setText("");
            lastNameField.setText("");
            ageField.setText("");
            emailField.setText("");
            phoneField.setText("");
            cityField.setText("");
            addressArea.setText("");
            maleBtn.setSelected(false);
            femaleBtn.setSelected(false);
            courseBox.setSelectedIndex(0);
            branchBox.setSelectedIndex(0);
        }
    }

    public static void main(String[] args) {
        new RegistrationForm();
    }
}
```
<img width="446" height="508" alt="image" src="https://github.com/user-attachments/assets/1e3107a3-7472-4108-832a-1279494e3d97" />

<img width="858" height="180" alt="image" src="https://github.com/user-attachments/assets/e4b28b39-0896-4c74-bf8c-06607a4c099e" />


## assi-13
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class CalculatorGUI extends JFrame implements ActionListener {

    JTextField display;
    String operator = "";
    double num1 = 0, num2 = 0;

    public CalculatorGUI() {

        setTitle("Calculator");
        setSize(300, 400);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new BorderLayout());

        // ===== DISPLAY =====
        display = new JTextField();
        display.setFont(new Font("Arial", Font.BOLD, 20));
        display.setHorizontalAlignment(JTextField.RIGHT);
        add(display, BorderLayout.NORTH);

        // ===== BUTTON PANEL =====
        JPanel panel = new JPanel(new GridLayout(4, 4, 5, 5));

        String buttons[] = {
            "7", "8", "9", "/",
            "4", "5", "6", "*",
            "1", "2", "3", "-",
            "0", "C", "=", "+"
        };

        for (String text : buttons) {
            JButton btn = new JButton(text);
            btn.setFont(new Font("Arial", Font.BOLD, 16));
            btn.addActionListener(this);
            panel.add(btn);
        }

        add(panel, BorderLayout.CENTER);

        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {

        String cmd = e.getActionCommand();

        // Numbers
        if (cmd.matches("[0-9]")) {
            display.setText(display.getText() + cmd);
        }

        // Operators
        else if (cmd.matches("[+\\-*/]")) {
            num1 = Double.parseDouble(display.getText());
            operator = cmd;
            display.setText("");
        }

        // Equals
        else if (cmd.equals("=")) {
            num2 = Double.parseDouble(display.getText());

            double result = 0;

            switch (operator) {
                case "+": result = num1 + num2; break;
                case "-": result = num1 - num2; break;
                case "*": result = num1 * num2; break;
                case "/": result = num1 / num2; break;
            }

            display.setText(String.valueOf(result));
        }

        // Clear
        else if (cmd.equals("C")) {
            display.setText("");
            num1 = num2 = 0;
        }
    }

    public static void main(String[] args) {
        new CalculatorGUI();
    }
}
```
<img width="284" height="392" alt="image" src="https://github.com/user-attachments/assets/67dbfb4f-987a-41f9-95ec-8c7e02727a6e" />


## assi-14
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class MatrixAdditionGUI extends JFrame implements ActionListener {

    JTextField[][] A = new JTextField[2][2];
    JTextField[][] B = new JTextField[2][2];
    JTextField[][] R = new JTextField[2][2];

    JButton addButton;

    public MatrixAdditionGUI() {

        setTitle("Matrix Addition");
        setSize(500, 400);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new BorderLayout(10, 10));

        // ===== TITLE =====
        JLabel title = new JLabel("Matrix Addition", JLabel.CENTER);
        title.setFont(new Font("Arial", Font.BOLD, 18));
        add(title, BorderLayout.NORTH);

        // ===== CENTER PANEL =====
        JPanel center = new JPanel(new GridLayout(1, 3, 20, 20));
        center.setBorder(BorderFactory.createEmptyBorder(20, 20, 20, 20));

        center.add(createMatrixPanel(A, "Matrix A"));
        center.add(createMatrixPanel(B, "Matrix B"));
        center.add(createMatrixPanel(R, "Result"));

        add(center, BorderLayout.CENTER);

        // ===== BUTTON PANEL =====
        JPanel bottom = new JPanel();
        addButton = new JButton("Add");
        addButton.setPreferredSize(new Dimension(100, 40));
        addButton.addActionListener(this);

        bottom.add(addButton);
        add(bottom, BorderLayout.SOUTH);

        setVisible(true);
    }

    // Method to create matrix panel
    JPanel createMatrixPanel(JTextField[][] matrix, String title) {
        JPanel panel = new JPanel(new GridLayout(2, 2, 5, 5));
        panel.setBorder(BorderFactory.createTitledBorder(title));

        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {

                matrix[i][j] = new JTextField();
                matrix[i][j].setHorizontalAlignment(JTextField.CENTER);

                if (title.equals("Result")) {
                    matrix[i][j].setEditable(false);
                    matrix[i][j].setBackground(new Color(230, 230, 230));
                }

                panel.add(matrix[i][j]);
            }
        }
        return panel;
    }

    public void actionPerformed(ActionEvent e) {
        try {
            for (int i = 0; i < 2; i++) {
                for (int j = 0; j < 2; j++) {

                    int a = Integer.parseInt(A[i][j].getText());
                    int b = Integer.parseInt(B[i][j].getText());

                    R[i][j].setText(String.valueOf(a + b));
                }
            }
        } catch (Exception ex) {
            JOptionPane.showMessageDialog(this, "Enter valid numbers!");
        }
    }

    public static void main(String[] args) {
        new MatrixAdditionGUI();
    }
}
```
<img width="484" height="392" alt="image" src="https://github.com/user-attachments/assets/68c1f6dc-364a-4d8d-a517-e3ee51abe03b" />

## assi-15
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class ShapeDrawer extends JFrame implements ActionListener {

    String shape = "";

    public ShapeDrawer() {

        setTitle("Shape Drawer");
        setSize(600, 500);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new BorderLayout());

        // Panel for buttons
        JPanel panel = new JPanel(new GridLayout(2, 5));

        String buttons[] = {
            "Circle", "Oval", "Rectangle", "Square", "Line",
            "Arc", "RoundRect", "3D Rect", "Fill Oval", "Fill Rect"
        };

        for (String name : buttons) {
            JButton btn = new JButton(name);
            btn.addActionListener(this);
            panel.add(btn);
        }

        add(panel, BorderLayout.NORTH);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        shape = e.getActionCommand();
        repaint(); // redraw when button clicked
    }

    public void paint(Graphics g) {
        super.paint(g);

        g.setColor(Color.BLUE);

        switch (shape) {
            case "Circle":
                g.drawOval(200, 150, 100, 100);
                break;

            case "Oval":
                g.drawOval(200, 150, 150, 100);
                break;

            case "Rectangle":
                g.drawRect(200, 150, 150, 100);
                break;

            case "Square":
                g.drawRect(200, 150, 100, 100);
                break;

            case "Line":
                g.drawLine(200, 150, 350, 250);
                break;

            case "Arc":
                g.drawArc(200, 150, 150, 100, 0, 180);
                break;

            case "RoundRect":
                g.drawRoundRect(200, 150, 150, 100, 30, 30);
                break;

            case "3D Rect":
                g.draw3DRect(200, 150, 150, 100, true);
                break;

            case "Fill Oval":
                g.fillOval(200, 150, 150, 100);
                break;

            case "Fill Rect":
                g.fillRect(200, 150, 150, 100);
                break;
        }
    }

    public static void main(String[] args) {
        new ShapeDrawer();
    }
}
```
<img width="568" height="469" alt="image" src="https://github.com/user-attachments/assets/fca9f628-35f0-4cc4-844e-a1757ac4864e" />

## assi-16
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class PaintBrush extends JFrame implements MouseListener, MouseMotionListener {

    int x1, y1, x2, y2;
    Color currentColor = Color.BLACK;
    int brushSize = 3;

    public PaintBrush() {

        setTitle("Simple Paint Brush");
        setSize(600, 500);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        addMouseListener(this);
        addMouseMotionListener(this);

        // Top Panel (Controls)
        JPanel panel = new JPanel();

        // Color Buttons
        JButton red = new JButton("Red");
        JButton blue = new JButton("Blue");
        JButton green = new JButton("Green");

        // Width Selector
        String sizes[] = {"2", "5", "10"};
        JComboBox<String> widthBox = new JComboBox<>(sizes);

        panel.add(red);
        panel.add(blue);
        panel.add(green);
        panel.add(new JLabel("Brush Size:"));
        panel.add(widthBox);

        add(panel, BorderLayout.NORTH);

        // Button Actions
        red.addActionListener(e -> currentColor = Color.RED);
        blue.addActionListener(e -> currentColor = Color.BLUE);
        green.addActionListener(e -> currentColor = Color.GREEN);

        widthBox.addActionListener(e -> {
            brushSize = Integer.parseInt((String) widthBox.getSelectedItem());
        });

        setVisible(true);
    }

    // Drawing
    public void mouseDragged(MouseEvent e) {
        x2 = e.getX();
        y2 = e.getY();

        Graphics g = getGraphics();
        g.setColor(currentColor);
        ((Graphics2D) g).setStroke(new BasicStroke(brushSize));
        g.drawLine(x1, y1, x2, y2);

        x1 = x2;
        y1 = y2;
    }

    public void mousePressed(MouseEvent e) {
        x1 = e.getX();
        y1 = e.getY();
    }

    // Unused methods (must implement)
    public void mouseReleased(MouseEvent e) {}
    public void mouseClicked(MouseEvent e) {}
    public void mouseEntered(MouseEvent e) {}
    public void mouseExited(MouseEvent e) {}
    public void mouseMoved(MouseEvent e) {}

    public static void main(String[] args) {
        new PaintBrush();
    }
}
```
<img width="567" height="469" alt="image" src="https://github.com/user-attachments/assets/7c48d58e-103a-46a7-841c-662990250642" />

## assi-17
```
//File: Employee.java
package company;
public class Employee {
    public void showEmployee() {
        System.out.println("This is Employee class in package company");
    }
}

//File: Salary.java
package company.payroll;

public class Salary {
    public void showSalary() {
        System.out.println("This is Salary class in sub-package company.payroll");
    }
}

//File: TestCompany.java
import company.Employee;
import company.payroll.Salary;

public class TestCompany {

    public static void main(String[] args) {

        Employee e = new Employee();
        e.showEmployee();

        Salary s = new Salary();
        s.showSalary();
    }
}
```
<img width="898" height="139" alt="image" src="https://github.com/user-attachments/assets/ea79a7e4-5f25-4d22-a88d-9d38c9a9f9f7" />


## assi-18
```
// File: Student.java
package mypack;

public class Student1 {

    public void showStudent() {
        System.out.println("This is Student class inside mypack package");
    }
}

// File: Result.java
package mypack.details;

public class Result {

    public void showResult() {
        System.out.println("This is Result class inside sub-package mypack.details");
    }
}

// File: TestPackage.java

import mypack.Student1;
import mypack.details.Result;

public class TestPackage {

    public static void main(String[] args) {

        Student1 s = new Student1();
        s.showStudent();

        Result r = new Result();
        r.showResult();
    }
}
```
<img width="879" height="151" alt="image" src="https://github.com/user-attachments/assets/5a7e0320-76fe-487e-a5fe-e3381c65650e" />

## assi-19
```
public class ExceptionDemo {

    public static void main(String[] args) {

        // -------- ARRAY OUT OF BOUNDS --------
        try {
            int arr[] = {10, 20, 30, 40, 50};

            System.out.println("Valid access: " + arr[2]);

            // Invalid access
            System.out.println("Invalid access: " + arr[8]);

        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Exception: Array index is out of bounds! Please access valid index.");
        }


        // -------- ARITHMETIC EXCEPTION --------
        try {
            int a = 10;
            int b = 0;

            int result = a / b;

            System.out.println("Result: " + result);

        } catch (ArithmeticException e) {
            System.out.println("Exception: Division by zero is not allowed!");
        }

        System.out.println("Program executed successfully.");
    }
}
```
<img width="816" height="173" alt="image" src="https://github.com/user-attachments/assets/09668dce-c9c5-4bdc-b787-854dabcc30f5" />

## assi-20
```
import java.util.Scanner;

// User Defined Exception
class InvalidAgeException extends Exception {
    InvalidAgeException(String message) {
        super(message);
    }
}

// Student Class (Main Class)
public class Student {

    int age;

    // Method to check age
    void checkAge() throws InvalidAgeException {
        if (age < 18) {
            throw new InvalidAgeException("Age is too low. Not eligible.");
        } 
        else if (age > 60) {
            throw new InvalidAgeException("Age is too high. Not eligible.");
        } 
        else {
            System.out.println("Valid Age. Student is eligible.");
        }
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        Student s = new Student();

        System.out.print("Enter age: ");
        s.age = sc.nextInt();

        try {
            s.checkAge();
        } catch (InvalidAgeException e) {
            System.out.println("Exception: " + e.getMessage());
        }

        sc.close();
    }
}
```

<img width="666" height="146" alt="image" src="https://github.com/user-attachments/assets/ea86a252-2c1c-45ba-aaaf-34a4195cd1b9" />

## assi-21
```
import java.io.*;
public class FileHandlingDemo {
    public static void main(String[] args) {
        try {

            // ================= BYTE STREAM COPY =================
            FileInputStream fis1 = new FileInputStream("source.txt");
            FileOutputStream fos1 = new FileOutputStream("dest_byte.txt");

            int b;
            while ((b = fis1.read()) != -1) {
                fos1.write(b);
            }

            fis1.close();
            fos1.close();
            System.out.println("BYTE STREAM COPY DONE");


            // ================= CHARACTER STREAM COPY =================
            FileReader fr1 = new FileReader("source.txt");
            FileWriter fw1 = new FileWriter("dest_char.txt");

            int ch;
            while ((ch = fr1.read()) != -1) {
                fw1.write(ch);
            }

            fr1.close();
            fw1.close();
            System.out.println("CHARACTER STREAM COPY DONE");


            // ================= WRITE & READ USING BYTE STREAM =================
            FileOutputStream fos2 = new FileOutputStream("bytefile.txt");
            fos2.write("Hello".getBytes());
            fos2.close();

            FileInputStream fis2 = new FileInputStream("bytefile.txt");
            while ((b = fis2.read()) != -1) {
                System.out.print((char) b);
            }
            fis2.close();
            System.out.println();


            // ================= WRITE & READ USING CHARACTER STREAM =================
            FileWriter fw2 = new FileWriter("charfile.txt");
            fw2.write("Hello Java");
            fw2.close();

            FileReader fr2 = new FileReader("charfile.txt");
            while ((ch = fr2.read()) != -1) {
                System.out.print((char) ch);
            }
            fr2.close();

        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
<img width="847" height="195" alt="image" src="https://github.com/user-attachments/assets/103de49e-c608-428a-9483-6ab1dfb1c71b" />


## assi-22
``` // Interface
interface Vehicle {
    void start();
    void stop();
}

// Abstract Class
abstract class Machine {
    abstract void fuelType();

    void display() {
        System.out.println("This is a machine");
    }
}

// Parent Class (Inheritance)
class Car extends Machine implements Vehicle {

    // Implementing interface methods
    public void start() {
        System.out.println("Car starts with key");
    }

    public void stop() {
        System.out.println("Car stops using brake");
    }

    // Implementing abstract method
    void fuelType() {
        System.out.println("Fuel Type: Petrol/Diesel");
    }
}

// Main Class
public class Main {
    public static void main(String[] args) {

        Car c = new Car();

        c.display();      // from abstract class (concrete method)
        c.fuelType();     // abstract method
        c.start();        // interface method
        c.stop();         // interface method
    }
}
```

<img width="526" height="169" alt="image" src="https://github.com/user-attachments/assets/0a217470-bfbc-466e-a127-05d6a801fda9" />


## Javalab

