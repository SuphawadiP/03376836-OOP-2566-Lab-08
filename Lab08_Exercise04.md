# Lab 8 Exercise 4

## Class inheritance 2

![alt text](./Pictures/image01.png)

1. สร้าง console application project

```cmd
dotnet new console --name Lab08_Ex04
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
class BaseClass2
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
dotnet build  Lab08_Ex04
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
<img width="796" alt="Screenshot 2024-03-29 115050" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/6e4e78d5-c2af-40ec-baca-7c39d1d4b44d">

#### โปรแกรมสามารถ Build ได้ เพราะ สืบทอดจาก class DerivedClass : BaseClass2
5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab08_Ex04
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
<img width="797" alt="Screenshot 2024-03-29 115133" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/4bf00c40-75fb-4f23-b4fa-4c75e0723e06">

#### โปรแกรมสามารถ Run ได้ เพราะ สืบทอดได้ถูกต้อง
7.อธิบายสิ่งที่พบในการทดลอง
#### โปแกรมจะแสดงผล
#### This is BaseClass2
#### This is DerivedClass
