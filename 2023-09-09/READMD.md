## 예외처리 _Exception
````
try { //  오류 없으면 안 해도 됨
.
.
}
  catch
    {  exception// 예외 발생 (여러개 가능), 오류 발생 시 실행
     .
     .
    }
      finally // 무조건 실행
           {

           }

// 예외처리문 외 문장은 정상 출력
 ````

## throw
- throw new Exception // 강제 예외 시키기
- throw e; // 다른 예외 호출하기 >> finally 전에 있더라도 무조건 finally 출력 후 넘어가기, 없을 시 생략없이 수행

## 생성자 
- 생성자 특징 : 생성자는 부모를 명시적으로 호출되지 않으면(ex. super 없는 경우) 인자없는 부모 값을 호출한다.
- 예시 : B b1 = new B()

## 오버로딩 
- 클래스는 같고 매개변수 다른 경우

## 오버라이딩
- 클래스와 매개변수 모두 같은 경우
- 부모를 자식으로 재정의한다. 
