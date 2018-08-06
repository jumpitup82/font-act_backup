---
description: Vue.js를 사용한 SPA 를 쉽게 만들 수 있도록 작성된 공식 라우터
---

# Router

## Vue Routing

URL의 변경에 따라 표시될 Vue Component View를 연결하는 것.

## Hash-Based routing

anchor\(\#\)를 사용한 경로의 특성을 이용하여 전체 시뮬레이트한 URL을 라우팅에 이용하는 것.

* ex\) [http://route-test.com/\#/products/123](http://route-test.com/#/products/123)
* \#뒤쪽의 주소\(\#/products/123\)는 서버로 전송되지 않음.
* \#이후의 주소의 변경 또한 페이지의 리로드를 발생시키지 않음.

## History Mode routing

HTML5의 history.pushState API를 라우팅에 이용하는 것.

* history.pushState API를 활용하여 페이지 리로드없이 URL 변경을 이용 
* URL의 변경에 따라 Client-side의 페이지가 연결되기 때문에, 변경된 URL로 직접 접근할 경우 404 오류를 유발 -&gt; 서버에 대체경로를 추가하여 처리\(ex. /abc/def -&gt; /index.html\)

## Features

* 모듈화된, 컴포넌트 기반의 라우터 설정
* 라우터 파라미터, 쿼리, 와일드카드

```javascript
const User = {
  template: '<div>User</div>'
}

const router = new VueRouter({
  routes: [
    // 동적 세그먼트는 콜론으로 시작합니다.
    { path: '/user/:id', component: User }
  ]
})
```

* Vue.js의 트랜지션 시스템을 이용한 트랜지션 효과
* 세밀한 네비게이션 컨트롤
* active CSS 클래스를 자동으로 추가해주는 링크
* HTML5 히스토리 모드 또는 해시 모드\(IE9에서 자동으로 폴백\)
* 사용자 정의 가능한 스크롤 동작

## 기본사용법

```markup
<script src="https://unpkg.com/vue-router/dist/vue-router.js"></script>

<div id="app">
  <h1>Hello App!</h1>
  <p>
    <!-- 아래의 router-link 를 통해 /foo 또는 /bar 로 URL이 변경되는 링크가 생성 -->
    <router-link to="/foo">Go to Foo</router-link>
    <router-link to="/bar">Go to Bar</router-link>
  </p>
  <!-- URL의 변경에 따라 표시되는 Component View가 아래의 router-view 자리에 표시 -->
  <router-view></router-view>
</div>
```

```javascript
const Foo = { template: '<div>foo</div>' }
const Bar = { template: '<div>bar</div>' }

const router = new VueRouter({
  routes: [
  { path: '/foo', component: Foo },
  { path: '/bar', component: Bar }
]})

const app = new Vue({
  router
}).$mount('#app')
```

