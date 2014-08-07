# 데이지 엔진
Wave Engine(C#) 기반 멀티플랫폼 비주얼 노벨 엔진.

## 데이직 언어
데이지의 '데'와 베이직의 '이직'을 합성해 만든 이름.
비구조적언어로써 Lua스크립트의 함수를 호출할 수 있다.

솔직히 말해서 네코노벨 스크립트에서 따온 것이 많다.

### 명령어

명령어에 띄어쓰기를 쓰면 **알아서** 무시된다.<br>
(명령어와 인수와 구분은 띄어쓰기로 구분되는데 파서에서는 명령어가 '명령어+공백문자' 로 인식 되기 때문에 별 문제가 없다.)<br>
변수 이름에는 가능하면 띄어쓰기를 쓰지 않도록 하고<br>
만약 사용할 경우'**변수 맛난호빵 = 참**', '**변수 맛난 호빵 = 참**', '**변수 맛난호빵=참**'은 같은 것으로 취급된다.

#### 텍스트

- **텍스트 [텍스트(문자열)], [X(정수)], [Y(정수)]**<br>
텍스트를 원하는 위치에 띄운다.
- **텍스트 [텍스트(문자열)], [X(정수)], [Y(정수)], [크기(정수)]**<br>
텍스트를 원하는 크기와 위치에 띄운다.
- **대사 [텍스트(문자열)]**<br>
대사를 띄운다.
- **대사 [텍스트(문자열)], [대사 잇기(부울)]**<br>
'대사 잇기'인수가 참이면 이어서 띄운다.
- **대사 [이름(문자열)], [텍스트(문자열)]**<br>
이름과 대사를 띄운다.<br>

#### 그래픽

- **그래픽 [그래픽 이름], [이미지 이름], [X(정수)], [Y(정수)], [알파값(정수)=255], [배율(실수)=1.0]**<br>
이미지를 원하는 크기와 위치에 띄운다.
- **그래픽 [그래픽 이름], [X(정수)], [Y(정수)], [알파값(정수)=0], [배율(실수)=1.0]**<br>
이미지를의 상태를 변경한다.
- **버튼 [버튼 이름], [이미지 이름], [X(정수)], [Y(정수)], [알파값(정수)=255], [배율(실수)=1.0]**<br>
버튼을 원하는 크기와 위치에 띄운다.<br>
버튼 클릭시 다음줄의 명령을 실행하며 보통은 그 줄의 다음 줄을 실행한다.
- **버튼 [버튼 이름], [X(정수)], [Y(정수)], [알파값(정수)=255], [배율(실수)=1.0]**<br>
버튼의 상태를 변경한다.
- **그래픽제거 [그래픽 이름]**<br>
이미지를 제거한다.
- **버튼제거 [버튼 이름]**<br>
버튼을 제거한다.

#### 변수

- **변수 [변수 이름][식]**<br>
변수를 정의하거나 데이터를 집어 넣는다.<br>
식에 '무효'를 대입하면 메모리 상에서 데이터가 지워진다.<br>
형식은 C# dynamic형식.
- **이미지 [이미지 이름], [경로(문자열)]**<br>
이미지를 불러와 메모리에 저장한다.
- **효과음 [텍스쳐 이름], [경로(문자열)]**<br>
효과음을 불러와 메모리에 저장한다.
- **음악 [텍스쳐 이름], [경로(문자열)]**<br>
음악을 불러와 메모리에 저장한다.

#### 진행

- **대기**
스크립트 진행을 잠시 멈춘다.<br>
키보드 엔터, 마우스 클릭을 하면 넘김 처리된다.
- **라벨 [라벨 이름]**
라벨을 선언한다.
- **이동 [라벨 이름]**
라벨 이름이 마지막으로 선언된 곳으로 이동한다.
- **함수 [인수 타입1], [인수 타입2], [인수 타입3]...**
이 파일이 함수임을 선언한다.

#### 프로퍼티

데이직에서는 중앙시스템에 큰 관련이 있는 변수는 프로퍼티라고 부르며, @로 변수와 구분된다.<br>
사용상 주의를 요하는 프로퍼티는 $로 구분된다.

- **@스킵(부울)**<br>
이 값이 참이면 '대기'명령을 무시한다.<br>
기본값 = 거짓
- **@대사창보여짐(부울)**
'대사창보이기' 함수가 실행됬으면 참이고<br>
'대사창숨기기' 함수가 실행됬으면 거짓이다.

### 함수

사용법은 명령어와 똑같으며 사용자 커스터마이징을 위해 분리시켜놨다고 보면된다.

#### 미리 구현된 함수

- **대사창보이기**
대사창을 보이게한다.
- **대사창숨기기**
대사창을 숨긴다.

#### 함수 구현 방법


### 예제

이미지 테스트, "Image\Test"<br>
대사 "호빵", "안뇽"<br>
대기<br>
대사 "전설에 의하면 호빵은 매우 맛있다고 한다.\n"<br>
대기
대사 "그러나 사람들은 그냥 맛있는 줄로만 알고 있다.", 참<br>
대기

### 변수 형식

데이직의 변수는 전적으로 C#의 dynamic형식에 좌우된다.
여기서는 어떤 경우에 판정하는지 서술한다.

- 정수<br>
변수 파이 = 314
- 실수<br>
변수 파이 = 3.14
- 문자열<br>
변수 파이 = "3.14"
- 부울<br>
변수 파이 = 참<br>
변수 파이 = 거짓

## 구성 파일

### 리소스 - *.wpk

Wave Engine의 한계사항으로 파일들을 직접 불러오지 못해 사용되는 포맷.
다만 Wave Engine Asset Exporter의 UI가 그리 어려운편은 아니기 때문에 이쪽을 사용하는 것을 유도할 계획.

### 헤더 - Header.json

게임 배포에 필요한 옵션들을 담고 있는 파일이다.
json문법으로 작성되고, 배포후 바이너리 데이터로 변환된다.

#### 입력 사항
- 대사창<br>
대사란이 띄워지는 위치, 영역을 지정한다.

## 저작권 방침
비영리적 이용은 자유로우나
영리적 이용시 게임제목과 게임 소개를 알려야함.
판매되는 게임을 확인하기 위함임.
