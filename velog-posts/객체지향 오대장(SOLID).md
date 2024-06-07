<p><img alt="" src="https://velog.velcdn.com/images/kimyongwook98/post/594eb347-8a04-4d21-9931-4aad4e867669/image.png" /></p>
<p>오늘의 주제는 객체지향 프로그래밍을 하면서 반드시 지켜야 하는 5가지 원칙인 솔리드 원칙이다. <br />
솔리드 원칙을 통해 코드를 확장하고 유지 보수 관리하기가 더 쉬워지며, 불필요한 복잡성을 제거해 리팩토링에 유리해져 프로젝트 개발 생산성을 높일 수 있다.
<br /><br /><br /></p>
<h3 id="1-srpsingle-responsibility-principle--단일-책임-원칙">1. SRP(Single Responsibility Principle) : 단일 책임 원칙</h3>
<p>하나의 클래스는 하나의 기능을 담당하여 하나의 책임을 수행하는데 집중되도록 클래스를 따로따로 여러 개 설계하라는 원칙이다. <br />
한 객체가 여러 기능을 담당한다면, 수정시 코드가 복잡해질 수 있다.
<img alt="" src="https://velog.velcdn.com/images/kimyongwook98/post/b1d62dc6-561c-4c3a-bca7-23fbef4aa946/image.png" />
이해를 돕기 위한 사진이다. <br />
이처럼 한 클래스가 요리사, 정원사, 운전병을 모두 담당할 수 없다.
단일 책임 원칙을 통해 코드의 <strong>유지보수성을 높일</strong> 수 있다..!</p>
<p><br /><br /><br /></p>
<h3 id="2-ocpopen-closed-priciple--개방-폐쇄-원칙">2. OCP(Open Closed Priciple) : 개방 폐쇄 원칙</h3>
<p>확장에 열려있어야 하며, 수정에는 닫혀있어야 한다는 원칙이다. <br /></p>
<blockquote>
<p><strong>확장에 열려있다</strong> - 요구 반영시 유연하게 코드를 추가해 기능을 확장한다.
<strong>수정에 닫혀있다</strong> - 기존 코드를 수정 없이 기능을 추가 또는 변경할 수 있다. <br /></p>
</blockquote>
<p>기능 추가시 클래스 확장을 통해 유연하게 구현하면서, 확장에 따른 클래스 수정은 최소화한다는 것인데.. <br />
그 이유는 ..! <br />
새 변경사항이 있을 때, 객체를 직접적으로 수정해야 한다면, 유지 보수 비용 증가로 이어지고, 이는 안 좋은 설계방식이기 때문이다!
<img alt="" src="https://velog.velcdn.com/images/kimyongwook98/post/a1f2edc5-4917-4a38-aacf-eeabc3e0c290/image.png" />
이해를 돕기 위한 사진이다. <br />
결국 개방 폐쇄 원칙은 <strong>추상화 사용을 통한 관계 구축을 권장</strong>하고, 다형성과 확장을 가능하게 하는 <strong>객체지향의 장점을 극대화</strong>하는 원칙이다..!
<br /><br /><br /></p>
<h3 id="3-lsplistov-substitution-priciple--리스코프-치환-원칙">3. LSP(Listov Substitution Priciple) : 리스코프 치환 원칙</h3>
<p>자식타입 객체는 언제든 부모타입 객체로 대체할 수 있다는 원칙이다. 
이는 일관성을 유지하여 부모자식 클래스를 오류 없이  사용할 수 있도록 한다.
<img alt="" src="https://velog.velcdn.com/images/kimyongwook98/post/ba1e5e04-ab75-4f16-b2a7-900cabb32910/image.png" />
이해를 돕기 위한 사진이다. <br />
리스코프 치환 원칙은 <strong>다형성 특징을 이용</strong>하기 위한 원칙임을 알 수 있다..!
<br /><br /><br /></p>
<h3 id="4-ispinterface-segregation-principle--인터페이스-분리-원칙">4. ISP(Interface Segregation Principle) : 인터페이스 분리 원칙</h3>
<p>각각의 인터페이스를 쓰임새에 맞게 분리해야한다는 원칙이다.
인터페이스의 단일 책임 원칙이라고 할 수 있다. <br />
이를 통해 클라이언트의 목적과 용도에 적합한 인터페이스 만을 제공
하여 불필요한 간섭을 최소화하는 것이 목적이다..! <br />
지나치게 역할이 많은 인터페이스는 결합도를 낮추기 때문이다.</p>
<blockquote>
<p>자고로 결합도는 낮고.. 응집도는 높아야.. 한다.. </p>
</blockquote>
<p><br /><img alt="" src="https://velog.velcdn.com/images/kimyongwook98/post/9fe13476-15ed-4762-835a-416b97f54fa1/image.png" />
이해를 돕기 위한 사진이다.<br />
로봇이 안테나가 없는 상황에서, 이를 수정할 때 wiggle 안테나와 <strong>관련이 없는</strong> arms와 spin <strong>클래스까지 영향을 끼칠 수 있다</strong>..!
킹치만 오른쪽 그림과 같이 분리하면 모든 클래스는 <strong>자신이 이용하지 않는 기능의 변화에 영향을 받지 않게</strong> 된다..!
<br /><br /><br /></p>
<h3 id="5-dipdependency-inversion-principle--의존-역전-원칙">5. DIP(Dependency Inversion Principle) : 의존 역전 원칙</h3>
<p>고수준 클래스는 저수준 클래스의 구현에 의존해서는 안되며, 저수준 모듈이 고수준 모듈에서 정의한 추상 타입에 의존해야 한다는 원칙이다.</p>
<blockquote>
<p><strong>고수준 클래스</strong> - 변하지 않는 것 (인터페이스, 추상 클래스) 
<strong>저수준 클래스</strong> - 자주 변하는 것 (메인 클래스, 객체) </p>
</blockquote>
<ul>
<li>구현 클래스에 의존하지 말고, 인터페이스에 의존하라는 뜻이다.</li>
<li>의존 역전 원칙이 위배되면 개방 폐쇄 원칙 역시 위배될 가능성이 높다.</li>
<li>의존 역전 원칙에서 의존성이 역전되는 시점은 컴파일 시점이다.</li>
</ul>
<p><img alt="" src="https://velog.velcdn.com/images/kimyongwook98/post/7445c909-aadc-4423-89e4-a69f254283b8/image.png" />
이해를 돕기 위한 사진이다. <br /></p>
<p>의존 역전 원칙은 결국 비즈니스와 관련된 부분이 세부 사항에는 의존하지 않는 설계 원칙이고, 이를 통해 인터페이스 <strong>변경에 따른 코드 수정을 최소화</strong>하고 <strong>확장에는 유연하게 대처</strong>할 수 있다..!</p>
<blockquote>
<p>결 합 도 를 낮 추는 원 칙 이 다 !</p>
</blockquote>
<p><br /><br /><br /></p>
<h3 id="정리">정리</h3>
<p><img alt="" src="https://velog.velcdn.com/images/kimyongwook98/post/29f1914c-0f12-427f-9648-c1a4a8f167a2/image.png" />
<strong>SOLID는 추상화와 다향성을 강조해서 유지보수 및 확장에 용이한 애플리케이션 제작을 중요시한다.</strong></p>