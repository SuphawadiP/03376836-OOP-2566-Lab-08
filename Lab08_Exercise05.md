# Lab 8 Exercise 5

## Multiple base class inheritance

![alt text](./Pictures/image01.png)

1. สร้าง console application project

```cmd
dotnet new console --name Lab08_Ex05
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

class DerivedClass : BaseClass1, BaseClass2
{
    public DerivedClass()
    {
        System.Console.WriteLine("This is DerivedClass");
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab08_Ex05
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
#### แก้ไขแล้ว
<img width="797" alt="Screenshot 2024-03-29 115556" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/3ab9a915-5f0d-4ffe-bb9b-86554668a64b">

#### ไม่สามารถ Build ได้เพราะ C# ไม่สามารถทำ multiple base class ได้ แก้จากให้เลือก Class อย่างใดอย่างหนึ่ง
5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab08_Ex05
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
#### แก้ไขแล้ว
<img width="797" alt="Screenshot 2024-03-29 115640" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/4aff50b0-1f12-469f-afa8-8f1f66c6a584">

#### ไม่สามารถ Run ได้เพราะ C# ไม่สามารถทำ multiple base class ได้ แก้จากให้เลือก Class อย่างใดอย่างหนึ่ง
7.อธิบายสิ่งที่พบในการทดลอง
#### โปรแกรมจะแสดงผล
#### This is BaseClass1
#### This is DerivedClass
