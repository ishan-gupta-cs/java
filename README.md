# Association, Aggregation and Composition in Java

These three concepts describe relationships between classes and objects in Object-Oriented Programming (OOP).

All three represent some form of relationship between objects, but the strength of relationship differs.

---

# 1. Association

## Definition

Association means:

> One object uses or connects with another object.

It is the most general relationship in OOP.

---

## Real-Life Examples

- Teacher teaches Student
- Driver drives Car
- Customer uses Bank

Both objects can exist independently.

---

## Java Example

```java
class Student
{
    String name;

    Student(String name)
    {
        this.name = name;
    }
}

class Teacher
{
    String teacherName;

    Teacher(String teacherName)
    {
        this.teacherName = teacherName;
    }

    void teach(Student s)
    {
        System.out.println(teacherName + " teaches " + s.name);
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Student s1 = new Student("Rahul");

        Teacher t1 = new Teacher("Ankit");

        t1.teach(s1);
    }
}
