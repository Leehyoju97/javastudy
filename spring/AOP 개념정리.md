## AOP
- 부가 기능을 모듈화하여 애플리케이션 전체에 걸쳐 사용하는 기능을 재정의 하는 것을 의미한다.
예를 들어 A라는 클래스가 회원가입이라는 기능이 있을 때 걸리는 시간을 알고 싶다면 회원가입 메소드 안에 코드를 작성하면 될것이다. 
하지만 1억개 정도 되는 메소드에 걸리는 시간을 구해야 된다면 모든 메소드에 걸리는 시간에 대한 코드를 작성하는 일은 매우 힘들고 수정해야 할일이 있다면 상당히 힘들 것이다.
이러한 문제를 aspect를 사용해 해결한다.

### AOP 용어

1. aspect
- 동일한 concern으로 모듈화하는 기능이다.
- advice + pointcut

2. advice
- aspect가 무엇을 언제할지 정의한다.
- Before : 메소드 실행 전
- After : AfterReturning + AfterThrowing
- AfterReturning : 정상 반환 이후
- AfterThrowing : 예외 발생 이후
- Around : before + after

3. pointcut
- advice를 정의할 jointpoint를 선별하는 기능이다.
- 실제 advice가 적용되는 시점

4. target
- 부가기능을 적용할 대상

5. jointpoint
- advice가 적용될 위치를 말한다. (spring에서는 메소드조인포인트만 제공)
- 메서드, 필드, 객체, 생성자 등
