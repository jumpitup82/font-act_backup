---
description: Syntactically Awesome Style Sheets
---

# SASS

### Variables

$문자를 변수선언 심볼로 사용

```css
// 변환전
$font-stack: Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```

```css
// 변환된 CSS
body {
  font: 100% Helvetica, sans-serif;
  color: #333;
}
```

### Nesting

계층구조를 가지는 형태로 작성가능

```css
// 변환전
nav {
  ul {
    margin: 0;
  }
  li { display: inline-block; }
}
```

```css
// 변환된 CSS
nav ul {
  margin: 0;
}

nav li {
  display: inline-block;
}
```

### Partials and Import

CSS 를 모듈화 하여 작성. 

기존CSS Import 의 경우 HTTP request를 사용하만, Sass  Import 의 경우 빌드 타임에 하나의 파일로 번들링 

```css
// _reset.scss

html,
body,
ul,
ol {
  margin:  0;
  padding: 0;
}
```

```css
// base.scss

@import 'reset';

body {
  font: 100% Helvetica, sans-serif;
  background-color: #efefef;
}
```

### Mixins

재사용 가능한 형태의 CSS 선언을 지

```css
@mixin transform($property) {
  -webkit-transform: $property;
      -ms-transform: $property;
          transform: $property;
}

.box { @include transform(rotate(30deg)); }
```

```css
// 변환된 CSS
.box {
  -webkit-transform: rotate(30deg);
  -ms-transform: rotate(30deg);
  transform: rotate(30deg);
}
```

### Extend/Inheritance

CSS 의 set을 공유할 수 있게 함

%를 symbol 로 사용하며, 사용되지 않은 것은 실제 CSS에 출력되지 않음

```css
// 변환전
// This CSS won't print because %equal-heights is never extended.
%equal-heights {
  display: flex;
  flex-wrap: wrap;
}

// This CSS will print because %message-shared is extended.
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.message {
  @extend %message-shared;
}

.success {
  @extend %message-shared;
  border-color: green;
}

.error {
  @extend %message-shared;
  border-color: red;
}

.warning {
  @extend %message-shared;
  border-color: yellow;
}
```

```css
// 변환된 CSS
.message, .success, .error, .warning {
  border: 1px solid #cccccc;
  padding: 10px;
  color: #333;
}

.success {
  border-color: green;
}

.error {
  border-color: red;
}

.warning {
  border-color: yellow;
}
```

### Operators

+, -, \*, / and % 와 같은 수학 연산자들을 사용가능

```css
// 변환
.container { width: 100%; }


article[role="main"] {
  float: left;
  width: 600px / 960px * 100%;
}

aside[role="complementary"] {
  float: right;
  width: 300px / 960px * 100%;
}
```

```css
// 변환된 CSS
.container {
  width: 100%;
}

article[role="main"] {
  float: left;
  width: 62.5%;
}

aside[role="complementary"] {
  float: right;
  width: 31.25%;
}
```

