---
description: 동일 페이지의 동적 재작성을 통해 사용자경험을 향상시키는 웹 어플리케이션의 하나
---

# Single Page Application

![](.gitbook/assets/spa-change.jpg)

### Single Page Application 이란?

* 2003 초기에 논의되었지만 용어의 출처는 분분명함.
* 서버로부터 페이지 전체를 수신받지 않고, **현재의 페이지를 동적으로 재작성함으로써 사용자와 상호작용** 하는 웹 어플리케이션 또는 웹 사이트
* **데스크탑 어플리케이션과 흡사한 사용자경험**을 줄 수 있음.

#### 기술적 접근

* Thin server architecture
  * 로직이 서버에서 클라이언트로 이동
  * 웹서버가 순수한 데이터 API 혹은 웹서비스로 발전할 수 있게 함
* Thick Stateful Server Architecture
  * 서버에 클라이언트의 상태를 저장
  * 서버에 특정 요청이 동작하면, 서버는 HTML/Javascript 등을 송신하여 클라이언트를 새로운 상태로 변경
* Thick Stateless Server Architecture
  * 클라이언트는 대개 Ajax를 통해 서버에 현재상태를 나타내는 데이터를 송신하고, 서버는 클라이언트의 일부를 수정할 수 있는 데이터 혹은 코드를 송신
  * 검색엔진 최적화 \(Search engine optimazation\)
* Javascript 실행의 부족\(동일 페이지에 대한\)으로 인해 검색엔진에 제대로 검색되지 않는 단점이 있음
* 검색엔진에 따른 최적화방법을 개별적으로 적용
  * Naver: [Syndication](https://webmastertool.naver.com/index.naver)
* 특정 페이지에 대한 SSR\(서버사이드렌더링\)
* [Google SEO 가이드](https://support.google.com/webmasters/answer/7451184?hl=ko)

#### _References_

{% embed data="{\"url\":\"https://en.wikipedia.org/wiki/Single-page\_application\",\"type\":\"link\",\"title\":\"Single-page application\",\"description\":\"A single-page application \(SPA\) is a web application or web site that interacts with the user by dynamically rewriting the current page rather than loading entire new pages from a server. This approach avoids interruption of the user experience between successive pages, making the application behave more like a desktop application. In an SPA, either all necessary code – HTML, JavaScript, and CSS – is retrieved with a single page load,&\#91;1&\#93; or the appropriate resources are dynamically loaded and added to the page as necessary, usually in response to user actions. The page does not reload at any point in the process, nor does control transfer to another page, although the location hash or the HTML5 History API can be used to provide the perception and navigability of separate logical pages in the application.&\#91;2&\#93; Interaction with the single page application often involves dynamic communication with the web server behind the scenes.\\n\",\"icon\":{\"type\":\"icon\",\"url\":\"https://en.wikipedia.org/static/apple-touch/wikipedia.png\",\"aspectRatio\":0}}" %}

