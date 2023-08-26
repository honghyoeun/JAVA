**Q11 (정보처리기사 21년 1회)**
````
public class Q11 {
    public static void main(String[] args) {
        // 2차원 배열을 생성하고 초기화
        int[][] arr = new int[][]{{45, 50, 75}, {89}};

        // arr[0] 배열의 길이 출력
        System.out.println(arr[0].length); // 3 (45, 50, 75)

        // arr[1] 배열의 길이 출력
        System.out.println(arr[1].length); // 1 (89)

        // arr[0][0]의 값 출력
        System.out.println(arr[0][0]); // 45

        // arr[0][1]의 값 출력
        System.out.println(arr[0][1]); // 50

        // arr[1][0]의 값 출력
        System.out.println(arr[1][0]); // 89
    }
}

````

**Q12 (정보처리기사 21년 1회)**
````
public class Q12 {
    public static void main(String[] args) {
        int i, j;

        // i와 j를 초기화하고 for 루프 시작
        for (j = 0, i = 0; i <= 5; i++) {
            j += i;  // j에 i를 더함

            System.out.print(i);  // 현재 i 값을 출력

            if (i == 5) {  // i가 5일 때
                System.out.print("=");  // 등호 출력
                System.out.print(j);    // 최종 덧셈 결과 j 출력
            } else {
                System.out.print("+");  // 다른 경우에는 덧셈 기호 출력
            }
        }
    }
}

````

**Q13 (정보처리기사 21년 2회)**
````
public class over1 {
    public static void main(String[] args) {
        ovr a1 = new ovr1();  // ovr1 클래스의 인스턴스를 생성하여 a1 변수에 할당
        ovr a2 = new ovr2();  // ovr2 클래스의 인스턴스를 생성하여 a2 변수에 할당
        System.out.println(a1.sum(3, 2) + a2.sum(3, 2));  // 결과 출력, 5 + 6 = 11
    }

    int sum(int x, int y) {
        return x + y; // 3+2
    }
}

class ovr2 extends ovr1 {

    int sum(int x, int y) {
        return x - y + super.sum(x, y); // 3-2 + 5
    }

    // 여기에 다른 메소드들도 추가 가능
}

````
