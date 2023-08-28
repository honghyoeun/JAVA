**Q14 (정보처리기사 21년 3회)**
````
class Connection {
    private static Connection _inst = null;  // Connection 클래스의 인스턴스를 담을 private 정적 변수
    private int count = 0;  // 카운트를 위한 멤버 변수

    static public Connection get() {  // 인스턴스를 반환하는 정적 메서드
        if (_inst == null) {  // 인스턴스가 생성되지 않았다면
            _inst = new Connection();  // 새로운 인스턴스 생성
            return _inst; 
        }
        return _inst;  // 기존 인스턴스 반환
    }

    public void count() {  // 카운트 증가 메서드
        count++;
    }

    public int getCount() {  // 카운트 값을 반환하는 메서드
        return count;
    }
}

public class testcon {
    public static void main(String[] args) {
        Connection conn1 = Connection.get();  // Connection 클래스의 인스턴스 가져오기
        conn1.count();  // 카운트 증가
        Connection conn2 = Connection.get();
        conn2.count();
        Connection conn3 = Connection.get();
        conn3.count();
        
        System.out.print(conn1.getCount());  // 카운트 값 출력
    }
}

````

**Q15 (정보처리기사 21년 2회)**
````
public class Test {
   public static void main(String[] args){
      system.out.print(test.check(1));
   }
   
   (    )  String check (int num) // 빈칸 static : 객체 생성 없이 메소드 이용하기 위함

{
      return (num >= 0) ? "positive" : "negative";
   }
}

[출력결과]
positive
````

**Q16 (정보처리기사 2)**
````
public class testco {
    public static void main(String[] args) {
        int a = 3, b = 4, c = 3, d = 5;

        // 첫 번째 if 문의 조건 분석
        if ((a == 2 | a == c) & !(c > d) & (1 == b ^ c != d)) {
            // 첫 번째 if 문의 조건이 true일 때 실행되는 블록
            a = b + c;  // a에 b + c의 값을 대입 (a = 4 + 3 = 7)

            // 중첩된 if 문의 조건 분석
            if (7 == b ^ c != a) {
                // 중첩된 if 문의 조건이 false이므로 이 블록은 실행되지 않음
                System.out.println(a);
            } else {
                // 중첩된 if 문의 조건이 false이므로 이 블록이 실행됨
                System.out.println(b);  // 출력: 4
            }
        } else {
            // 첫 번째 if 문의 조건이 false일 때 실행되는 블록
            a = c + d;  // a에 c + d의 값을 대입 (a = 3 + 5 = 8)

            // 중첩된 if 문의 조건 분석
            if (7 == c ^ d != a) {
                // 중첩된 if 문의 조건이 true이므로 이 블록이 실행됨
                System.out.println(a);  // 출력: 8
            } else {
                // 중첩된 if 문의 조건이 true이므로 이 블록은 실행되지 않음
                System.out.println(d);
            }
        }
    }
}

````
