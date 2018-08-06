# 사용자 정의 디렉티브

## 디렉티브 작성 및 사용

```javascript
// 전역 사용자 정의 디렉티브 v-focus 등록
Vue.directive('focus', {
  // 바인딩 된 엘리먼트가 DOM에 삽입되었을 때...
  inserted: function (el) {
    // 엘리먼트에 포커스를 줍니다
    el.focus()
  }
})
```

```markup
<input v-focus>
```

## 디렉티브 훅

* bind: 디렉티브가 처음 엘리먼트에 바인딩 될 때 한번 만 호출 
* inserted: 바인딩 된 엘리먼트가 부모 노드에 삽입 되었을 때 호출
* update: 포함하는 컴포넌트가 업데이트 되었을 때 호출
* componentUpdated: 포함하고 있는 컴포넌트와 그 자식들이 업데이트 되었을 때 호출
* unbind: 디렉티브가 엘리먼트로 부터 언바딩 된 경우 한번 만 호출

