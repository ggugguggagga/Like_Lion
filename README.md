***
### HTML, CSS, Javascript 란? 

|HTML|CSS|JS|
|:---:|:---:|:---:|
|![HTML logo](/image/HTML.png)|![CSS logo](/image/CSS.png)|![JS logo](/image/JS.png)|
|HTML은 웹 브라우저 창에 웹 문서의 내용을 보여주는 데 필요한 것 이다. HTML은 웹 브라우저의 여러 내용 중에서 제목과 본문, 이미지, 표와 같은 것을 정하는데에 사용한다.|CSS는 HTML로 만든 내용을 사용자가 알아보기 쉽게 꾸미거나 사용하기 편리하도록 배치할 때 사용한다.또한 반응형 웹 디자인을 만들려면 CSS를 공부해야한다.|동적인 효과를 사용하려면 자바스크립트가 필요하다. 그리고 규모가 큰 웹 사이트 개발에서는 리액트(React)나, 뷰(Vue)같은 자바스크립트 프레임워크를 사용한다.|

***
### 브라우저 작동 방식
![Browser](/image/Browser.png)
브라우저의 구성 요소에는 ``User Interface``, ``Browser Engine``, ``Rendering Engine``, ``Networking``, ``JS Engine``, ``UI Backend``, ``Data Storage``가 있다.

|Name|Description|
|:---:|:---:|
|``User Interface``|사용자가 접근할 수 있는 영역으로 검색창, 뒤로가기/앞으로가기, 새로 고침 등 브라우저를 구성하는 GUI 부분이다.|
|``Browser Engine``|User Interface와 Rendering Engine 사이의 동작을 제어한다. Data Storage에 있는 데이터를 이용해 다양한 작업을 한다.|
|``Rendering Engine``|브라우저에서 핵심이며, HTML, CSS 등을 해석해서 화면에 출력하는 등 요청한 콘텐츠를 화면에 출력한다.|
|``Networking``|HTTP 요청을 하며 네트워크를 호출 할 수 있고, 브라우저마다 독립적이다.|
|``JS Engine``|javascript를 해석하고 실행한다.|
|``UI Backend``|기본적이 위젯을 그리는 인터페이스다.|
|``Data Storaage``|Local Storage, Indexed DB, 쿠키 등 브라우저 메모리를 활용하여 저장하는 영역이다.|
<br>

![Rendering_Engine](/image/RenderingEngine.png)
<br>

1. 브라우저는 서버로 부터 HTML 정보를 받고, Rendering Engine이 HTML 정보를 해석해서 DOM tree로 만든다. 
2. DOM tree와 외부 CSS파일과 스타일 요소를 해석해서 Render tree를 만든다. 
3. Render tree의 각 노드에 대해서 화면 상 어디에 배치할 지 결정한다.
4. UI Backend에서 Render tree를 그리게되고, 사용자가 볼 수 있도록 화면에 출력된다.
<br>

![Rendering_Engine](/image/RenderingEngineEX.png)

***
### DOM 란?

> ##### DOM(Document Object Model)
> `웹페이지에 대한 프로그래밍 인터페이스이다. 여러 프로그램들이 페이지 콘텐츠 및 구조, 스타일을 읽고 조작할 수 있는 API를 제공한다.`

<br>

DOM은 원본 HTML 문서의 객체 기반 표현 방식이며 DOM의 개체 구조는 `Node tree`로 표현된다.

***
### HTTP & HTTPS