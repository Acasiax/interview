# interview

===, !==    식별 연산자 - 두개의 참조가 같은 인스턴스를 가르키고 있는지를 비교하는 방법

lazy var 는 값을 초기화 (설정) 해야함

메모리 공간 낭비나 불필요한 성능저하를 예방할 수 있음

계산속성 get set

- 실제로, 계산 속성은 겉모습은 속성(변수) 형태를 가진 메서드(함수)임
- 계산 속성은 실제 메모리 공간을 가지지 않고, 해당 속성에 접근했을때 다른 속성에 접근해서 계산한후, 그 계산 결과를 리턴하거나 세팅하는 메서드 이다.

### **Swift에서의 ARC와 GC의 차이**

- **ARC**: Swift에서 사용하는 메모리 관리 방식으로, 컴파일 시간에 메모리 관리 코드를 삽입합니다. ARC는 런타임 오버헤드가 없으며, 개발자가 메모리 관리에 더 세밀하게 접근할 수 있도록 합니다.
- **GC**: 런타임 중에 메모리를 자동으로 관리하는 방식으로, Swift에서는 사용되지 않습니다. GC는 메모리 관리를 자동화하지만, 런타임 중에 수행되기 때문에 성능 저하를 일으킬 수 있습니다.

Swift를 사용할 때는 ARC의 원리와 참조 순환을 방지하는 방법(예: 약한 참조(weak)와 미소유 참조(unowned) 사용)을 이해하는 것이 중요합니다. 이렇게 하면 메모리 관리를 효율적으로 수행하고, 성능 문제를 최소화할 수 있습니다.


## 💡프로토콜이란 무엇인가요?
네 프로토콜은 특정 작업을 요구하기 위한 '계약서'로 생각합니다. 우선 프로토콜 키워드를 사용해서 (메서드명,변수,변환타입등)요구사항틀을 만들고
클래스에 프로토콜을 채택하여 요구사항을 정의한 다음, 다른 클래스에서 var 딜리게이트를 사용하여 사용하는 것으로 알고 있습니다.


## 프로토콜이란 무엇인가요?
프로토콜은 특정 작업을 요구하기 위한 '계약서'로 생각합니다. 일단 프로토콜은 protocol 키워드를 사용해서 정의하고 
요구사항은 항상 var 키워드로 선언하고, { get } 또는 { get set }으로 표시하여 읽기/쓰기 가능 여부를 명시한 다음에
메서드 요구사항은 실행 가능한 코드 없이 메서드의 이름, 매개변수, 반환 타입만을 정의합니다.

그 다음 클래스에 프로토콜을 채택해서 요구사항을 정의한 다음
다른 클래스에서 프로토콜을 채택한 딜리게이트를 var로 연결시켜서 딜리게이트. 점 하여 사용하는 것으로 알고 있습니다.

## 💡딜리게이트이란 무엇인가요?
딜리게이트 패턴은 1:1 통신을 위한 것으로, 객체가 특정 이벤트 처리라던지 데이터 전달 등의 책임을 다른 객체에 위임하는 것으로 알고 있습니다.

프로토콜과 딜리게이트를 사용하면, 코드의 유연성과 재사용성을 높이며, 각 객체의 역할을 명확하게 파악 할 수 있는 장점이 있습니다.

## 구조체에서는 싱글톤 패턴을 안쓰나요?

구조체는 값 타입입니다. 값 타입은 복사될 때마다 '새로운 인스턴스가 생성'되므로, 싱글톤 패턴을 구현하는 데 적합하지 않습니다. 

싱글톤 인스턴스에 접근할 때마다 동일한 인스턴스에 접근해야 하지만, 구조체를 사용하면 복사본이 생성되어 이 원칙이 깨집니다.
따라서 Swift에서 싱글톤 패턴을 구현할 때는 클래스를 사용하는 것이 일반적입니다.


