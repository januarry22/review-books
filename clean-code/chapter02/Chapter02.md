# Chapter 2. 의미 있는 이름

### 의미가 분명한 이름 짓기

```bash
	int a;
	String b;

	변수 a 와 b 의 역할과 타입을 고려해 상세한 변수명이 필요하다.

	int itemCount;
	String itemName;

	의도가 드러나는 이름을 사용하면 코드 이해와 변경이 쉬워진다.
```

### 루프 속 i j k 사용하지 않기

```bash
for(int i =0; i < message.size(); i++){

...
}

배열을 순회할 떄 index를 의미하는 i를 사용하지 않고
advanced for 문으로 대체할 수 있다.

for(String message : messages){
..
}

lamda 를 사용할 수도 있다.

messages.stream().forEach()
	message -> ..
)
```

### 통일성 있는 단어 사용하기

```bash
Member / Customer / User
Servece / Manager
Repository / DAO

팀간의 소통을 통해 하나의 통일성 있는 클래스 네임으로 명시한다.
```

### 변수명에 타입 넣지 않기

```bash
Stirng nameString (👎)-> name 
Int itemPriceAmount (👎) -> itemPrice

List<Account> accountList (👍) ->accounts, accountList
```

### Google Java Naming Guide

- Package Naming Guide
    - All lower case, no underscores
        
        ```bash
        com.example.deepspace (👍)
        com.example.deepSpace (👎)
        com.example.deep_space (👎)
        ```
        
- Class Naming Guide
    - UpperCamelCase (대문자로 시작)
        
        ```bash
        // 클래스는 명사, 명사구
        Character, ImmutableList
        
        // 인터페이스는 명사, 명사구, (형용사)
        List, Readable
        
        // 테스트 클래스는 Test로 끝나기
        HashTest, HashIntegrationTest
        ```
        

- Method Naming Guide
    - LowerCamelCase (소문자로 시작)
        
        ```bash
        // 메서드는 동사, 동사구
        sendMessage, stop
        
        //jUnit 테스트에 underscore 사용되기도 함
        //<methodUnderTest>_<state> 패턴
        pop_emptyStack
        ```