<h1 id="-">데이지 엔진</h1>
<p>Wave Engine(C#) 기반 멀티플랫폼 비주얼 노벨 엔진.</p>
<h2 id="-">데이직 언어</h2>
<p>데이지의 &#39;데&#39;와 베이직의 &#39;이직&#39;을 합성해 만든 이름.<br>비구조적언어로써 Lua스크립트의 함수를 호출할 수 있다.</p>
<p>솔직히 말해서 네코노벨 스크립트에서 따온 것이 많다.</p>
<h3 id="-">명령어</h3>
<p>명령어에 띄어쓰기를 쓰면 <strong>알아서</strong> 무시된다.<br>(명령어와 인수와 구분은 띄어쓰기로 구분되는데 파서에서는 명령어가 &#39;명령어+공백문자&#39; 로 인식 되기 때문에 별 문제가 없다.)<br>변수 이름에는 가능하면 띄어쓰기를 쓰지 않도록 하고<br>만약 사용할 경우&#39;<strong>변수 맛난호빵 = 참</strong>&#39;, &#39;<strong>변수 맛난 호빵 = 참</strong>&#39;, &#39;<strong>변수 맛난호빵=참</strong>&#39;은 같은 것으로 취급된다.<br>(아직 파서 제네레이터의 특성이나 트릭을 잘 모르겠지만 스페이스바가 단어를 구분하는데 이용될 수 있기 때문에 가급적 띄어쓰기는 필요한 곳에만 쓰도록 한다.)</p>
<h3 id="-">함수</h3>
<p>스크립트상에서 바로 쓰이지 않고 식에서 사용된다.<br>인수들을 전달받아 반환 값을 내뱉는다.</p>
<h3 id="-">사용자 정의</h3>
<p>데이직에서는 명령어와 함수를 사용자가 직접 구현할 수 있다.</p>
<h3 id="-">변수 형식</h3>
<p>데이직의 변수는 전적으로 C#의 dynamic형식에 좌우된다.<br>여기서는 보통 어떤 경우에 판정하는지 서술한다.</p>
<ul>
<li>정수<br>변수 파이 = 314</li>
<li>실수<br>변수 파이 = 3.14</li>
<li>문자열<br>변수 파이 = &quot;3.14&quot;</li>
<li>부울<br>변수 파이 = 참<br>변수 파이 = 거짓</li>
</ul>
<h3 id="-">예제</h3>
<p>이미지 테스트, &quot;Image\Test&quot;<br>대사 &quot;호빵&quot;, &quot;안뇽&quot;<br>대기<br>대사 &quot;전설에 의하면 호빵은 매우 맛있다고 한다.\n&quot;<br>대기<br>대사 &quot;그러나 사람들은 그냥 맛있는 줄로만 알고 있다.&quot;, 참<br>대기</p>
<h2 id="-">구성 파일</h2>
<h3 id="-wpk">리소스 - *.wpk</h3>
<p>Wave Engine의 한계사항으로 png나 mp3같은 파일들을 직접 불러오지 못해 사용되는 포맷.<br>다만 Wave Engine Asset Exporter의 UI가 그리 어려운편은 아니기 때문에 이쪽을 사용하는 것을 유도할 계획.</p>
<h3 id="-header-json">헤더 - Header.json</h3>
<p>게임 배포에 필요한 옵션들을 담고 있는 파일이다.<br>json문법으로 작성되고, 배포시 바이너리 데이터로 변환된다.</p>
<h4 id="-">입력 사항</h4>
<ul>
<li>대사창<br>대사란이 띄워지는 위치, 영역을 지정한다.</li>
</ul>
<h2 id="-">저작권 방침</h2>
<p>공개 작품 제작시 제보해야하며<br>비영리적 작품은 의무적으로 시행할 필요는 없고,<br>영리적 작품은 <strong>의무 불이행</strong>시 법적인 조치를 취할 수 있다.</p>
