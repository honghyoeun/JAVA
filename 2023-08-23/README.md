**Q1 반복문 (정보처리기사 20년 1회)**

````
public class Q1 {
    public static void main(String[] args) {
        int i; // 정수형 변수 i를 선언
        int[] a = {0, 1, 2, 3}; // 크기가 4인 정수형 배열 a를 선언하고 초기화

        // 배열 a의 요소들을 반복문을 통해 출력
        for (i = 0; i < 4; i++) { // i를 0부터 시작하여 3까지 반복 (총 4번 반복)
            System.out.print(a[i] + ""); // 현재 인덱스 i에 해당하는 배열 a의 요소를 출력
        }
    }
}

````

**Q2 Switch 반복문 (정보처리기사 20년 1회)**
````
public class Q2 {
    public static void main(String[] args) {
        int i = 3; // 변수 i에 3을 할당
        int k = 1; // 변수 k에 1을 할당

        switch (i) { // 변수 i의 값에 따라 다양한 경우를 처리할 switch 문
            case 0: // i가 0인 경우
            case 1: // i가 1인 경우
            case 2: // i가 2인 경우
            case 3: // i가 3인 경우
                k = 0; // k를 0으로 설정
            case 4: // i가 4인 경우
                k += 3; // k에 3을 더하기
            case 5: // i가 5인 경우
                k -= 10; // k에서 10을 뺴기
            default:
                k--; // switch 문의 어떤 case에도 해당하지 않는 경우 k에서 1 뺴기
        }

        System.out.print(k); // 최종적인 변수 k의 값을 출력
    }
}
````

**Q3. 상속 (정보처리기사 20년 2회)**
````
class Parent {
    public void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {
    public void show() {
        System.out.println("Child");
    }
}

public class Q3 {
    public static void main(String[] args) {
        Parent pa = new Child(); // Parent 타입의 변수에 Child 객체를 할당, 즉 클래스의 변수 'pa'를 선언하고, 'Child' 클래스의 객체를 할당
        pa.show(); // 변수 'pa'는 'Parent' 클래스의 변수이지만, 객체는 'Child' 클래스의 객체이다. 따라서 'Child' 클래스의 'show()'메서드가 호출되어 'Child'가 출    }
}

// 상속 장점 : 코드 재사용을 높일 수 있고, 클래스 간의 관계를 더욱 명확하게 표현 가능
````

**Q1-Q3 손코딩**
![image](https://github.com/honghyoeun/JAVA/assets/77725041/89f8439c-710e-481a-9891-476f5a7125c1)

