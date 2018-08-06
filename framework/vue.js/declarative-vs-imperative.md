# Declarative vs Imperative

## 선언적 렌더링 {#undefined-1}

```markup
<div id="app">  
    {{ message }}
</div>
```

```javascript
var app = new Vue({  
    el: '#app',  
    data: {
        message: '안녕하세요 Vue!'  
        }
    }
);
```

## 명령적 프로그래밍

* 어떻게 할 것인가에 관심 
* 절차적

```javascript
<div>
    <div id="message"/>
    <button id="btn">Hello</button>
</div>

<script>
    $('#btn').click(function() {
        $('#message').innerHTML = 'Hello!!';
    });
</script>
```

## 선언적 프로그래밍

* 무엇을 할 것인가에 관심 
* 인터페이스 식별에 용이 

```javascript
<div id="app">
    <div>{{ message }}</div>
    <button @click="onButtonClick">Hello</button>
</div>

<script>
    new Vue({
        el: '#app',
        data: {
            message: '',
        },
        methods: {
            onButtonClick () {
                this.message = 'Hello';
            }
        }
    });
</script>
```

### References

{% embed data="{\"url\":\"https://codeburst.io/declarative-vs-imperative-programming-a8a7c93d9ad2\",\"type\":\"link\",\"title\":\"Declarative vs Imperative Programming\",\"description\":\"Or wrong ways I was thinking about React\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn-images-1.medium.com/fit/c/304/304/1\*mNmxddJJTzkiBfK77mWuGA.png\",\"width\":152,\"height\":152,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn-images-1.medium.com/max/2000/1\*46\_mippZl0SdzGjMBH-oJA.jpeg\",\"width\":2000,\"height\":1329,\"aspectRatio\":0.6645}}" %}

