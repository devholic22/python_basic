# python_basic
파이썬 문법 공부 레포지토리 (개인 공부 and prefare for 공개SW, SW프입문)

## 공부 방법
작년에 공부했던 [혼자 공부하는 파이썬] 책을 바탕으로 공부를 진행한다.

## 공부 목적
* 개인적으로 파이썬을 활용한 코딩테스트를 제대로 준비하기 위해 문법을 한 번 다시 정독하는 과정이 필요하다고 생각했다.
* 또한, 공개SW실무와 SW프로그래밍입문 시험 대비도 이 책으로 통일시키는 게 더 효율적일 것 같다는 생각이 들었다.

## 진도
- [x] 파이썬 시작하기
- [x] 자료
- [x] 조건문
- [ ] 반복문
- [ ] 함수
- [ ] 예외 처리
- [ ] 모듈
- [ ] 클래스

## 각 단원마다에서의 중요점
<details>
<summary>파이썬 시작하기</summary>
<div markdown="1">
  <h3>이 책에서 자주 나오는 파이썬 용어들</h3>
  <ul>
    <li>
      <code><b>키워드</b></code>: 특별한 의미가 부여된 단어로, 파이썬이 만들어질 때 이미 사용하겠다고 예약해 놓은 단어
    </li>
    <li>
      <code><b>식별자</b></code>: 프로그래밍 언어에서 이름을 붙일 때 사용하는 단어
      <ul>
        <li>키워드를 사용하면 안 됩니다.</li>
        <li>특수 문자는 언더 바(_)만 허용됩니다.</li>
        <li>숫자로 시작하면 안 됩니다.</li>
        <li>공백을 포함할 수 없습니다.</li>
        <li>캐멀케이스(대문자시작)은 <code><b>클래스</b></code>를 의미, 괄호가 있으면 <code><b>생성자</b></code>를 의미</li>
        <li>스네이크케이스(소문자시작)은 괄호가 있으면 <code><b>함수</b></code>, 없으면 <code><b>변수</b></code>를 의미</li>
      </ul>
    </li>
  </ul>
  <ul>
    <li>파이썬은 <code><b>대소문자를 구분</b></code>합니다.</li>
    <li><code><b>print()</b></code>함수로 여러 개를 출력하면, 공백 한 칸이 추가되면서 여러 개가 출력됩니다.</li>
  </ul>
</div>
  
</details>
<details>
<summary>자료</summary>
<div markdown="1">
  <h3>자료형과 문자열</h3>
  <ul>
    <li><code><b>type()</b></code>: 자료의 형식 확인</li>
    <li><code><b>len()</b></code>: 길이 확인</li>
    <li><code><b>문자열+문자열</b></code>: 공백 없이 바로 문자열이 연결됩니다. 참고로, 문자열과 숫자를 결합할 수는 없습니다.</li>
    <li><code><b>문자*숫자</b></code> 또는 <code><b>숫자*문자</b></code>: 문자열을 숫자만큼 반복합니다.</li>
    <li>
      <code><b>[a:b]</b></code>: 슬라이싱 (특정 범위를 선택합니다. b 직전까지를 선택하며, 원본이 변하지 않습니다.)
      <ul>
        <li>변형1:<code><b>[-3:-1]</b></code>: -1은 뒤에서부터를 의미합니다. 뒤에서부터 2번째, 3번째를 선택한다는 뜻 입니다.</li>
        <li>변형2:<code><b>[1:]</b></code>: 1번째 (2번째) 값부터 끝까지를 선택한다는 뜻 입니다.</li>
        <li>변형3:<code><b>[:3]</b></code>: 0번째, 1번째, 2번째까지를 선택한다는 뜻 입니다.</li>
      </ul>
    </li>
  </ul>
  <ul>
    <li>문자열에서 따옴표를 출력하려면 앞에 \ 문자를 넣으면 됩니다.</li>
    <li>\ 문자를 두 번 넣으면 \ 하나를 의미합니다.</li>
    <li>
      """와 같이 따옴표를 세 번 입력하면 여러 줄 문자열을 입력할 수 있습니다.
      <li>
        """를 입력한 뒤 한 줄씩 내린 다음 문자열을 입력하면 위 아래로 의도치 않은 줄바꿈이 들어갑니다. 이때 따옴표 앞에 \를 붙인다면 없앨 수 있습니다.
      </li>
    </li>
    <li>파이썬은 <code><b>제로 인덱스</b></code>라서 0부터 시작합니다.</li>
  </ul>
  <h3>숫자</h3>
  <ul>
    <li>파이썬의 숫자 타입은 <code><b>int</b></code>와 <code><b>float</b></code>으로 나뉩니다.</li>
  </ul>
  <h3>변수와 입력</h3>
  <ul>
    <li><code><b>input()</code></b>함수로는 입력을 받을 수 있으며, 결과는 무조건 <code><b>문자열</b></code>입니다.</li>
    <li>
      <code><b>int()</b></code> 또는 <code><b>float()</b></code>: 문자열 또는 숫자를 정수, 실수로 변환합니다.
      <ul>
        <li><code><b>int(실수)</b></code>: 소수점 버리고 나머지 숫자로 변환</li>
        <li><code><b>float(정수)</b></code>, <code><b>float(정수문자열)</b></code>: .0을 붙이며 실수로 변환</li>
        <li><code><b>int(실수문자열)</b></code>: ValueError 발생</li>
      </ul>
    </li>
    <li><code><b>str()</b></code>: 문자열로 변환합니다.</li>
  </ul>
  <h3>숫자와 문자열의 다양한 기능</h3>
  <ul>
    <li>
      <code><b>format()</b></code> 함수를 이용하면 자료를 문자열로 변환할 수 있습니다. 또, 특정 양식으로 출력할 수도 있습니다.
      <ul>
        <li>
          <code>"{}".format(10)</code>와 같이 사용할 수 있고, 숫자 이외의 자료형에도 적용할 수 있습니다.
        </li>
        <li>괄호의 갯수가 변수의 갯수보다 많으면 IndexError가 발생하며, 그 반대의 경우는 문제가 없습니다.</li>
        <li><code><b>"{:g}".format(문자열)</b></code>를 활용하면 문자열에서 의미없는 소수점을 제거할 수 있습니다.</li>
      </ul>
    </li>
    <li><code><b>upper()</b></code>와 <code><b>lower()</b></code> 로 알파벳 문자열을 각각 대문자, 소문자로 바꿀 수 있으며 비파괴적입니다.</li>
    <li><code><b>strip()</b></code>을 사용하면 문자열 양옆의 공백을 제거할 수 있습니다.</li>
    <li><code><b>isOO()</b></code>을 사용하면 문자열이 특정 규칙으로만 구성되어 있는지 검사할 수 있습니다.</li>
    <li><code><b>문자열.find(테스트 문자열)</b></code>는 테스트 문자열이 문자열의 몇 번째에서 처음 등장하는지를 확인합니다. 없으면 -1이 나옵니다.</li>
    <li><code><b>테스트 문자열 in 문자열</b></code>의 in을 활용하면 테스트 문자열이 문자열 안에 있는지 확인할 수 있습니다.</li>
    <li><code><b>split()</b></code>메서드로 문자열을 특정 문자를 기준으로 나눌 수 있습니다. 리스트가 반환됩니다.</li>
  </ul>
</div>
</details>
<details>
<summary>조건문</summary>
<div markdown="1">
  <h3>불 자료형과 if 조건문</h3>
  <ul>
    <li><code>if (9 <= x <= 12):</code>와 같이 작성하면 연속적으로 조건을 검사할 수 있습니다.</li>
  </ul>
  <h3>if-else와 elif 구문</h3>
  <ul>
    <li><code>if-elif-else</code>를 사용할 때 else가 꼭 필요한 것은 아닙니다.</li>
    <li>None, 0, 0.0, 빈 컨테이너는 모두 False로 변환되고, 나머지 경우는 True로 변환됩니다.</li>
    <li><code>pass</code> 키워드를 사용하면 특정 조건에서 아무것도 안 함을 표시할 수 있습니다.</li>
  </ul>
</div>
</details>
<details>
<summary>반복문</summary>
<div markdown="1">
</div>
</details>
<details>
<summary>함수</summary>
<div markdown="1">
</div>
</details>
<details>
<summary>예외 처리</summary>
<div markdown="1">
</div>
</details>
<details>
<summary>모듈</summary>
<div markdown="1">
</div>
</details>
<details>
<summary>클래스</summary>
<div markdown="1">
</div>
</details>
