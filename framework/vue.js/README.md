# Vue.js

### Vue 소개

Progressive Javascript Framework



{% embed data="{\"url\":\"https://kr.vuejs.org/index.html\",\"type\":\"link\",\"title\":\"Vue.js\",\"description\":\"Vue.js - 프로그레시브 자바스크립트 프레임워크\",\"icon\":{\"type\":\"icon\",\"url\":\"https://kr.vuejs.org/images/icons/android-icon-192x192.png\",\"width\":192,\"height\":192,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://vuejs.org//images/logo.png\",\"width\":400,\"height\":400,\"aspectRatio\":1}}" %}

#### 특징

* Approchable
* Versatile
* Performant
* Maintainable
* Testable

#### 탄생 배경

* 2013년 google 엔지니어 Evan You가 개발
*  AngularJS에서 좋아하는 특성만 담은 가벼운 라이브러리를 만들고자 탄생
* 2016년 4월 V2.0 발표 이후 인기 얻기 시

#### 장점

* 배우기 쉽다.
* 다른 라이브러리나 기존 프로젝트와의 통합이 쉽다.
* Virtual DOM을 사용하여 일반적인 상황에서 충분히 빠르다.

### Reactive in Depth {#separation-of-concerns}

​데이터 변경 추적

* Object.defineProperty 의 getter/setters 를 이용하여 property 변경을 추적
* 이러한 이유때문에 ES5를 지원하지 않는 IE8 이하의 브라우저는 지원되지 않음

![](../../.gitbook/assets/responsive-data.png)

### Separation of Concerns in Vue.js

* 관심사의 분리가 파일타입의 분리\(css, js 등\)와 같지 않다고 봄
* 현대적인 UI 개발에서 코드베이스를 서로 얽혀있는 세 개의 거대한 레이어\(HTML, CSS, JS\)로 나누는 대신, 느슨하게 결합 된 컴포넌트로 나누고 구성하는 것이 더 중요
* 컴포넌트 내부에서 템플릿, 로직 및 스타일이 본질적으로 결합되어 배치되면 컴포넌트의 응집력과 유지 보수성이 향상됩니다.



