**Q7 C++ 생성자(정보처리기사 20년 3회)**
````
해당 클래스의 객체가 생성될 때 자동으로 호출되는 특수한 종류의 메서드
````

**Q8 n이 10 일 때, 10을 2진수로 변환하는 코드(정보처리기사 20년 4회)**
````
class Q8 {
	public static void main (String[] args) {
    	int[]a = new int[8];
        int i=0; int n=10;
        while (  1.  ) { // n>0 : n이 0보다 큰 동안 반복
        	a[i++] = (  2.  ); // n%2 : 배열 a의 i번째 요소에 n을 2로 나눈 나머지를 저장하고, i를 1 증가
            n /= 2; // 'n'을 2로 나눈 몫으로 갱신, 'n'을 2진수로 변환하는 과정에서 자리수를 한자리씩 줄여나가는 것 의미
        }
        for(i=7; i>=0; i--) // 이진수 변환을 마친 배열 'a'를 거꾸로 출력하기 위한 루프
{
         System.out.print(a[i]);
        }
     }
  }
````

**Q9 (정보처리기사 20년 4회)**
````
<출력결과>
1 4 7 10 13
2 5 8 11 14
3 6 9 12 15

public class Q9 {
    public static void main(String[] args) {
        int[][] a = new int[3][5]; // 2차원 배열 a를 선언하고, 행(row)은 3, 열(column)은 5인 배열을 생성

        for (int i = 0; i < 3; i++) {     // i는 0부터 2까지 반복
            for (int j = 0; j < 5; j++) { // j는 0부터 4까지 반복
                a[i][j] = j * 3 + (i + 1); // a[i][j]에 값을 할당하는데, (i+1)은 행 번호에 따른 보정값
                System.out.print(a[i][j] + " "); // a[i][j]의 값을 출력하고 공백을 추가
            }
            System.out.println(); // 한 행의 출력이 끝나면 줄바꿈을 수행
        }
    }
}

````

**Q10 (정보처리기사 20년 4회)**
````
class parent {
    public int compute(int num) {
        if (num <= 1) return num; // num이 1 이하일 경우 num을 반환
        return compute(num - 1) + compute(num - 2); // num을 바탕으로 재귀적으로 계산하여 반환
    }
}

class Child extends parent {
    public int compute(int num) {
        if (num <= 1) return num; // num이 1 이하일 경우 num을 반환
        return compute(num - 1) + compute(num - 3); // num을 바탕으로 재귀적으로 계산하여 반환
    }
}

class Q10 {
    public static void main(String[] args) {
        parent obj = new Child(); // 부모 클래스의 객체를 자식 클래스로 초기화
        System.out.print(obj.compute(4)); // obj의 compute 메서드를 호출하여 결과 출력
    }
}

// 상속 관련 공부 더 해야할 듯 
````


