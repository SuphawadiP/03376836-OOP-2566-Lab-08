# Lab 8 Exercise 2

## Class Inheritance การใช้งาน method และ field ของ base และ  derived class

1. สร้าง console application project

```cmd
dotnet new console --name Lab08_Ex02
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
var dc = new DerivedClass();
dc.Method1(dc.Field1);  // call with method and field of base class
dc.Method2(dc.Field1);  // call with method of derived class and field of base class
dc.Method1(dc.Field2);  // call with method of base class and field of derived class
dc.Method2(dc.Field2);  // call with method and field of derived class

class BaseClass
{
    public string Field1 = "Field 1 in BaseClass";
    public void Method1(string value)
    {
        System.Console.WriteLine($"Method1() in BaseClass, string input = {value} ");
    }
}
class DerivedClass: BaseClass
{
    public string Field2 = "Field 2 in DerivedClass";
    public void Method2(string value)
    {
        System.Console.WriteLine($"Method2() in DerivedClass, string input = {value} ");
    }

}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab08_Ex02
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
<img width="792" alt="Screenshot 2024-03-29 114052" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/382009f7-63dc-4b0a-b9e2-22f044623c35">

#### สามารถ Build ได้ เพราะ เป็นการใช้ method และ field ของ base และ deroved class
5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab08_Ex02
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
<img width="790" alt="Screenshot 2024-03-29 114151" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/c5de8279-4e86-400c-a8aa-74aa18b2c3bd">

#### สามารถ Run ได้ เพราะ เป็นการเรียกใช้ method ต่างๆมาแสดงผล จาก class base Class และ DerivedClass สืบทอดจาก base Class
7.อธิบายสิ่งที่พบในการทดลอง
#### โปรแกรมจะแสดงผล
#### Method1() in BaseClass, string input = Field 1 in BaseClass
#### Method2() in DerivedClass, string input = Field 1 in BaseClass
#### Method1() in BaseClass, string input = Field 2 in DerivedClass
#### Method2() in DerivedClass, string input = Field 2 in DerivedClass
