# prepare_frontend_interview

## HTML/ CSS

<b>프론트엔드 기술 면접을 위한 핸드북 만들기</b>

## HTML 목차

- [DOCTYPE 🔥](#DOCTYPE)

  - DOCTYPE에 대하여 설명하시오
    - HTML이 어떤 버전으로 작성되었는지 미리 선언하여, 문서 형식을 정의해주는 것입니다.
  - meta 태그에 대해서 알고 있나요?
    - HTML 문서가 어떤 내용을 담고 있고, 키워드는 무엇이며, 누가 만들었는지에 대한 정보를 담고있는 태그입니다.
  - meta 태그의 요소에 대해서 아는대로 말해보세요
    - title : HTML 문서 전체의 타이틀을 표현하기 위한 메타데이터
    - charset : 인코딩 방식 특정
    - name, content : 메타 요소가 어떤 정보와 내용을 갖고 있는지 알려줍니다. SEO를 위해 적용함.
  - 검색 엔진 최적화를 위해 활용해본 메타 태그가 있나요?
    1. 검색 엔진을 위한 키워드를 정의
       ```html
       <meta name="keyword" content="HTML, meta, tag, element, reference" />
       ```
    2. 웹 페이지에 대한 설명을 정의
       ```html
       <meta name="description" content="HTML meta tag page" />
       ```
    3. 문서의 저자(author)를 정의
       ```html
       <meta name="author" content="TCPSchool" />
       ```
    4. 5초 뒤에 다른 페이지로 리다이렉트(redirect)시키기
       ```html
       <meta http-equiv="refresh" content="5;url=http://www.tcpschool.com" />
       ```
    5. 모든 장치에서 웹 사이트가 잘 보이도록 뷰포트(viewport)를 설정
       ```html
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       ```

- [웹 표준 및 웹 접근성 🔥](#웹-표준-및-웹-접근성)

  - 웹 표준이란?
    - 웹 사이트를 어떠한 운영체제나 브라우저에서 보더라도 동일하게 보여지도록 W3C(World Wide Web Consorium) 기구 표준에 맞추는 것입니다.
  - 웹 접근성이란?
    - 장애인과 비장애인, 노인 등이 웹사이트를 자유롭게 이용할 수 있게하는 권리를 말합니다. 스크린 리더기를 이용하는 것이 대표적인 예시입니다.
  - 웹 접근성에 맞는 마크업 예시 몇가지 말해보시오

    1. img 태그의 alt태그는 빠짐없이 입력해야 합니다.
    2. 배경 이미지일 경우 img 태그의 alt태그는 빈값으로 넣어서 스크린리더에 읽히지 않게 해야합니다.
    3. 동영상은 대본이나 자막을 제공하고 자동재생은 금지합니다.
    4. input 태그에는 적절한 label이 제공되어야 합니다.
    5. qr코드나 바코드와 같은 이미지 정보는 대체 텍스트로 연결링크를 제공해야 합니다.
    6. 버튼의 기능을 명확히 이해할 수 있는 대체 텍스트를 제공해야 합니다.
       ```html
       <input type="image" src="next.gif" alt="메뉴 더보기" />)
       ```

  - 시멘틱 태그란 무엇인가 왜 사용하는가
    - 서로 관계가 있는 정보를 파악하고, 콘텐츠가 어떤 맥락 안에 있는지 알기 쉽게 해줍니다. 또한 검색 엔진을 통해 검색이 잘 될 수 있도록 도와줍니다.
  - 텍스트 관련 태그
    - 줄바꿈이 일어나는 태그
      - `<h1>` ~ `<h6>` : 제목 표시
      - `<hr>` : 수평줄
      - `<pre>` : 표시한 공백이 그대로 표시된다.
      - `<blockquote>` : 태그 안쪽 테스트가 인용문임을 알리는 태그
    - 줄바꿈이 일어나지 않는 태그
      - `<strong>` : 글자 굵게 표시(중요한 내용임을 의미)
      - `<b>` : 글자 굵게 표시(중요한 내용임을 의미X)
      - `<em>` : 강조하고자 하는 내용임을 의미하며, 글자 기울여 표시
      - `<i>` : 강조하고자 하는 내용임을 의미X, 글자 기울여 표시
      - `<q>` : 내용 앞뒤에 따옴표 표시
      - `<mark>` : 형광펜 표시
  - SEO란 무엇인가?
    - 검색 엔진 최적화(SEO : Search Engine Optimization)는 검색 엔진이 웹 페이지의 자료를 수집하거나 순위를 방식에 맞게 웹 페이지를 구성하여, 검색 결과의 상위에 나올 수 있게 하는 행위를 말합니다.
  - Button 태그의 Default type은 무엇인가?
    - `sumbit`입니다. form 태그 안에 form data와 관련 없는 버튼을 만든 후, 그 버튼을 누르면 전송되는 경우가 발생할 수 있으니 버튼 태그의 type은 꼭 명시하는 것이 좋습니다.
    - `submit` : 폼을 제출하는 이벤트 발생시킴
    - `reset` : 폼 안에 작성된 내용을 초기화시킴
    - `button` : 아무런 이벤트 없음. click 이벤트와 연결시켜서 자바스크립트를 활용하는 방법을 많이 사용함
  - Section 태그와 article 태그의 차이점
    - `article`태그는 `section`과 다르게 독립적으로 존재할 수 있으며, 재사용할 수 있습니다. 즉 `article`이 좀 더 구체적입니다. `section`은 주제별로 구분한 그룹입니다. 논리적으로 관계 있는 요소 또는 문서를 분리할 때 사용합니다.

- [그 외 🔥](#그-외)

  - 이미지 크기가 클 경우 렌더링 속도가 느려질텐데 이를 개선하기 위한 방법
    1. 이미지의 용량을 줄인다.
    2. 이미지 스프라이트를 활용한다.
    3. 벡터 이미지(svg)를 활용한다.
    - svg에 대해 설명해주세요.
      - 확장가능한 벡터 그래픽을 말합니다. 픽셀을 이용하는 png, jpg 등과 다르게 벡터를 기반으로 이미지를 표현합니다. 크기를 조절해도 깨지는 것이 없고, 상대적으로 용량이 작습니다.
  - UI란 무엇인지 설명하시오
    - 유저 인터페이스를 말하며, 다양한 사용자가 사용할 수 있도록 보편성을 지녀야합니다.
  - 왜 일반적으로 CSS `<link>`를 head 태그 사이에 위치시키고, JS `<script>` 태그를 body 직전에 위치시키는 것이 좋은 방법인지 설명하시오
    - `<head>` 안에 `<link>`를 넣는 이유
      - 파싱 과정에서 DOM tree(HTML의 태그)가 생성되어도, CSSOM Tree(CSS 파일)가 없으면 렌더링이 되지 않아 빈 화면이 뜨게 됩니다. 따라서 빠르게 CSSOM Tree를 읽어와 렌더링을 하기 위해 `<head>` 안에 CSS 파일을 넣어야합니다.
    - `<script>`를 `<body>` 직전에 위치시키는 이유
      - 파싱 과정에서 `<head>` 안에서 `<script>`를 만나게 되면 파싱을 멈추고, Script 파일을 읽습니다. Script 파일을 읽는 동안 렌더링에 방해가 되어 무거운 스크립트가 실행될 때는 사용자 입장에서 웹페이지가 느리게 보이기 때문에, `<script>`를 `<body>` 직전에 위치시키는 것이 베스트입니다.
        > `<script>`를 `<head>`에 넣어야 하는 경우엔 defer를 사용하자.
  - `data-속성` 은 무엇에 좋은지 설명하시오
    - 데이터 속성의 장점은 예전처럼 hidden으로 태그를 숨겨두고 데이터를 저장할 필요가 없어졌다는 점 입니다. 따라서 데이터 속성을 쓰면, 훨씬 HTML 스크립트가 간결해집니다.
    ```html
    <!-- 이전 코드 -->
    <input type="hidden" name="country" value="Korea" />
    <!-- 데이터 속성 -->
    <input type="text" data-country="Korea" data-code="c03" name="country" />
    ```

- [SVG란?🔥](#SVG란)

  - SVG 장점과 단점
    - 장점
      - 벡터 기반 이미지이므로 사이즈를 조절해도 깨지지 않습니다.
      - 웹 사이트 로딩 속도가 빠릅니다.
      - SEO 친화적입니다. svg는 xml코드이기 때문에 키워드, 설명, 링크 등이 포함될 수 있습니다.
    - 단점
      - 너무 복잡한 svg는 비효율적일 수 있습니다. 많은 모양, 색상 등을 포함하여서 파일크기가 jpg나 png 보다 커지는 경우가 종종 있습니다.
  - SVG 내부 도형에 대해 아는게 있나요?
    - `<rect>` : 사각형
    - `<circle>` : 원
    - `<polyline>` : 연결된 직선들의 그룹

## CSS 목차

- [display 🔥](#display)

  - block 이란?
    - 항상 새로운 라인에 요소가 시작되고, 기본적으로 전체 화면의 가로 폭만큼 width를 차지합니다. width값을 부여해주면 그 너비만큼 영역을 차지합니다.
  - inline 이란?
    - 새로운 라인에 시작되지 않으며, 다른 요소들과 같은 줄에 배치될 수 있고 content 너비만큼의 영역을 차지합니다. width, height, margin-top, margin-bottom 속성이 적용되지 않습니다.
  - inline-block 이란?
    - block과 inline 요소의 특징을 모두 가지고 있습니다. 한 줄에 inline 요소들과 같이 배치될 수 있으며, width와 height 속성으로 영역의 크기를 지정할 수 있습니다.
  - none 이란?
    - 아예 사라지게 합니다. 보이지도 않고 해당 공간도 존재하지 않게 됩니다.
    - `display: none`과 `visibility: hidden`의 차이점
      - `visibility: hidden`은 보이지만 않고 해당 공간을 존재합니다. width와 height값을 주었다면 그 공간만큼 존재하게 됩니다.

- [position 속성에 대하여 🔥](#position-속성에-대하여)

  - static
    - 기본값으로 요소들이 겹치지 않고 상->하로 배치됩니다.
  - relative
    - 원래 배치되어야 할 위치에서 지정한 값만큼 떨어진 곳에 요소를 배치합니다.
  - fixed
    - 웹 브라우저 화면 전체를 기준으로 배치합니다. 스크롤을 하더라도 위치가 고정됩니다.
  - absolute
    - 가장 가까운 상위 요소의 위치를 기준으로 지정한 값만큼 떨어진 곳에 요소를 배치합니다.
  - sticky
    - 스크롤 위치가 임계점에 이르면 fixed와 같이 박스를 화면에 고정할 수 있는 속성으로 스크롤 영역 기준으로 배치합니다.

- [float가 어떻게 작동하는가🔥](#float가-어떻게-작동하는가)

  - float는 주변의 다른 요소들과 자연스럽게 어울리도록 만들어줍니다. 컨테이너 요소에 float가 적용되면 그 이후에 등장하는 모든 요소들은 정확한 위치를 설정하기 힘들어지기 때문에 `clear` 속성을 사용하여 float 속성에 영향 받지 않도록 설정합니다.

- [Flexbox나 Grid 각각의 특징🔥](#Flexbox나-Grid-각각의-특징)

  - flex를 사용하는 이유가 무엇인가요?
    - float는 내가 원하는 위치에 위치시키기 어렵다는 단점이 있습니다(left, right 속성밖에 없음). 또한 clear 속성을 병행해야하는 불편함도 있기 때문에 flex를 사용하는 추세입니다.
  - Grid를 사용하는 이유가 무엇인가요?
    - grid를 사용하면 list에 간격과 width 비율만 입력해주면 쉽고 간편히 만들 수 있습니다. 또한 브라우저 창을 줄이면 자동으로 width에 퍼센트를 준 것처럼 반응합니다.

- [이미지 태그를 스타일로 대체하는 법 🔥](#이미지-태그를-스타일로-대체하는-법)
  - background-image로 대체합니다.
- [반응형 웹의 3요소 🔥](#반응형-웹의-3요소)
  1. 그리드 레이아웃 : 부모요소에 `display: grid`를 넣어준다.
  2. 가변형 이미지 : max-width, width, min-width 등을 이용해 화면 너비에 따라 높이와 너비가 바뀌는 이미지
  3. 미디어 쿼리 : 컨텐츠의 변경없이 주로 화면의 크기에 따라 스타일 시트를 달리하여 적절한 모양을 보여줄 수 있습니다.
- [CSS selector가 어떠한 원리로 동작하나요? 🔥](#CSS-selector가-어떠한-원리로-동작하나요?)
  - 선택자는 크게 4가지가 있습니다. id, class, tag 그리고 \*(universal). 스타일 엔진은 키 셀렉터로부터 시작하여 왼쪽으로 이동하면서 엘리먼트가 규칙에 적합한지 확인합니다. 만약 엘리먼트가 이 규칙에 적합하거나 적합하지 않다는 게 확인되면 멈춥니다.
- [반응형웹과 적응형웹에 설명하시오 🔥](#반응형웹과-적응형웹에-설명하시오)

  - 반응형 웹이란?
    - 하나의 웹사이트에서 접속하는 디스플레이의 종류에 따라 화면의 크기가 자동으로 변하도록 만든 웹페이지 접근 기법을 말합니다.
  - 적응형 웹이란?
    - 반응형 웹의 반대 개념이며, 사용자의 기기 정보를 미리 받아서 조건에 맞는 화면을 보여주는 것입니다.

- [PX, EM에 대해 설명하시오 🔥](#PX,-EM에-대해-설명하시오)

  - px은 고정된 절대값의 단위이며, em과 rem은 환경에 따라 변하는 단위입니다. em은 같은 엘리먼트에서 지정된 font-size 기준으로 px로 바뀝니다. rem은 최상위 엘리먼트에서 지정된 font-size값을 기준으로 변환됩니다.

- [CSS 적용 우선순위 🔥](#CSS-적용-우선순위)

  - 기본적으로 나중에 선언된 css가 우선순위가 높습니다.
  - !important > inline style attribute > id > class, 다른 attribute, 수도클래스(:first-child같은 것) > tag element, 수도엘레먼트(::before같은 것) 순으로 우선순위가 높습니다.
  - 우선순위가 같다면 개수가 많은 css가 우선순위가 높습니다.

- [CSS-in-JS에 대해서 설명해 주세요 🔥](#CSS-in-JS에-대해서-설명해-주세요)

  - 대표적인 라이브러리로 styled-components와 Emotion이 있습니다. 자바스크립트를 사용하여 css를 작성할 수 있으며, 컴포넌트 단위로 추상화되기 때문에 css 파일(모듈)간의 의존성을 신경 쓰지 않아도 된다는 장점이 있습니다. 제가 실제로 느꼈던 장점으로는 특정 스타일을 가진 태그의 네임을 커스터마이징 함으로써 가독성이 좋아진다는 장점이 있었습니다. 단점으로는 번들 크기가 증가한다는 점이 있습니다.

- [CSS 전처리기를 사용해보셨나요? 🔥](#CSS-전처리기를-사용해보셨나요)

  - 사용해봤다면 장점과 단점
    - CSS 전처리기를 사용하게 되면 selector를 중첩으로 관리할 수 있고, 조건문이나 반복문, 간단한 연산 등을 할 수 있어서 css를 프로그래밍하듯이 코딩할 수 있다는 장점이 있습니다. 단점은 웹에서는 css만 동작하기 때문에 컴파일을 거쳐야합니다.

- [padding과 margin의 차이가 무엇인가요? 🔥](#padding과-margin의-차이가-무엇인가요)
  - padding에 대하여
    - 내부 여백
  - margin에 대하여
    - 외부 여백

## 내가 뽑은 핵심 질문

1. 시맨틱 태그에 대해 설명해주세요.
   - 의미론적인 마크업을 말합니다. 시맨틱 태그를 사용하면 검색 엔진은 페이지의 검색 랭킹에 영향을 줄 수 있는 중요한 키워드로 간주합니다. 또한 가독성이 높아지는 이점이 있습니다.
2. SEO가 뭔가요?
   - SEO(검색 엔진 최적화)는 웹사이트가 검색 결과에 더 잘 보이도록 최적화하는 과정입니다. 검색 랭크 개선이라고도 합니다.
   - SEO는 어떤 원리로 작동되는지 아나요?(예상 꼬리 질문)
     - 검색 엔진은 웹을 크롤링하여 가져온 콘텐츠를 주제별로 인덱싱합니다. 이후 검색 의도에 맞춰 인덱싱한 콘텐츠에 순위를 부여하여 결과로 제공합니다.
3. 이미지 최적화 방법에 대해 알고 있는 게 있나요?
   - 이미지의 용량을 줄이거나, 벡터 이미지(svg)를 활용합니다. 또는 css Sprite 기법을 사용하거나 lazy loading을 활용하는 방법 등이 있습니다.
4. CSS-in-JS에 대해 설명해주세요.
   - 대표적인 라이브러리로 styled-components와 Emotion이 있습니다. 자바스크립트를 사용하여 css를 작성할 수 있으며, 컴포넌트 단위로 추상화되기 때문에 css 모듈간의 의존성을 신경 쓰지 않아도 된다는 장점이 있습니다. 제가 실제로 느꼈던 장점으로는 특정 스타일을 가진 태그의 네임을 커스터마이징 함으로써 가독성이 좋아진다는 장점이 있었습니다. 또한 단점으로는 번들 크기가 증가한다는 점이 있습니다.
5. 왜 일반적으로 CSS `<link>`를 head 태그 사이에 위치시키고, JS `<script>` 태그를 body 직전에 위치시키는 것이 좋은 방법인지 설명하시오.
   - 먼저, `<head>` 안에 `<link>`를 넣는 이유는 파싱 과정에서 DOM tree(HTML의 태그)가 생성되어도, CSSOM Tree(CSS 파일)가 없으면 렌더링이 되지 않아 빈 화면이 뜨게 됩니다. 따라서 빠르게 CSSOM Tree를 읽어와 렌더링을 하기 위해 `<head>` 안에 CSS 파일을 넣어야합니다.
     그리고 `<script>`를 `<body>` 직전에 위치시키는 이유는 파싱 과정에서 `<head>` 안에서 `<script>`를 만나게 되면 파싱을 멈추고, Script 파일을 읽습니다. Script 파일을 읽는 동안 렌더링에 방해가 되어 무거운 스크립트가 실행될 때는 사용자 입장에서 웹페이지가 느리게 보이기 때문에, `<script>`를 `<body>` 직전에 위치시키는 것이 가장 좋은 방법입니다. `<script>`를 `<head>`에 넣어야 하는 경우엔 defer를 사용하는 것이 좋습니다.
6. CSS 전처리기의 장점과 단점은 무엇인가요?
   - CSS 전처리기를 사용하게 되면 selector를 중첩으로 관리할 수 있고, 조건문이나 반복문, 간단한 연산 등을 할 수 있어서 css를 프로그래밍하듯이 코딩할 수 있다는 장점이 있습니다. 단점은 웹에서는 css만 동작하기 때문에 컴파일을 거쳐야합니다.