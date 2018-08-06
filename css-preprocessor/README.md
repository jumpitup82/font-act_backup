---
description: 변형 CSS 언어를 표준 CSS 언어로 변환시키는 처리기
---

# CSS Preprocessor

### 필요한 이유 

* CSS 는 원시적이고 완성적이지 않음. 
* function 을 만들거나, 재사용 혹은 상속등의 개념을 사용하기가 매우 어렵기 때문에, 시스템이 커질수록 유지보수에 큰 어려움을 겪기때문에 더 성숙한 모델이 필요.

### 어떤 부분에서 유용한가?

* $variables
  * 의미없는 Color Code\(\#1F2D47\)가 아닌 의미 있는 변수명을 사용할 수 있다.
  * 가독성 향상
  * 코드 중복 감소
* @import
  * 기존에 존재하는 &lt;link&gt; 와는 달리 최종적으로 배포되는 파일을 하나로 유지하면서도 의미있는 단위로 파일을 분리할 수 있다.
* @mixins
  * Javascript 의 function과 흡사한 기능을 제공
* @extend
  * 하나의 클래스에 다른 클래스의 CSS 들을 주입할 수 있음.\(상속과 흡사\)
* Math
* Loops
  * 코드중복 감
* Nesting
  * child와 parent 관계를 가지는 구조적 설계를 가능하게 한다.
* Pre-built functions
* Framework & Library
  * Preprocessor 생태계에 구성된 다른 효과적인 프로그램들과 연동할 수 있음
  * [Compass](http://compass-style.org/)
  * [Bourbon](https://www.bourbon.io/) 
* Code Optimization

### Preprocessors

* SASS
  * [Syntactically Awesome Style Sheets](https://sass-lang.com/)
* PostCSS
* Less
* Stylus

#### _References_

{% embed data="{\"url\":\"https://raygun.com/blog/10-reasons-css-preprocessor/\",\"type\":\"link\",\"title\":\"10 Reasons to Use a CSS Preprocessor in 2018 \| Raygun Blog\",\"description\":\"So, you’ve probably heard of CSS preprocessors before, be it Sass, LESS, or Stylus—they’re all great. Here\'s 10 reasons why I love them.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://raygun.com/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://raygun.com/blog/images/css-preprocessor/css-preprocessor.png\",\"width\":1024,\"height\":512,\"aspectRatio\":0.5}}" %}



