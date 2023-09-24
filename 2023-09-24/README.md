**Q1**
````
public class soojebi {

    // getValue() 메서드 정의
    public static int getValue(int[] n) {
        int sum = 0; // 배열 요소의 합을 저장할 변수를 초기화

        // 향상된 for 루프를 사용하여 배열의 각 요소를 반복
        for (int i : n) {
            sum += i; // 각 요소를 sum 변수에 더하기
        }

        return sum / n.length; // 배열 요소의 평균을 계산하고 반환 
    }

    // main() 메서드 정의
    public static void main(String[] args) {
        int[] num = { 90, 80, 90 }; // 정수 배열 num을 선언하고 초기화
        System.out.print(getValue(num)); // getValue() 메서드를 호출하고 결과를 출력
    }
}

````
