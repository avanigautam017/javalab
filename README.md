## INDEX

[Program-1 wap to print hello world](#assi-1)

[Program-2 wap to perform function call.](#assi-2)

## assi-1
```package com.mycompany.avanigautam;
public class Avanigautam {

    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```
<img width="815" height="417" alt="image" src="https://github.com/user-attachments/assets/07d22cdf-bfef-4dee-a1d1-d8d64c34f315" />



## assi-2
```class NewMain {
    public static void main(String[] args) {
          
    }
    
}
public class TestA{
    void funA(){
            System.out.println("We are in class A");
    }
    public static void main(String[] args){
        TestC obj=new TestC();
        obj.funA();
        obj.funB();
        obj.funC();
        
    }
    
}
class TestB extends TestA {
    void funB(){
        System.out.println("We are in class B");
    }
}
class TestC extends TestB{
    void funC(){
        System.out.println("We are in class C");
    }
    
}
```
<img width="528" height="322" alt="image" src="https://github.com/user-attachments/assets/82d3025f-0310-4845-8d1b-a2c54f981b9d" />

