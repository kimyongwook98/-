<p>최근 면접에서 직무테스트를 보다 JVM에 관한 문제가 나왔는데, 제대로 풀지를 못해서 복습 겸 JDK, JRE 그리고 JVM에 대해 공부해봐야겠다.. <br /><img alt="" src="https://velog.velcdn.com/images/kimyongwook98/post/3688e27a-67a6-4c2a-94fa-68b73600fd2b/image.png" /> <br /><br /><br /><br />
한 장 요약
<img alt="" src="https://velog.velcdn.com/images/kimyongwook98/post/a885073e-caa4-46f0-942b-a3c150c276bf/image.png" /> <br /></p>
<h3 id="1-자바-가상-머신-jvm-java-virtual-machine">1. 자바 가상 머신 (JVM, Java Virtual Machine)</h3>
<ul>
<li>자바 프로그램이 <strong>어느 플랫폼, 어느 운영체제 상에서도 실행</strong>될 수 있게 만들어 줌 -&gt; WORA</li>
<li>자바 소스코드로부터 만들어지는 자바 바이너리 파일(.class)을 실행할 수 있음</li>
<li>인터프리터와 JIT 컴파일러를 통해 바이트 코드를 각 운영체제에 맞는 기계어로 해석시켜 실행</li>
<li>가비지 콜렉터를 통해 어플리케이션의 동적 메모리를 관리 <br /><br /><br /><br /><h3 id="2-자바-런타임-환경-jre-java-runtime-environment">2. 자바 런타임 환경 (JRE, Java Runtime Environment)</h3>
</li>
<li>JRE는 JVM의 실행환경을 구현 </li>
<li>자바 클래스 라이브러리(Java class libraries), 자바 가상 머신(JVM) 그리고 자바 클래스 로더(Java class loader)를 포함</li>
<li>클래스 로더, 클래스 라이브러리를 통해 작성한 자바 코드를 라이브러리와 결합한 후 JVM에 넘겨 실행 <br /><br /><br /><br /><h3 id="3-자바-개발-키트-jdk-java-development-kit">3. 자바 개발 키트 (JDK, Java Development Kit)</h3>
</li>
<li>일반적으로 자바를 실행하기 위해 설치하는 것이 JDK</li>
<li>JDK를 설치하면 JRE가 자동으로 설치 </li>
<li>JDK는 JRE를 포함하고 있고, JRE는 JVM을 포함</li>
<li>JDK에는 JRE에는 없는 &quot;자바 컴파일러(javac, java compiler)&quot;를 포함</li>
<li>컴파일러란 우리가 작성한 자바 문법을 컴퓨터가 이해할 수 있게 바꿔주는 해석기</li>
<li>실제로 .java 파일을 만들어서 실행(빌드)하면 컴파일 작업을 거쳐 .class 라는 파일이 자동으로 생성 <br /><br /><br /><br /><h4 id="자바-프로그램-실행-과정">자바 프로그램 실행 과정</h4>
<img alt="" src="https://velog.velcdn.com/images/kimyongwook98/post/fe1e14d6-3e8f-4f9e-81e9-2ed360514380/image.PNG" /></li>
<li>소스코드(MyPrograme.java) 작성</li>
<li>Compiler는 자바 소스코드를 이용하여 클래스 파(MyProgram.class)생성, 컴파일 된 클래스 파일은 JVM(Java Virtual Machine)이 인식할 수 있는 바이트 코드 파일</li>
<li>JVM은 클래스 파일의 바이트 코드를 해석하여 바이너리 코드로 변환하고 프로그램을 수행</li>
<li>MyProgram 수행 결과가 컴퓨터에 반영</li>
</ul>