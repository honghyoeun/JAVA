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
