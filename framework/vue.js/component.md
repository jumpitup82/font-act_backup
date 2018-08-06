# Component

## 특징

* Vue의 핵심 기능 중 하나 
* HTML을 확장하여 재사용 가능한 코드 작성에 도움 
* 사용자 정의 엘리먼트 

![vue.js &#xB85C; &#xB9CC;&#xB4E0; &#xC5B4;&#xD50C;&#xB9AC;&#xCF00;&#xC774;&#xC158;&#xC740; Component Tree&#xC640; &#xAC19;&#xC740; &#xD615;&#xD0DC;](../../.gitbook/assets/components.png)

## Component 등록

전역 컴포넌트 예

```javascript
<div id="example">
  <my-component></my-component>
</div>

<script>
  Vue.component('my-component', {
    template: '<div>사용자 정의 컴포넌트 입니다!</div>'
  })

  new Vue({
    el: '#example'
  })
<script>
```

## Data Flow

![](../../.gitbook/assets/data-flow-1.png)

## Single File Component

```markup
<template>
    <div class="header">
        {{ title }}
    </div>
    <child-component :message="message"/> 
</template>

<script>
import ChildComponent from './ChildComponent.vue'

export default {
    data() {
        return {
            title: 'single file component',
            message: 'message to child component'
        }
    },
    components: {
        ChildComponent
    }
}
</script>

<style scoped>
    .header{
        font-size: 3em;
    }
</style>
```

* 빌드도구를 사용 해야 함
* Component scoped CSS 지원
* 특정  Template engine 사용 가능
* 생산성 향상에 도움을 주는 javascript/css 전처리기 사용 가능
* ES6사용 권장

### Javascript와 CSS 파일 분리 가능

```markup
<template>
    <div> {{ message }}</div>
</template>
<script src="./my-component.js"></script>
<style src="./my-component.css"></style>
```

