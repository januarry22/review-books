# Chapter 3. 함수

# 01 SOLID

[The S.O.L.I.D Principles in Pictures](https://medium.com/backticks-tildes/the-s-o-l-i-d-principles-in-pictures-b34ce2f1e898)

### 객체지향 설계의 5가지 원칙

- **SRP  단일 책임의 원칙 : 한 클래스는 하나의 책임만 가져야 한다.**
    - 클래스는 하나의 기능만 가지며, 어떤 변화에 의해 클래스를 변경해야 하는 이유는 오직 하나뿐이어야 한다.
    - SRP 책임이 분명해지기 때문에, 변경에 의한 연쇄작용에서 자유로워 질 수 있다.
    - 가독성 향상과 유지보수가 용이해진다.
    - 실전에서 쉽지 않지만 늘 상기해야함 !
- **OCP 개발-폐쇄 원칙 : 소프트웨어 요소는 확장에는 열려 있으나 변경에는 닫혀 있어야 한다.**
    - 변경을 위한 비용은 가능한 줄이고, 확장을 위한 비용은 가능한 극대화 해야 한다.
    - 요구사항의 변경이나 추가사항이 발생하더라고, 기존 구성요소에는 수정이 일어나지 않고, 기존 구성 요소를 쉽게 확장해서 재사용한다.
    - 객체지향의 추상화와 다형성을 활용한다.
- **LSP 리스코프 치환 원칙 : 서브 타입은 언제나 기반 타입으로 교체할 수 있어야 한다.**
    - 서브 타입은 기반 타입이 약속한 규약(접근제한자, 예외 포함)을 지켜야한다.
    - 클래스 상속, 인터페이스 상속을 이용해 확장성을 획득한다.
    - 다형성과 확장성을 극대화하기 위해 인터페이스를 사용하는 것이 더 좋다.
    - 합성(composition)을 이용할 수도 있다.
- **ISP 인터페이스 분리 원칙 : 자신이 사용하지 않는 인터페이스는 구현하지 말아야 한다.**
    - 가능한 최소한의 인터페이스만 구현한다.
    - 만약 어떤 클래스를 이용하는 클라이언트가 여러 개고, 이들이 클래스의 특정 부분만 이용한다면, 여러 인터페이스로 분류하여 클라이언트가 필요한 기능만 전달한다.
    - SRP가 클래스의 단일 책임이라면, ISP는 인터페이스의 단일 책임
- **DIP 의존성 역전 원칙 : 상위 모델은 하위 모델에 의존하면 안된다. 둘다 추상화에 의존해야 한다. 추상화는 세부 사항에 의존해서는 안된다. 세부 사항은 추상화에 따라 달라진다.**
    - 하위 모델의 변경이 상위 모듈의 변경을 요구하는 위계관계를 끊는다.
    - 실제 사용관계는 그대로이지만, 추상화를 매개로 메시지를 주고 받으면서 관계를 느슨하게 만든다.
    

# 02 간결한 함수 작성하기

### 한가지만 하기(SRP), 변경에 닫게 만들기(OCP)

- 로직과 타입을 분리함

### 함수 인수

- 인수의 갯수는 0~2 개가 적당.
- 3가지 이상인 경우 ?
    - 객체를 인자로 넘기기
    - 가변 인자를 넘기기 → 특별한 경우를 제외하고는 사용 안함

# 03 안전한 함수 작성하기

### 부수 효과 (Side Effect) 없는 함수

<aside>
💡 Side Effect?
값을 반환하는 함수가 외부 상태를 변경하는 경우

</aside>

# 04 함수 리팩터링

1. 기능을 구현하는 서투른 함수를 작성
    - 길고, 복작하고, 중복도 있음
2. 테스트 코드를 작성
    - 함수 내부의 분기와 엣지값마다 빠짐없이 테스트하는 코드를 짠다.
3. 리팩터링
    - 코드를 다듬고, 함수를 쪼개고, 이름을 바꾸고, 중복을 제거한다.

## 실습 01.

✅ 부동산 중개 보수 산출 통한 클린코드 실습해보기 

[서울시 부동산 정보광장 메인](http://land.seoul.go.kr)

![스크린샷 2022-04-14 오후 11.29.06.png](Chapter%203%20%E1%84%92%E1%85%A1%E1%86%B7%E1%84%89%E1%85%AE%202800330fa6864dd88c881715e913f001/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-04-14_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_11.29.06.png)