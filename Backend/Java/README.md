# Java

<details>
<summary>static</summary>
static 키워드를 통해, 정적 변수 및 정적 메소드를 사용할 수 있다.

정적 변수와 정적 메소드는 프로그램 시작 시점에 메모리에 한번 할당되어, 프로그램이 종료되는 시점에 메모리에서 해제된다.

일반적으로 new 키워드로 생성된 객체들은 heap영역에 생성되어, Garvage Collector (GC)에 관리를 받는다. 반대로, static 키워드로 static 영역에 생성된 메모리는 GC의 관리를 받지 않는다.
(이때 class들도 static 영역에 생성된다.)
</details>

<details>
<summary>Access Modifier</summary>
접근 제한자 혹은 접근 지정자

클래스, 인터페이스 혹은 멤버에 대한 접근을 제한하기 위해 사용되는 키워드이다.

public, protected, private이 있고, 아무 제한자가 사용되지 않았을 때 사용되는 default 제한자가 존재한다.

* public [클래스 / 멤버]: 외부 클래스가 자유롭게 사용 가능하다.
* protected [멤버]: 같은 패키지 (클래스들의 모음) 혹은 자식 클래스에서 사용 가능하다. (부모 클래스는 사용하지 못한다는 의미)
* private [멤버]: 외부에서 사용할 수 없다.
* default [클래스 / 멤버]: 같은 패키지에 소속된 클래스만 사용할 수 있다.

Java는 객체지향언어로, private 멤버 선언을 지향해야 한다.


</details>

<details>
<summary>final</summary>
  <p>java에서 사용되는 키워드. 무언가를 제한할 때 사용된다. 변수, 매서드, 클래스에서 사용이 가능하며 각각에 따라 의미가 조금씩 다르다.</p>

* 변수: 값 수정을 제한한다. 따라서 초기화 값이 반드시 필요하다. 클래스의 맴버 변수라면, 생성자 혹은 static 블록을 통한 초기화까지는 허용한다.
* 메서드: override를 제한한다. 상속받은 클래스에서 해당 매서드를 수정해서 사용하지 못하도록 한다.
* 클래스: 상속을 제한한다. 다른 클래스에서 상속하여 재정의하지 못하도록 한다. 


</details>

<details>
<summary>annotation</summary>
  <p>메타 데이터를 가지고 있는 주석</p>
이때 메타 데이터란 애플리케이션이 처리해야 할 데이터가 아니라 컴파일 과정에서 실행 과정에서 코드를 어떻게 처리해야할 지를 알려주기 위한 추가 정보를 의미한다.

자바의 어노테이션은 메타 데이터의 일종이다.

<strong>annotation 종류</strong>

* built-in annotation
  * @Override: 메서드를 오버라이드 하겠다는 의미. 만약 상속받은 클래스 혹은 인터페이스에서 해당 메소드가 없다면 컴파일 오류 발생
  * @Deprecated: 메서드를 Deprecated (더이상 사용하지 않겠다)시킨다. 이 메서드를 사용하는 애플리케이션을 컴파일할 경우, 컴파일 경고를 날린다. 해당 메서드를 사용하지 말라고 경고를 날리고 싶을 때 사용.
  * @SuppressWarnings: 컴파일러 경고를 출력하지 않도록 설정
  * 등등
* meta annotaion (커스텀 어노테이션을 만들 때 사용하는 어노테이션)
  * @Target: 어노테이션 적용 범위
  * @Retention: 언제까지 메타 정보를 유지할지 기간을 설정 [Source, Class, Runtime]
  * @Documented: 자바 문서에도 어노테이션 정보가 들어가도록 함
  
<strong>annotation processor</strong>

컴파일 단계에서 annotation에 정의된 일련의 프로세스(소스코드를 참고하여 새로운 코드를 작성하는 것)를 동작하게 하는 것이다. 컴파일 단계에서 실행되기 때문에, 빌드 단계에서 에러를 출력할 수 있고, 소스코드 및 바이트 코드를 생성할 수 있다.


</details>

