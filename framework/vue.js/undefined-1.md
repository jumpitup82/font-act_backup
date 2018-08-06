# 비교

## VS React

#### 사용 언어

* Vue는 es5 ~
* React는 es2015\(es6\) ~

#### 공통점

* Virtual DOM 사용
* 반응적이고 조합 가능한 컴포넌트 사용
* 코어 라이브러리에만 집중하고 나머지\(Router, State management 등\)는 자유롭게 선택 

#### 렌더링 성능

* 필요한 DOM 조작 수 최소화를 목표로 하며 두 Framework가 동일
* DOM 조작에는 가능한 적은 오버헤드만 가해져야 하는데 snabbdom 기반의 Vue가 우세 

#### 갱신 성능

* React 는 컴포넌트의 상태가 변경되면 기본적으로 해당 컴포넌트 루트로부터 시작하여 전체 하위트리를 다시 렌더링 하며 이를 피하려면 shouldComponentUpdate를 직접 구현하고 변경 불가능한 데이터 구조 사용.
* Vue에서  컴포넌트의 종속성은 렌더링 중 자동으로 추적 

#### HTML

* React는 XML유사구문인 JSX문법 사용
* Vue는 HTML 템플릿 확장



## VS Angular \(Angular 2\)

#### 사용언어

* typescript

#### 런타임 퍼포먼스

* 유의미한 차이 없음

#### 용량

* Vue \(~30kb gzipped\)
* Angular \( ~130kb gzipped\)

#### 유연성

* Vue는 덜 강요적 - 코어 렌더링 라이브러리에서 원하는 기능 확장
* Angular는 많은 기능과 모듈 내포

#### 러닝커브

* 시작하기에 Vue가 상대적으로 쉽다
* Angular는 대규모 어플리케이션을 목표로 하기 때문에 생산성이 올라가기전 많은 것들을 알아야함

#### _References_

{% embed data="{\"url\":\"https://medium.com/javascript-in-plain-english/i-created-the-exact-same-app-in-react-and-vue-here-are-the-differences-e9a1ae8077fd\",\"type\":\"link\",\"title\":\"I created the exact same app in React and Vue. Here are the differences.\",\"description\":\"React vs Vue. Finally, a side-by-side code comparison between Vue and React! 🎉\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn-images-1.medium.com/fit/c/304/304/1\*5996wmlLTse13YC42IVAWw.png\",\"width\":152,\"height\":152,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn-images-1.medium.com/max/2000/1\*mJ-qdNqldpgae2U5oS0qDg.png\",\"width\":1266,\"height\":826,\"aspectRatio\":0.6524486571879937}}" %}

