**Q4 (정보처리기사 20년 3회)**
````
class A {
    private int a;  // 클래스 A의 멤버 변수로서 private 접근 제어자로 선언된 정수형 변수 a

    public A(int a) {  // 클래스 A의 생성자 메소드
        this.a = a;  // 생성자를 통해 전달받은 값을 멤버 변수 a에 할당
    }

    public void display() {  // 클래스 A의 메소드 display()
        System.out.println("a=" + a);  // 멤버 변수 a의 값을 출력
    }
}

class B extends A {  // 클래스 B가 클래스 A를 상속받음
    public B(int a) {  // 클래스 B의 생성자 메소드
        super(a);  // 부모 클래스 A의 생성자 호출하여 초기화
        super.display();  // 부모 클래스 A의 display() 메소드 호출하여 출력
    }
}

public class Q4 {  // 메인 클래스인 Q4
    public static void main(String[] args) {  // 프로그램의 시작점
        B obj = new B(10);  // 클래스 B의 생성자를 호출하여 객체 생성
    }
}

````

**Q5 (정보처리기사 20년 3회)**
````
public static Q5
public class Q5 {  // 클래스 Q5 선언

    public static void main(String[] args) {  // 프로그램의 시작점

        int i = 0;  // 정수형 변수 i 초기화
        int sum = 0;  // 합을 저장할 변수 sum 초기화

        while (true) {  // 무한 루프 시작
            i++;  // i 값을 1씩 증가

            if (i % 2 == 1)  // i가 홀수라면
                continue;  // 다음 루프 반복을 위해 continue 문을 사용하여 건너뜀

            sum += i;  // 짝수 i 값을 sum에 더함

            if (i >= 10)  // i가 10 이상이면 반복 종료
                break;  // 반복문 탈출
        }

        System.out.println(sum);  // 최종적으로 구해진 짝수의 합인 sum을 출력
    }
}

````

**Q6 (정보처리기사 20년 3회)**
````
abstract class Vehicle {
    String name;  // 문자열 형태의 name 멤버 변수 선언

    abstract public String getName(String val);  // 추상 메소드 선언

    public Vehicle(String val) {  // 생성자 메소드
        this.name = val;  // 전달받은 값을 멤버 변수 name에 할당
    }

    public String getName() {
        return "Vehicle name: " + name;  // name 값을 포함한 문자열 반환
    }
}

class Car extends Vehicle {
    public Car(String val) {
        super(val);  // 부모 클래스 생성자 호출하여 name 초기화
    }

    public String getName(String val) {
        return "Car name: " + val;  // 전달받은 val 값을 포함한 문자열 반환
    }

    public String getName(byte val[]) {
        return "Car name: " + val;  // 전달받은 byte 배열 val 값을 포함한 문자열 반환
    }
}

public class Exam {
    public static void main(String[] args) {
        Vehicle obj = new Car("Spark");  // Car 클래스의 객체 생성
        System.out.println(obj.getName());  // obj의 getName 메소드 호출 및 결과 출력
    }
}

````





