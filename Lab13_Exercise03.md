# Lab 13 Exercise 3

## Call from abstract class references

1.สร้าง console application project

```cmd
dotnet new console --name Lab13_Ex03
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
Animal [] animals = new Animal[3];
animals[0] = new Dog();
animals[1] = new Bird();
animals[2] = new Fish();

foreach (var animal in animals)
{
    animal.Move();
}

interface IMovable
{
    public void Move();
}

abstract class Animal : IMovable
{
    abstract public void Move();
}
class Dog : Animal
{
    public override void Move()
    {
        System.Console.WriteLine("Dog move by running on the ground");
    }
}
class Fish : Animal
{
    public override void Move()
    {
        System.Console.WriteLine("Fish move by swimming in the water");
    }
}
class Bird : Animal
{
    public override void Move()
    {
        System.Console.WriteLine("Bird move by flying in the air");
    }
}

```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab13_Ex03
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![image](https://github.com/ThanchiraCharakhon099/03376836-OOP-2566-Lab-13/assets/144195708/fd9fa860-c9ec-4344-8459-9f5f2ba79a3d)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab13_Ex03
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/ThanchiraCharakhon099/03376836-OOP-2566-Lab-13/assets/144195708/44180d08-4abc-44c3-9242-16a3b4b2f1d5)

7.อธิบายสิ่งที่พบในการทดลอง

        แสดงผล

Dog move by running on the ground

Bird move by flying in the air

Fish move by swimming in the water
