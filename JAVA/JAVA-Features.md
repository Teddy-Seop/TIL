# JAVA-Features
------------
## 자바의 특징
#### 객체 지향 언어
- 자바는 객체 지향 언어로 캡슐화, 상속, 다형성 등을 지원

#### 플랫폼의 독립성
- 하드웨어, 운영체제 등 플랫폼에 종속되지 않는 독립적인 바이트 코드로 컴파일됨
- 자바 가상 머신(JVM)만 있으면 하드웨어/운영체제를 가리지 않고 자바 프로그램의 실행이 가능

#### 클래스로 캡슐화
- 객체의 필드, 메소드를 하나로 묶고 실제 구현 내용을 외부에 감추는 것을 의미
- 외부 객체는 내부의 구조를 알지 못하며 객체가 노출해서 제공하는 필드와 메소드만 이용할 수 있음
- 필드와 메소드를 캡슐화하여 보호하는 이유는 외부의 잘못된 사용으로 인해 객체가 손상되지 않도록 하는 데 있음
- 캡슐화된 멤버를 노출시킬지 숨길지 결정하기 위해 접근 제한자를 사용
- 클래스에 속하지 않는 필드나 메소드는 존재 할 수 없고 클래스 안에 새로운 클래스, 즉 내부 클래스를 만들 수 있음

#### 소스와 클래스 파일
- 자바 소스가 컴파일된 클래스 파일에는 반드시 하나의 자바 클래스만이 들어있음
- 하나의 자바 소스파일에 여러 개의 클래스를 작성했을 때 컴파일 하면 클래스마다 별도의 클래스 파일이 생성됨

#### 실행 모듈
- 자바 응용프로그램은 한 개의 클래스 파일 또는 다수의 클래스 파일로 구성됨
- 다수의 클래스 파일을 jar파일 형태로 압축하여 배포 및 실행이 가능
- 자바의 실행은 main() 메소드에서 시작되며 하나의 클래스 파일에 두 개 이상의 main()메소드가 있을 수 없음 (각 클래스 파일이 main()메소드를 가지는 것은 상관 없음)

#### 패키지
- 서로 관련 있는 클래스는 패키지로 묶어 관리
- 파일 시스템의 폴더 개념과 같음

#### 멀티스레드
- 하나의 자바 프로그램에서 다수의 스레드가 동시에 실행될 수 있는 환경을 지원
- 일반적인 멀티스레드 프로그램을 작성하기 위해서는 운영체제가 멀티스레드르 지원 또는 API나 라이브러리를 제공해야함
- 자바는 운영체제의 도움없이 멀티스레드 프로그래밍이 가능

#### Garbage Collection
- 자바 언어는 메모리를 할당받는 기능이 있지만 메모리를 반환하는 기능은 없어 프로그래밍의 부담을 대폭 줄여줌
- 프로그램 내에 사용되지 않는 메모리는 `JVM`의 `Garbage Collection`기능에 의해 자동으로 회수됨

#### 실시간 응용 시스템에 부적합
- 자바 응용프로그램은 실행 도중 예측할 수 없는 시점에 `Garbage Collection`이 실행되므로 프로그램 실행이 일시적으로 중단됨
- 일정 시간 내에 반드시 실행 결과를 내야하는 실시간 시스템에는 자바가 부적합함

#### 자바 프로그램의 안전성
- 타입 체크가 매우 엄격
- `C/C++`과 다르게 메모리의 물리적 주소를 사용하는 포인터의 개념이 없기 때문에 잘못된 코드로 컴퓨터 시스템이 중단되는 일이 없음

#### 프로그램 작성이 쉬움
- 포인터의 개념이 없음
- 다양한 라이브러리와 스윙 등 GUI 라이브러리를 지원하므로 프로그램 작성이 빠르고 쉬움
