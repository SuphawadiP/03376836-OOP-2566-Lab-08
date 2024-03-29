# Lab 8 Exercise 7

## Overriding base class member

1. สร้าง console application project

```cmd
dotnet new console --name Lab08_Ex07
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
DerivedClass dc = new DerivedClass();
System.Console.WriteLine(dc.Hello);

class BaseClass
{
    public string Hello = "Hello From BaseClass";
}
class DerivedClass : BaseClass
{
    public string Hello = "Hello From DerivedClass";
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab08_Ex07
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
<img width="797" alt="Screenshot 2024-03-29 120341" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/433e3f68-60f0-43eb-92b2-7779554c0884">

#### สามารถ Build ได้ แต่การซ่อนสมาชิกที่ถูกสืบทอดมาจากคลาสหลัก (base class) ด้วยสมาชิกที่มีชื่อเดียวกันในคลาสที่สืบทอด (derived class) โดยไม่ได้ใช้คำสำคัญ new เพื่อระบุว่าการซ่อนนี้เป็นเจตนา
5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab08_Ex07
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
<img width="797" alt="Screenshot 2024-03-29 120416" src="https://github.com/SuphawadiP/03376836-OOP-2566-Lab-08/assets/144196049/815c2c2a-cc7d-46a1-a536-a1b2ce4aa724">

#### สามารถ Run ได้ เพราะ ไม่มีข้อผิดพลาดมีแค่เตือน
7.อธิบายสิ่งที่พบในการทดลอง
#### โปรแกรมจะแสดงผล Hello From DerivedClass
