---
description: DOM요소에게 정의된 행동을 수행하도록 알리는 지시어. DOM과 모델의 상호작용.
---

# Directive

## 내장 Directives

* v- 접두사로 시작
* 속성값은 단일 javascript 표현 \(v-for는 제외\)

### 조건부 렌더링

#### &lt;v-if&gt;

* 조건에 맞지 않으면 렌더링 자체를 하지 않는다.
* 초기 렌더링 비용은 낮 변경에 대한 비용이 크므로 조건이 자주 바뀌지 않는 경우 사용 

```markup
<div v-if="type === 'A'">
  A
</div>
<div v-else-if="type === 'B'">
  B
</div>
<div v-else-if="type === 'C'">
  C
</div>
<div v-else>
  Not A/B/C
</div>
```

#### &lt;v-show&gt;

* 조건과 상관없이 렌더링 되며 화면 표시 여부가 조건에 따라 달라진다. 
* 초기 렌더링 비용은 높고 변경에 대한 비용이 높아 자주 토글 되는 View에 사용 

```markup
<div v-show="isTrue">
    안녕하세요!!
</div>
```

### 반복 렌더링

#### Array

```javascript
var vm = new Vue({
  el: '#example-1',
  data: {
    items: [
      { name: 'Foo' },
      { name: 'Bar' }
    ]
  }
})
```

```markup
<ul id="example-1">
  <li v-for="item in items">
    {{ item.name }}
  </li>
</ul>
```

* Foo
* Bar

```markup
<ul id="example-1">
  <li v-for="(item, index) in items">
    <span>{{ index + 1 }}</span>
    <span> : </span>
    <span>{{ item.name }}</span>
  </li>
</ul>
```

* 1 : Foo
* 2: Bar

#### Array의 변경 감지

* 감시중인 Array의 변이 메소드를 래핑하여 변경 감지 \(push, pop, shift, unshift, splice, sort, reverse\)
* 배열 대체를 통한 감지
* Vue.set Api를 통한 감지

```javascript
items.push({ name: 'ABC'})                       //OK
vm.items = [...items, { name: 'ABC'}]            //OK
Vue.set(vm, 2, { name: 'ABC'})                   //OK
vm.$set(vm, 2, { name: 'ABC'})                   //OK

vm.items[2] = { name: 'ABC'}                     //Fail
vm.items.length = 1                              //Fail
```

#### Object

```javascript
var example1 = new Vue({
  el: '#example-1',
  data: {
    user: {
      name: 'Foo',
      age: 36,
    }
  }
})
```

```markup
<ul id="v-for-object" class="demo">
  <li v-for="(value, key, index) in object">
    <span>{{ index + 1 }} </span>
    <span>{{ key }} : {{ value }}</span>
  </li>
</ul>
```

* 1 name : Foo
* 2 age : 36

#### Object의 변경 감지

* javascript 의 한계로 속성의 추가나 삭제 감지하지 못한다.
* Vue.set API 활용

