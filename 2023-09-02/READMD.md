## 상속, 접근지정자

1. **public:**
   - `public` 접근 제어자는 가장 넓은 범위의 접근 권한을 가짐
   - `public`으로 선언된 멤버는 어디서든 접근할 수 있습니다. 다른 클래스에서도 접근이 가능
   - 예를 들어, `public`으로 선언된 메서드는 다른 클래스에서 호출

2. **private:**
   - `private` 접근 제어자는 가장 제한적인 범위의 접근 권한을 가짐
   - `private`으로 선언된 멤버는 동일한 클래스 내에서만 접근할 수 있으며, 외부에서는 직접 접근할 수 없음
   - 보통 클래스의 내부 상태를 캡슐화하고 숨기기 위해 사용

3. **protected:**
   - `protected` 접근 제어자는 같은 패키지 내의 클래스와 해당 클래스를 상속하는 하위 클래스에서 접근
   - 하지만 다른 패키지의 클래스에서는 `protected` 멤버에 접근할 수 없음
   - `protected`는 클래스의 상속과 관련이 있으며, 하위 클래스에서 상위 클래스의 멤버를 사용하고 확장할 때 사용

예시:
```java
public class MyClass {
    public int publicField;     // 다른 클래스에서 접근 가능
    private int privateField;   // 같은 클래스 내에서만 접근 가능
    protected int protectedField; // 같은 패키지 내 및 하위 클래스에서 접근 가능
}
```

**객체 생성**

````
class Ref {
    int a;

    // 생성자: 객체를 초기화하는 메서드
    Ref(int x) {
        a = x;
    }

    // sum 메서드: Ref 클래스의 객체를 받아와서 연산을 수행하는 메서드
    int sum(Ref obj) {
        int k;
        k = obj.a - a;  // obj 객체의 a와 현재 객체(this)의 a를 뺀 값을 k에 할당
        a = 10;         // 현재 객체(this)의 a를 10으로 업데이트
        obj.a = 20;     // obj 객체의 a를 20으로 업데이트
        return k;       // k 값을 반환
    }
}

public class PassRef {
    public static void main(String[] args) {
        // Ref 클래스의 객체 생성 및 초기화
        Ref obj1 = new Ref(3);
        Ref obj2 = new Ref(4);

        // sum 메서드 호출하여 obj2에서 obj1을 참조하고 반환값을 변수 k1에 저장
        int k1 = obj2.sum(obj1);

        // 결과 출력
        System.out.print("k1 = " + k1);       // k1의 값 출력
        System.out.print(" obj1.a = " + obj1.a);  // obj1 객체의 a 출력
        System.out.print(" obj2.a = " + obj2.a);  // obj2 객체의 a 출력
    }
}

**상속, 객체 생성**
````
class C{}
class CS extends C {}
interface I {
class CI extends C implements I {}

class Example {
static I i = new CI();
static C ca = new CI();
static CS ca = new C(); // 오류 : c 클래스와 CS 클래스 간의 상속 관계는 없다
static C cb = new CS();

}
}

````
