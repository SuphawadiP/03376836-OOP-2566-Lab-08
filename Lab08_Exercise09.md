# Lab 8 Exercise 9

## Access base member by `base` keyword

1. สร้าง console application project

```cmd
dotnet new console --name Lab08_Ex09
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
DerivedClass dc = new DerivedClass();
dc.PrintBaseHello();

class BaseClass
{
    public string Hello = "Hello From BaseClass";
}
class DerivedClass : BaseClass
{
    new public string Hello = "Hello From DerivedClass";

    public void PrintBaseHello()
    {
        string BaseHello = base.Hello;
        System.Console.WriteLine(BaseHello);
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab08_Ex09
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
<img width="797" alt="Screenshot 2024-03-29 121041" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/021004b7-dd11-4f49-9235-cfaf063ba363">

#### สามารถ Build ได้ พราะ ได้ใช้ base keyword จาก class ที่กำหนดมา คือ PrintBaseHello()
5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab08_Ex09
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
<img width="798" alt="Screenshot 2024-03-29 121114" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/7ad2c559-1f3b-403d-b75a-d77324334121">

#### สามารถ Run ได้ เพราะ เป็นการเรียกใช้ base keyword กำหนด base.Hello มาแสดงผล
7.อธิบายสิ่งที่พบในการทดลอง
#### โปรแกรมจะแสดงผล Hello From BaseClass
