1. **생성자 (Constructor)**:
   - 생성자는 객체를 초기화하는 특별한 메서드
   - 클래스의 인스턴스를 만들 때 호출되며, 객체의 초기 상태를 설정
   - 생성자는 클래스 이름과 동일하며 반환 타입이 없음.
   - 예: 
     ```java
     public class MyClass {
         public MyClass() {
             // 생성자 내부에서 초기화 코드 작성
         }
     }
     ```

2. **오버로딩 (Overloading)**:
   - 오버로딩은 같은 이름의 메서드나 생성자를 여러 번 정의하는 것을 의미
   - 메서드나 생성자의 매개변수 개수나 데이터 타입을 다르게 하여 다양한 호출을 지원
   - 컴파일러는 전달된 인자에 따라 올바른 메서드나 생성자를 호출
   - 예:
     ```java
     public int add(int a, int b) {
         return a + b;
     }
     
     public double add(double a, double b) {
         return a + b;
     }
     ```

3. **오버라이딩 (Overriding)**:
   - 오버라이딩은 상위 클래스에서 정의된 메서드를 하위 클래스에서 다시 정의하는 것을 의미
   - 메서드 시그니처(메서드 이름, 매개변수 타입 및 순서)는 동일
   - 하위 클래스에서 오버라이딩된 메서드는 상위 클래스의 메서드를 대체하며, 다형성을 지원
   - 예:
     ```java
     class Animal {
         public void makeSound() {
             System.out.println("Animal makes a sound");
         }
     }
     
     class Dog extends Animal {
         @Override
         public void makeSound() {
             System.out.println("Dog barks");
         }
     }
     ```
