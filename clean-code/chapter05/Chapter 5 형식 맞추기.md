# Chapter 5. 형식 맞추기

# 01 포맷팅이 중요한 이유

### 가독성에 필수적

- 코드를 수월하게 읽어나갈 수 있다.
- 아마추어처럼 보이지 않음 (?)
- 포맷팅으로 인해 코드를 잘못해석해 버그를 발생할 위험을 줄인다.
- 유지보수와 확장성에 지속적으로 영향

# 02 클린코드 포맷팅

### 적절한 행 길이를 유지

- 200라인 (~ 500라인)
    - 코드 길이가 200라인을 넘어가면, 클래스가 여러개의 일을 하고 있을 수 있다.(SRP 위배)
    

### 밀접한 개념은 서로 가까이 둔다.

- 행 묶음은 완결된 생각 하나를 표현하기하기 떄문에 개념은 빈행으로 분리한다.
- 변수는 사용되는 위치에서 최대한 가까이 선언한다.

# 03 Java Class Declarations

### Class 내부 코드 순서

1. static 변수
    - public → protected → package → private
2. instance 변수
    - public → protected → package → private
3. 생성자
4. 메서드
    - public 메서드에서 호출되는 private 메서드는 그 아래에 둔다. 가독성 위주로 그룹핑

# 04 Team Coding Convention

### 팀의 코딩 스타일에 관한 약속 👍

- MySQL Convention : 컬럼명은 snake_case로 네이밍한다.
- Team Convention : enum 타입으로 사용하는 varchar 타입의 경우 컬럼명의 _type으로 끝나도록 네이밍한다.

[Google Java Style Guide](https://google.github.io/styleguide/javaguide.html)

[캠퍼스 핵데이 Java 코딩 컨벤션](https://naver.github.io/hackday-conventions-java/)