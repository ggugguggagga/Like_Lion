***
### HTML, CSS, Javascript 란? 

|Name|Description|
|:---:|:---:|
|![HTML logo](/image/HTML.png)|HTML은 웹 브라우저 창에 웹 문서의 내용을 보여주는 데 필요한 것 이다. HTML은 웹 브라우저의 여러 내용 중에서 제목과 본문, 이미지, 표와 같은 것을 정하는데에 사용한다.|
|![CSS logo](/image/CSS.png)|CSS는 HTML로 만든 내용을 사용자가 알아보기 쉽게 꾸미거나 사용하기 편리하도록 배치할 때 사용한다.또한 반응형 웹 디자인을 만들려면 CSS를 알아야한다.|
|![JS logo](/image/JS.png)|동적인 효과를 사용하려면 자바스크립트가 필요하다. 그리고 규모가 큰 웹 사이트 개발에서는 리액트(React)나, 뷰(Vue)같은 자바스크립트 프레임워크를 사용한다.|

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

![Rendering_Engine](/image/DOM.png)

> ##### DOM(Document Object Model)
> `웹페이지에 대한 프로그래밍 인터페이스이다. 여러 프로그램들이 페이지 콘텐츠 및 구조, 스타일을 읽고 조작할 수 있는 API를 제공한다.`

<br>

`DOM`은 원본 `HTML` 문서의 객체 기반 표현 방식이며 DOM의 개체 구조는 `Node tree`로 표현된다.

![Rendering_Engine](/image/htmlEX.png)

위의 HTML 코드는 아래와 같이 표현된다.

![Rendering_Engine](/image/domNodeEX.png)

`DOM`은 `HTML` 문서로부터 생성되지만 항상 동일하지는 않다.

-**HTML**: 화면에 보이고자 하는 모양과 구조를 문서로 만들것으로 텍스트로 구성되어있다. 즉, 최초에 화면을 그릴때 사용하는 설계도이다.<br>
-**DOM**: `HTML`문서의 내용과 구조가 객체 모델로 변화되어 다양한 프로그램에서 사용될 수 있다. 즉, 설계도를 이용하여 실제로 화면에 나타내지는 인터페이스이다.

***
### HTTP & HTTPS
<br>

![Rendering_Engine](/image/HTTP.png)

`HTTP(Hyper Text Tansfer Protocol)`란 **서버/클라이언트 모델을 따라 데이터를 주고 받기 위한 프로토콜**이다. 즉, `HTTP`는 인터넷에서 하이퍼텍스트를 교환하기 위한 통신 규약으로, 80번 포트를 사용하고있다. 따라서 `HTTP` 서버가 80번 포트에서 요청을 기다리고 있으며, 클라이언트는 80번 포트로 요청을 보내게된다.

하지만 `HTTP`는 암호화가 되지 않은 평문 데이터를 전송하는 프로토콜이였기 때문에, `HTTP`로 비밀번호나 주민등록번호 등을 주고 받으면 제 3자가 정보를 조회할 수 있었기에 이러한 문제를 해결하기 위해서 `HTTPS`가 등장하게 되었다.

![Rendering_Engine](/image/HTTPS.png)

즉, `HyperText Protocol over Secure Socket Layer`, `HTTP over TLS`, `HTTP over SSL`, `HTTP Secure` 등으로 불리는 `HTTPS`는 **HTTP에 데이터 암호화가 추가된 프로토콜**이다. `HTTPS`는 `HTTP`와 다르게 443번 포트를 사용하며, 네트워크 상에서 중간에 제 3자가 정보를 볼 수 없도록 암호화를 지원하고있다.

***
### AJAX 란?

- AJAX (Asynchronous Javascript And Xml) : 비동기식 자바스크립트와 xml의 약자
- 브라우저가 가지고있는 XMLHttpRequest 객체를 이용해서 전체 페이지를 새로 고치지 않고도 페이지의 일부만을 위한 데이터를 로드하는 기법
- 자바스크립트를 통해서 서버에 데이터를 비동기 방식으로 요청하는 것

> ##### XML
> eXtensible Markup Language의 두문자어로, W3C 권고 확정성이 있는 마크업 언어로, W3C가 인간과 응용프로그램간, 혹은 응용프로그램 간에 정보를 쉽게 교환하기 위해 만든 데이터 교환 포멧이다. 즉, 확장될 수 있는 표시 언어이다. - 데이터를 설명하는 태그(Tag)를 사용자 마음대로 정의할 수 있다.<br> 
> - `XML`은 Data를 전달하는 데에 포커스를 맞춘 언어이다.
> - `HTML`은 Data를 표현하는 데에 포커스를 맞춘 언어이다.
> - `HTML`의 태그는 이미 약속한 태그들만 사용이 가능하다. ex) ```<p></p>```
> - `XML`의 태그는 사용자가 임의로 만들어 사용이 가능하다. <br>
> [예시](http://www.tcpschool.com/xml/xml_basic_structure) <br><br>
> *데이터를 알아서 우리가 어디에 사용하는가?*

> ##### 비동기 방식이란?
> 자바스크립트는 싱글 스레드 방식이라서 한개의 동작을하면 다음에 실행시켜야하는 함수로 넘어갈 수 없어서 블로킹(작업 중단)이된다. 그래서 멀티 스레드처럼 여러가지 일을 할 수 있게 만드는 것이 비동기적 프로그래밍이다.
<br>

##### AJAX를 사용 가능하게 만드는 것
- HTML
- DOM
- JavaScript
- XMLHttpRequest

##### 사용하는 이유
 단순하게 웹화면에서 무언가 부르거나 데이터를 조회하고 싶을 경우, 페이지 전체를 새로고침하지 않기 위해 사용한다. 기본적으로 `HTTP 프로토콜`은 클라이언트쪽에서 요청하고 서버에서 반응하면 이어졌던 연결이 끊기는데, 이때 내용을 갱신하기 위해서는 다시 요청하고 반응하며 페이지 전체를 갱신해야한다. 하지만 이는 비효율적이다.<br>

 그래서 `AJA`X는 `HTML` 페이지 전체가 아닌 일부분만 갱신할 수 있도록 `XMLHttpRequest`객체를 통해 서버에 요청한다. 그럼 `JSON`이나 `XML`형태로 필요한 데이터만 받아 갱신하기 때문에 효율적이다.

 |Name|Description|
 |:---:|:---:|
 |장점|웹페이지의 속도향상<br>서버의 처리가 완료될 때까지 기다리지 않고 처리가 가능하다.<br>다양한 UI기능을 구현할 수 있다.|
 |단점|페이지 이동없는 통신으로 인한 보안상의 문제가 있다.<br>연속으로 데이터를 요청하면 서버 부하가 증가할 수 있다.<br>디버깅이 힘들다.<br>기능이 한정 되어있다.|

 ***
 ### 반응형 웹이란?
 ![반응형_웹](/image/web.png)
 <br>
 반응형 웹이란 PC, TV, 네비게이션, 스마트 기기 등 기기마다 또는 환경마다 최적화된 웹사이트를 제공해주는 것을 말한다.

 예를 들어 화면이 작은 기기에서 반응형 웹으로 제작된 웹사이트를 접속했을 때는 웹사이트의 구조를 작은 화면에 최적화된 구조로 변경하여 보여주고, 큰 화면을 가진 기기에서는 웹사이트의 구조를 큰 화면에 최적화된 구조로 변경하여 보여준다.

 이처럼 기기의 화면이나 환경에 맞게 자유자재로 변하는 것이 반응형 웹이다.
