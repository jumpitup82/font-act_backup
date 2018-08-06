---
description: 'v-on 디렉티브를 사용하여 DOM를 리스닝 하고, 트리거 될때 javascript 실행 가능하며 약어로 @ 사용 가능.'
---

# 이벤트 핸들링

### 메소드 이벤트 핸들러

```markup
<div id="menu"> 
    <button v-on:click="onButtonClick">...</button>
</div>
```

```javascript
var vm = new Vue({
    el: '#menu',
    methods: {
        onButtonClick (event) {
            ...
        }
    }
});
```

### 인라인 메소드 핸들러

```markup
<div id="menu"> 
    <button v-on:click="onButtonClick('hi')">...</button>
</div>
```

```javascript
var vm = new Vue({
    el: '#menu',
    methods: {
        onButtonClick (message, event) {
            //핸들러의 마지막 인자는 event 객체
            ...
        }
    }
});
```

## 이벤트 수식어

### 이벤트 기본 수식어

```markup
<!-- 클릭 이벤트 전파가 중단됩니다 -->
<a @click.stop="doThis"></a>

<!-- 제출 이벤트가 페이지를 다시 로드 하지 않습니다 -->
<form @submit.prevent="onSubmit"></form>

<!-- 수식어는 체이닝 가능합니다 -->
<a @click.stop.prevent="doThat"></a>

<!-- 단순히 수식어만 사용할 수 있습니다 -->
<form @submit.prevent></form>

<!-- 이벤트 리스너를 추가할 때 캡처모드를 사용합니다 -->
<div @click.capture="doThis">...</div>

<!-- 이벤트 리스너를 추가하며 한번만 트리거링함 -->
<div @click.once>...</div>
```

### 키 수식어

```markup
<!-- keyCode가 13일 때만 `vm.submit()`을 호출합니다  -->
<input v-on:keyup.13="submit">
```

### Alias

```markup
<!-- 위와 같습니다 -->
<input v-on:keyup.enter="submit">
```

* enter, tab, delete, esc, space, up, down, left, right

### 사용자 지정 키 수식어

```javascript
// `v-on:keyup.f1`을 사용할 수 있습니다.
Vue.config.keyCodes.f1 = 112
```

### 시스템 키 수식어

ctrl, alt, shift, meta

```markup
<!-- Alt + C -->
<input @keyup.alt.67="clear">

<!-- Ctrl + Click -->
<div @click.ctrl="doSomething">Do something</div>
```

### 마우스 버튼 수식어

left, right, middle

```markup
<button @click.right="doSomething">...</button>
<button @click.ctrl.right="doSomething">...</button>
```

