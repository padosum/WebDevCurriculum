# Quest 01. HTML과 웹의 기초

## Introduction
* HTML은 HyperText Markup Language의 약자로, 웹 브라우저에 내용을 표시하기 위한 가장 기본적인 언어입니다. 이번 퀘스트를 통해 HTML에 관한 기초적인 사항들을 알아볼 예정입니다.

## Topics
* HTML의 역사
  * HTML 4.01, XHTML 1.0, XHTML 1.1
  * XHTML 2.0과 HTML5의 대립
  * HTML5와 현재
* 브라우저의 역사
  * Mosaic와 Netscape
  * Internet Explorer의 독점시대
  * Firefox와 Chrome의 등장
  * iOS Safari와 모바일 환경의 브라우저
  * Edge와 Whale 등의 최근의 Chromium 계열 브라우저
* HTML 문서의 구조
  * `<html>`, `<head>`와 `<body>` 등의 HTML 문서의 기본 구조
  * 시맨틱 엘리먼트
  * 블록 엘리먼트와 인라인 엘리먼트의 차이

## Resources
* [MDN - HTML](https://developer.mozilla.org/ko/docs/Web/HTML)
* [HTML For Beginners](https://html.com/)
* [History of the web browser](https://en.wikipedia.org/wiki/History_of_the_web_browser)
* [History of HTML](https://en.wikipedia.org/wiki/HTML)
* [StatCounter](https://gs.statcounter.com/)

## Checklis
* **HTML 표준의 역사는 어떻게 될까요?**
  * HTML은 1989년에 팀 버너스리에 의해 처음 개발되어 빠르게 발전되었습니다. 중간에 XHTML 표준 개발에 대한 시도가 시장으로부터 외면을 받았고 이 시점에 W3C와 생각이 다른 업체 애플, 모질라, 오페라가 WHATWG를 결성해 HTML, CSS, DOM 및 자바스크립트에 대한 개선 표준 개발을 시작하게 되었습니다. 
    * [http://weekly.tta.or.kr/weekly/files/20104826094826_admin.pdf](http://weekly.tta.or.kr/weekly/files/20104826094826_admin.pdf)
  * **HTML 표준을 지키는 것은 왜 중요할까요?**
    * HTML 표준이란 HTML에서 사용되는 표준 기술이나 규칙을 의미합니다. HTML 표준을 준수함으로써 HTML을 사용한 웹 페이지가 브라우저, 기종, 플랫폼에 상관없이 정상적인 기능 작동이 가능합니다.
  * **XHTML 2.0은 왜 세상에 나오지 못하게 되었을까요?**
    * 브라우저 및 서버 개발자들이 XHTML 대신 HTML에 거의 정착했다고 결론이 지어지면서 HTML 5에만 집중하게 되었고 XHTML 개발은 중단되었습니다. 
    * [https://www.quora.com/Why-was-the-XHTML-2-0-standard-eventually-abandoned](https://www.quora.com/Why-was-the-XHTML-2-0-standard-eventually-abandoned)
  * **HTML5 표준은 어떤 과정을 통해 정해질까요?**
    * 현재 HTML5 표준은 WHATWG라는 조직이 만들고 있습니다. 2011년까지 WHATWG와 W3C는 같이 협력하는 관계였으나, 서로 목표가 다름을 밝히며 분리되었습니다. WHATWG는 새로운 기능 구현에 더 관심이 있었고, 2019년 WHATWG의 Living Standard가 HTML5 표준이 되었습니다.
    * [https://mytory.net/2021/04/20/w3c-and-whatwg.html](https://mytory.net/2021/04/20/w3c-and-whatwg.html)  
* **브라우저의 역사는 어떻게 될까요?**
  * **Internet Explorer가 브라우저 시장을 독점하면서 어떤 문제가 일어났고, 이 문제는 어떻게 해결되었을까요?**
    * IE가 시장을 독점을 하며 추가적인 기능 개선을 거의 중단하다시피 하게되었고 개발자들은 낡은 브라우저를 사용하는 사용자들을 위해 최신 기술을 개발에 적용하지 못하게 됩니다. 하지만 2007년 아이폰이 출시되면서 모바일 시대가 찾아오게 되었고, 브라우저 시장에도 큰 영향을 끼칩니다. 모바일이 대세가 됨에도 모바일용 브라우저를 출시하지 않은 IE는 몰락하게 되었고 모바일 강세를 보여준 크롬과 사파리의 점유율이 올라가게 됩니다. 기존 IE를 사용하던 사용자들은 경쟁 제품으로 대거 이탈하게 되었습니다.
  * **현재 시점에 브라우저별 점유율은 어떻게 될까요? 이 브라우저별 점유율을 알아보는 것은 왜 중요할까요?**
    * 현재는 Chrome이 독점하고 있습니다. 웹 페이지를 개발할 때 해당 웹 페이지를 이용하는 대상이 어떤 브라우저를 사용하느냐에 따라 기술 적용 등, 개발 환경과 프로세스가 달라지기 때문에 브라우저 점유율이 중요합니다.
  * **브라우저 엔진(렌더링 엔진)이란 무엇일까요? 어떤 브라우저들이 어떤 엔진을 쓸까요?**
    * 브라우저 엔진은 모든 웹 브라우저의 핵심이 되는 소프트웨어 구성 요소로 HTML 문서와 기타 자원의 웹 페이지를 사용자의 장치에 시각 표현으로 변환시키는 작업을 합니다.
    * 게코(Gecko)는 Firefox, 블링크(Blink)는 Chrome과 Opera, Webkit은 Safari 등이 사용하고 있습니다.
  * **모바일 시대 이후, 최근에 출시된 브라우저들은 어떤 특징을 가지고 있을까요?**
    * 데스크톱용과 모바일용 브라우저가 계정을 통해 북마크, 탭 등을 연동할 수 있는 기능들이 생겨났고, 아무래도 모바일 환경에 적용할 수 있는 다양한 써드파티 앱(오프라인에서 웹 탐색, 광고 제거)등이 만들어지게 되었습니다.
* **HTML 문서는 어떤 구조로 이루어져 있나요?**
  ```html
  <!DOCTYPE html>
  <html>
    <head>
      <meta charset="utf-8" name="description" content="WebDevCurriculum입니다.">
      <title>Hello World</title>
    </head>
    <body>
      <p>Hello~</p>
    </body>
  </html>
  </html>
  ```
  * **`<head>`에 자주 들어가는 엘리먼트들은 어떤 것이 있고, 어떤 역할을 할까요?**
    * `<title>`는 HTML 문서 전체의 타이틀을 표현하기 위한 메타데이터입니다. 
    * `<meta>` 엘리먼트는 데이터를 설명하는 데이터로 `charset` 속성으로 문서의 인코딩을 특정할 수 있고, `name`과 `content` 속성으로 저자와 설명등의 정보 입력이 가능합니다.
  * **시맨틱 태그는 무엇일까요?**
    * 검색 엔진은 매일 전세계의 웹사이트 정보를 수집할 때 HTML 코드만으로 코드의 의미를 인지하여야 하는데 이때  시맨틱 태그를 통해 해석을 하게 됩니다.
    * **시맨틱 엘리먼트를 사용하면 어떤 점이 좋을까요?**
      * 시맨틱 엘리먼트는 개발자가 의도한 요소의 의미를 명확하게 드러냅니다. 검색 엔진에게 콘텐츠의 의미를 명확하게 설명하고, 코드의 가독성도 높여 유지보수에도 도움이 됩니다.
    * **`<section>`과 `<div>`, `<header>`, `<footer>`, `<article>` 엘리먼트의 차이점은 무엇인가요?**
  * **블록 레벨 엘리먼트와 인라인 엘리먼트는 어떤 차이가 있을까요?**
    * 블록 레벨 엘리먼트는 항상 새 줄로 시작이 되고, 줄 전체 너비를 차지합니다. 
    * 인라인 엘리먼트는 새 줄로 시작하지 않고, 다른 엘리먼트와 함께 수평으로 한 행에 존재합니다. 필요한 만큼만 너비를 차지합니다.

## Quest
* [x] [이 화면](screen.png)의 정보를 HTML 문서로 표현해 보세요. 다만 CSS를 전혀 사용하지 않고, 문서의 구조가 어떻게 되어 있는지를 파악하여 구현해 보세요.
  * [CSS Naked Day](https://css-naked-day.github.io/)는 매년 4월 9일에 CSS 없는 웹 페이지를 공개하여 내용과 마크업에 집중한 HTML 구조의 중요성을 강조하는 행사입니다.
* [x] 폴더에 있는 `skeleton.html` 파일을 바탕으로 작업해 보시면 됩니다.
  * 화면을 구성하는 큰 요소들을 어떻게 처리하면 좋을까요?
  * HTML 문서상에서 같은 층위에 비슷한 요소들이 반복될 때는 어떤 식으로 처리하는 것이 좋을까요?

## Advanced
* **XML은 어떤 표준일까요? 어떤 식으로 발전해 왔을까요?**
  * XML은 인터넷에 연결된 시스템끼리 데이터를 쉽게 주고받으려고 만든 표준입니다. W3C에서 표준화 작업이 시작되어 1998년에 XML 1.0 표준 권고안이 나오게 됩니다. 
* **YML, Markdown 등 다른 마크업 언어들은 어떤 특징을 가지고 있고, 어떤 용도로 쓰일까요?**
  * YAML은 사람이 보기에 매우 이해하기 쉬운 형태를 가지고 있습니다. `Key:Value` 형태에 계층 구조로 나타내 동일한 구성이 중복되는 것을 방지하는 특징을 가지고 있습니다. DB나 서버 접속에 필요한 URL, ID, Password, 경로 등을 저장해놓고 가져올 때 사용합니다.
  * Markdown은 텍스트 기반의 마크업 언어이고, 특수기호와 문자를 사용해 빠르게 컨텐츠 작성이 가능한 특징이 있습니다. 다양한 형태로 변환이 가능하고 지원하는 프로그램, 플랫폼이 다양합니다. 하지만 표준이 없어 도구에 따라 방식이 다른 경우가 있습니다. Github 등의 저장소에서 정보를 기록하는 용도로 많이 사용합니다. (README.md 파일 등)  