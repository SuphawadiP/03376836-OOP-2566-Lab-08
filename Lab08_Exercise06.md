# Lab 8 Exercise 6

## Multiple base class inheritance

![alt text](./Pictures/image02.png)

1. สร้าง console application project

```cmd
dotnet new console --name Lab08_Ex06
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
DerivedClass dc = new DerivedClass();
class BaseClass1
 {
    public BaseClass1()
    {
        System.Console.WriteLine("This is BaseClass1");
    }
 }
class BaseClass2: BaseClass1
 {
    public BaseClass2()
    {
        System.Console.WriteLine("This is BaseClass2");
    }
 }

class DerivedClass : BaseClass2
{
    public DerivedClass()
    {
        System.Console.WriteLine("This is DerivedClass");
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab08_Ex06
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
<img width="797" alt="Screenshot 2024-03-29 120002" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/44378ea6-9e33-4d2b-88ed-dfe89500d4cd">

#### สามารถ Build ได้ เพราะ BaseClass2:BaseClass1 และ DerivedClass : BaseClass2 สืบทอดกันมา
5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab08_Ex06
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
<img width="800" alt="Screenshot 2024-03-29 120039" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/20ac595f-7b6c-4eba-8448-95053f37389f">

#### สามารถ Run ได้ เพราะสืบทอด Class อย่างถูกต้อง
7.อธิบายสิ่งที่พบในการทดลอง
#### โปรแกรมจะแสดงผล
#### This is BaseClass1
#### This is BaseClass2
#### This is DerivedClass
