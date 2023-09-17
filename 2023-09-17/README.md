## 객체 전달

Java에서 객체 전달은 다른 메서드 또는 클래스로 객체를 전달하는 프로세스를 나타낸다. 
Java는 객체 지향 프로그래밍 언어로, 객체는 데이터와 해당 데이터를 처리하는 메서드를 포함하는 개체. 이러한 객체를 다른 메서드 또는 클래스로 전달하여 코드를 구성하고 데이터를 처리하는 데 사용된다.

객체 전달 방법

1. 메서드 매개변수로 객체 전달: 메서드를 호출할 때 객체를 메서드의 매개변수로 전달할 수 있다. 이렇게 하면 메서드 내에서 객체의 상태를 변경하거나 해당 객체의 메서드를 호출한다.

```java
public class Person {
    private String name;

    public Person(String name) {
        this.name = name;
    }

    public void sayHello() {
        System.out.println("Hello, my name is " + name);
    }
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person("Alice");
        greetPerson(person);
    }

    public static void greetPerson(Person person) {
        person.sayHello();
    }
}
```

2. 객체 반환: 메서드는 새로운 객체를 생성하거나 이미 존재하는 객체를 반환할 수 있다. 이렇게 반환된 객체는 호출자에게 전달된다.

```java
public class Calculator {
    public int add(int a, int b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator calculator = new Calculator();
        int result = calculator.add(5, 3);
        System.out.println("The result is: " + result);
    }
}
```

3. 객체 참조 전달: Java에서 객체는 참조로 전달된다. 이는 객체의 주소가 메서드로 전달되므로 원래 객체를 수정할 수 있다.

```java
public class Person {
    private String name;

    public Person(String name) {
        this.name = name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person("Alice");
        changeName(person);
        System.out.println("New name: " + person.getName());
    }

    public static void changeName(Person person) {
        person.setName("Bob");
    }
}
```

Java에서 객체를 전달하는 방법은 객체 지향 프로그래밍의 핵심 원칙 중 하나인 캡슐화와 관련이 있다. 객체를 적절하게 전달하고 사용함으로써 코드의 모듈성과 재사용성을 향상시킬 수 있다.
