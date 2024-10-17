- 👋 Hi, I’m @onionsgun
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...none
- 
Solutions for "ვარიანტი 1" (file 1)
Task 1: Data Types and Control Structures

csharp

using System;

class Program
{
    static void Main()
    {
        int age = 25; // replace with your age
        string name = "John"; // replace with your name

        for (int i = 1; i <= 10; i++)
        {
            Console.WriteLine($"{name} - Iteration: {i}");
        }
    }
}

Task 2: Classes and Methods

csharp

using System;

class Person
{
    private int age;
    public string Name { get; set; }

    public Person(int age, string name)
    {
        this.age = age;
        this.Name = name;
    }

    public string Introduction()
    {
        return $"Hi I'm {Name} and I'm {age} years old";
    }
}

class Program
{
    static void Main()
    {
        Person person = new Person(25, "John");
        Console.WriteLine(person.Introduction());
    }
}

Task 3: Inheritance and Method Overloading

csharp

using System;

class Shape
{
    protected double Area { get; set; }

    public Shape()
    {
        Area = 0;
    }
}

class Rectangle : Shape
{
    private double _length;
    private double _width;

    public double Length
    {
        get { return _length; }
        set { _length = value; }
    }

    public double Width
    {
        get { return _width; }
        set { _width = value; }
    }

    public void CalculateArea(double length, double width)
    {
        Area = length * width;
    }

    public double GetArea()
    {
        return Area;
    }
}

class Circle : Shape
{
    private double _radius;

    public double Radius
    {
        get { return _radius; }
        set { _radius = value; }
    }

    public void CalculateArea(double radius)
    {
        Area = Math.PI * radius * radius;
    }

    public double GetArea()
    {
        return Area;
    }
}

class Program
{
    static void Main()
    {
        Rectangle rectangle = new Rectangle();
        rectangle.CalculateArea(10, 5);
        Console.WriteLine($"Rectangle Area: {rectangle.GetArea()}");

        Circle circle = new Circle();
        circle.CalculateArea(7);
        Console.WriteLine($"Circle Area: {circle.GetArea()}");
    }
}

Task 4: Abstract Classes and Interfaces

csharp

using System;

abstract class Vehicle
{
    public abstract void StartEngine();
}

class Car : Vehicle
{
    public override void StartEngine()
    {
        Console.WriteLine("Car engine started");
    }
}

class Bicycle : Vehicle
{
    public override void StartEngine()
    {
        Console.WriteLine("Pedaling the bicycle");
    }
}

class Program
{
    static void Main()
    {
        Vehicle car = new Car();
        car.StartEngine();

        Vehicle bicycle = new Bicycle();
        bicycle.StartEngine();
    }
}

Task 5: Generics

csharp

using System;
using System.Collections.Generic;

class MyList<T>
{
    private List<T> items = new List<T>();

    public void Add(T item)
    {
        items.Add(item);
    }

    public T Get(int index)
    {
        return items[index];
    }
}

class Program
{
    static void Main()
    {
        MyList<int> list = new MyList<int>();
        list.Add(10);
        list.Add(20);
        list.Add(30);

        Console.WriteLine(list.Get(1)); // Output: 20
    }
}

Solutions for "ვარიანტი 2" (file 2)
Task 1: Data Types and Control Structures

csharp

using System;

class Program
{
    static void Main()
    {
        int quantity = 7;
        string itemName = "Widget";

        for (int i = 1; i <= 5; i++)
        {
            Console.WriteLine($"{itemName} - Iteration: {i}");
        }
    }
}

Task 2: Classes and Methods

csharp

using System;

class Employee
{
    private string _employeeName;
    public string Salary { get; set; }

    public Employee(string name, string salary)
    {
        _employeeName = name;
        Salary = salary;
    }

    public string DisplayInfo()
    {
        return $"Hi I'm {_employeeName} and I earn {Salary} per year";
    }
}

class Program
{
    static void Main()
    {
        Employee employee = new Employee("Alice", "$50,000");
        Console.WriteLine(employee.DisplayInfo());
    }
}

Task 3: Inheritance and Method Overloading

csharp

using System;

class Item
{
    protected double Price { get; set; }

    public Item()
    {
        Price = 0;
    }
}

class Fruit : Item
{
    private double _weightInKg;
    private double _priceOfOneKg;

    public double WeightInKg
    {
        get { return _weightInKg; }
        set { _weightInKg = value; }
    }

    public double PriceOfOneKg
    {
        get { return _priceOfOneKg; }
        set { _priceOfOneKg = value; }
    }

    public void CalculateTotalPrice(double weight, double pricePerKg)
    {
        Price = weight * pricePerKg;
    }

    public double GetTotalPrice()
    {
        return Price;
    }
}

class Electronics : Item
{
    private int _quantity;
    private double _oneUnitPrice;

    public void CalculateTotalPrice(int quantity, double pricePerUnit)
    {
        Price = quantity * pricePerUnit;
    }

    public double GetTotalPrice()
    {
        return Price;
    }
}

class Program
{
    static void Main()
    {
        Fruit fruit = new Fruit();
        fruit.CalculateTotalPrice(2, 3);
        Console.WriteLine($"Fruit Total Price: {fruit.GetTotalPrice()}");

        Electronics electronics = new Electronics();
        electronics.CalculateTotalPrice(5, 200);
        Console.WriteLine($"Electronics Total Price: {electronics.GetTotalPrice()}");
    }
}

Task 4: Abstract Classes and Interfaces

csharp

using System;

abstract class Bird
{
    public abstract void MakeSound();
}

class Sparrow : Bird
{
    public override void MakeSound()
    {
        Console.WriteLine("Chirp");
    }
}

class Pigeon : Bird
{
    public override void MakeSound()
    {
        Console.WriteLine("Coo");
    }
}

class Program
{
    static void Main()
    {
        Bird sparrow = new Sparrow();
        sparrow.MakeSound();

        Bird pigeon = new Pigeon();
        pigeon.MakeSound();
    }
}

Task 5: Generics

csharp

using System;
using System.Collections.Generic;

class MyCollection<T>
{
    private List<T> items = new List<T>();

    public void AddItem(T item)
    {
        items.Add(item);
    }

    public T GetItem(int index)
    {
        return items[index];
    }
}

class Program
{
    static void Main()
    {
        MyCollection<string> collection = new MyCollection<string>();
        collection.AddItem("Apple");
        collection.AddItem("Banana");

        Console.WriteLine(collection.GetItem(1)); // Output: Banana
    }
}

Solutions for "ვარიანტი 3" (file 3)
Task 1: Data Types and Control Structures

csharp

using System;

class Program
{
    static void Main()
    {
        int temperature = 22;
        string city = "Tbilisi";

        for (int i = 1; i <= 7; i++)
        {
            double fahrenheit = (temperature * 9 / 5) + 32;
            Console.WriteLine($"{city} - Day {i}: {fahrenheit}F");
        }
    }
}

Task 2: Classes and Methods

csharp

using System;

class Student
{
    private string _studentName;
    public string Grade { get; set; }

    public Student(string name, string grade)
    {
        _studentName = name;
        Grade = grade;
    }

    public string Greeting()
    {
        return $"Hi I'm {_studentName} and I'm in grade {Grade}";
    }
}

class Program
{
    static void Main()
    {
        Student student = new Student("John", "A");
        Console.WriteLine(student.Greeting());
    }
}

Task 3: Inheritance and Method Overloading

csharp

using System;

class Figure
{
    protected double Area { get; set; }

    public Figure()
    {
        Area = 0;
    }
}

class Triangle : Figure
{
    private double _base;
    private double _height;

    public double Base
    {
        get { return _base; }
        set { _base = value; }
    }

    public double Height
    {
        get { return _height; }
        set { _height = value; }
    }

    public void CalculateArea(double baseLength, double height)
    {
        Area = (baseLength * height) / 2;
    }

    public double GetArea()
    {
        return Area;
    }
}

class Square : Figure
{
    private double _sideLength;

    public double SideLength
    {
        get { return _sideLength; }
        set { _sideLength = value; }
    }

    public void CalculateArea(double sideLength)
    {
        Area = sideLength * sideLength;
    }

    public double GetArea()
    {
        return Area;
    }
}

class Program
{
    static void Main()
    {
        Triangle triangle = new Triangle();
        triangle.CalculateArea(5, 10);
        Console.WriteLine($"Triangle Area: {triangle.GetArea()}");

        Square square = new Square();
        square.CalculateArea(4);
        Console.WriteLine($"Square Area: {square.GetArea()}");
    }
}

Task 4: Abstract Classes and Interfaces

csharp

using System;

abstract class Animal
{
    public abstract void MakeSound();
}

class Dog : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("Woof");
    }
}

class Cat : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("Meow");
    }
}

class Program
{
    static void Main()
    {
        Animal dog = new Dog();
        dog.MakeSound();

        Animal cat = new Cat();
        cat.MakeSound();
    }
}

Task 5: Generics

csharp

using System;
using System.Collections.Generic;

class MyCollection<T>
{
    private List<T> items = new List<T>();

    public void AddItem(T item)
    {
        items.Add(item);
    }

    public T GetItem(int index)
    {
        return items[index];
    }
}

class Program
{
    static void Main()
    {
        MyCollection<string> collection = new MyCollection<string>();
        collection.AddItem("Dog");
        collection.AddItem("Cat");

        Console.WriteLine(collection.GetItem(0)); // Output: Dog
    }
}

Each solution provides the necessary code to meet the requirements of the given task. Let me know if you need any adjustments or further explanations!

<!---
onionsgun/onionsgun is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

