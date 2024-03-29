# Lab 8 Exercise 10

## Using a references to a base class

1. สร้าง console application project

```cmd
dotnet new console --name Lab08_Ex10
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
DerivedClass DC = new DerivedClass();
System.Console.WriteLine($"DC.Field1 = {DC.Field1}");
BaseClass BC = (BaseClass)DC;
System.Console.WriteLine($"BC.Field1 = {BC.Field1}");

class BaseClass
{
    public string Field1 = "Field1 of BaseClass"; 
}
class DerivedClass:BaseClass
{
    new public string Field1 = "Field1 of DerivedClass"; 
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab08_Ex10
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
<img width="796" alt="Screenshot 2024-03-29 121420" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/70bb695f-ddfe-445b-9db6-92c58853dcf8">

#### สามารถ build ได้ เพราะการใช้ reference ของ base class ในที่นี้ช่วยให้เราสามารถอ้างถึงอ็อบเจกต์ของ derived class ได้ และพึ่งพาการแปลงชนิดเพื่อให้ reference ของ base class เรียกใช้เมธอดหรือเข้าถึงสมาชิกของ derived class ได้โดยตรง
5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab08_Ex10
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
<img width="799" alt="Screenshot 2024-03-29 121441" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/0fe261cb-7f0d-49c4-8b2f-dbb1b8e4ec3b">

#### สามารถ Run ได้ ปกติ
7.อธิบายสิ่งที่พบในการทดลอง
#### โปรแกรมจะแสดงผล
#### DC.Field1 = Field1 of DerivedClass
#### BC.Field1 = Field1 of BaseClass
