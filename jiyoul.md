# 스프링 핵심 원리 - 기본편
Inflearn 김영한님 강의 : 스프링 핵심 원리 - 기본편

※ 1일차 ※

IOC : 제어의 역전

SOLID
SRP : 단일책임원칙(Single Responsibility Principle)
- 중요한 기준은 변경이다! 변경이 있을때 파급 효과가 적으면 잘 따른것이다.
- 한 클래스는 하나의 책임만 가져야 한다.
- 하나의 책임이라는 것은 모호하다.
- ex) UI변경, 객체의 생성과 사용을 분리하는것.

OCP : 개방-폐쇄 원칙(Open / Closed Principle)
- 확장에는 열려있고 변경에는 닫혀있어야 한다.
- 다형성을 활용할것.
* 다형성을 사용했지만 OCP 원칙을 지킬 수가 없음.
* 이때문에 객체를 생성하고 연관관계를 맺어주는 별도의 조립, 설정자가 필요 = 스프링 컨테이너(IOC, DI 등)
- 인터페이스를 구현한 새로운 클래스를 만들어서 새로운 기능을 또 구현가능.


LSP : 리스코프 치환 원칙(Liskov Substitution Principle)
- 예를 들어 엑셀(인터페이스)은 밟으면(구현) 앞으로만 가야함.(뒤로가면 안됨. 기능보장하기)
- 객체는 프로그램의 정확성을 깨지않고 하위 타입의 인스턴스를 바꿀 수 있어야 한다.
- 하위 클래스는 인터페이스의 규약을 다 지켜야함.

ISP : 인터페이스 분리 원칙(Interface segregation principle)
- 범용 인터페이스 하나보다 여러개의 인터페이스가 낫다.
- 정비 인터페이스의 정비사 기능을 바꾸는데 운전자 기능이 바뀌면 안됨.
- 인터페이스를 분리하면 명확해지고 대체 가능성이 높아진다.

DIP : 의존관계 역전 원칙(Dependency Inversion Principle)
- 로미오를 연기하는 사람이 줄리엣만 알면 되지 줄리엣의 배우까지 알필요는 없음.
- 구현 클래스에 의존하지 말고 인터페이스에 의존해야 한다.

개발방법 정리
- 이상적인 개발은 모든설계에 인터페이스를 부여하는것이 좋다.
* 배보다 배꼽이 더 클때도 있음.
* 기능을 확장할 가능성이 없으면 구체 클래스를 바로 하고 나중에 인터페이스로 리팩토링해도 됌.
- 모든 역할과 구현을 분리하자.