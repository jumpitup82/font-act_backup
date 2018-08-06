---
description: 데이터의 변경없이 형식된 출력을 지원
---

# Filter

## 선언

로컬 필터

* 컴포넌트 내부에 선언
* 선언된 컴포넌트에서 사용가능

```javascript
// 컴포넌트 내
filters: {
  capitalize: function (value) {
    if (!value) return ''
    value = value.toString()
    return value.charAt(0).toUpperCase() + value.slice(1)
  }
}
```

전역필터

* 컴포넌트 외부에 선언
* 모든 컴포넌트에서 사용가능

```javascript
Vue.filter('capitalize', function (value) {
  if (!value) return ''
  value = value.toString()
  return value.charAt(0).toUpperCase() + value.slice(1)
})
```

## 사용 방법

* 파이프 심볼을 이용
* 중괄호 보간법 혹은 v-bind 표현법 안에서 사용가능
* 필터함수는 첫 번째 전달인자로 표현식의 값\(이전 체이닝의 결과\)를 받음.
* 필터는 체이닝하여 사용가능
* 추가 전달인자 가능. 추가로 전달된 인자는 두번째 인자부터 시작되어 전달됨.

```markup
<!-- 중괄호 보간법 -->
{{ message | capitalize }}

<!-- v-bind 표현 -->
<div v-bind:msg="message | capitalize"></div>

<!-- chaining filter
message가  ABC일 경우 최종 출력은 Abc
-->
<div v-bind:msg="message | lowercase | capitalize"></div>

<!-- 추가 전달인자 
message가 ABC일 경우 최종 출력은 **Abc
-->
<div v-bind:msg="message | lowercase | capitalize | padLeft('*', 5)"></div>
```

