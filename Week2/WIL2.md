WIL2
===============

# 컨트롤러, 서비스, 리포지토리의 역할
1. 컨트롤러는 MVC 패턴에서 Controller에 해당하는 역할을 한다. 컨트롤러는 웹 사용자의 요청을 처리하고 View를
반환한다. 사용자의 요청은 서비스 객체를 통하여 이루어진다. View의 반환은 model 객체를 통해 이루어진다. 그리고
컨트롤러는 서비스와 의존 관계를 가진다.
2. 서비스는 웹 사용자의 요청을 실질적으로 처리하는 영역이라 할 수 있다. 서비스 내에는 사용자의 요청을 처리하기
위한 여러가지 로직들이 구현되어있다. 서비스는 리포지토리와 의존 관계를 가진다. 서비스는 필요할 때마다 리포지토리를 통하여 데이터베이스에 접근한다. 
3. 리포지토리는 도메인 객체들을 저장하는 장소이다. 리포지토리에는 간단한 로직들만이 구현되어있고 서비스에서 구체화된다. 또한 리포지토리를 통해 데이터베이스에 접근한다. 

# TDD란? 왜 하는가?
1. TDD는 Test Driven Development의 약자로서 '테스트 주도 개발'이라고 한다.
구체적으로 TDD에 대해 설명하자면 테스트 코드를 작성한 후 실제 코드를 작성하는 것이다. 일반적으로 디자인 -> 코드개발 -> 테스트 -> 배포 의 형식으로 개발하는 것과 대조적으로 디자인 -> 테스트 코드 작성 -> 코드개발 의 형식을 지닌다.
2. 테스트 코드를 작성한 후 코드 개발을 하기 때문에 즉각적인 피드백이 가능하다.
또한 TDD를 통해 코드복잡도를 줄일 수 있고 새로운 기능 추가시 기존 기능들이 충돌 없이 잘 작동하는지 확인 가능하다. 그리고 TDD를 함으로써 디버깅 시간을 줄일 수 있다.