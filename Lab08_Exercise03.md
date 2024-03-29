# Lab 8 Exercise 3

## Class inheritance 1

![alt text](./Pictures/image01.png)

1. สร้าง console application project

```cmd
dotnet new console --name Lab08_Ex03
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

class DerivedClass : BaseClass1
{
    public DerivedClass()
    {
        System.Console.WriteLine("This is DerivedClass");
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab08_Ex03
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
<img width="797" alt="Screenshot 2024-03-29 114641" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/e9d7fbed-98ef-4eb2-93ec-55dab9207507">

#### สามารถ Build ได้ เพราะ เป็นการสืบทอด Class จาก DerivedClass : BaseClass1
5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab08_Ex03
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
<img width="795" alt="Screenshot 2024-03-29 114748" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/3cc9c99f-0d0b-4550-a2f1-426200e4f974">

#### สามารถ Run ได้ เพราะ เป็นการสืบทดอ Class อย่างถูกต้อง
7.อธิบายสิ่งที่พบในการทดลอง
#### โปรแกรมจะแสดงผล
#### This is BaseClass1
#### This is DerivedClass
