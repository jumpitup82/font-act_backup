# 계산된 속성과 감시자

## 계산된 속성

템플릿내에 로직이 많이지 표현되면서 유지보수성이 빠르게 감소

```javascript
<div id="example">
  {{ message.split('').reverse().join('') }}
</div>
```

이러한 단점을 보완하기 위해 계산된 속성\(computed\)을 이용.

```markup
<div>
  <p>원본 메시지: "{{ message }}"</p>
  <p>뒤집히도록 계산된 메시지: "{{ reversedMessage }}"</p>
</div>
```

```javascript
var vm = new Vue({
  data: {
    message: '안녕하세요'
  },
  computed: {
    reversedMessage: function () {
      return this.message.split('').reverse().join('')
    }
  }
})
```

## 계산된 속성과 Method의 차이

표현식에 메소드를 사용하여 같은 결과를 얻을 수 있음.

```javascript
var vm = new Vue({
  data: {
    message: '안녕하세요'
  },
  methods: {
  reversedMessage: function () {
    return this.message.split('').reverse().join('')
  }
})
```

최종 출력은 계산된 속성과 메소드 둘다 같은 결과.  
하지만 **계산된 속성은 종속성에 따라 캐시처리.** 계산된 속성은 종속성 중 일부가 변경된 경우에만 다시 계산됨.

하지만 반응형 종속성을 가지지 않는 코드의 경우 계산된 속성이 정상동작하지 않음.

```javascript
computed: {
  now: function () {
    // Data.now() 는 반응형 종속성을 가지지 않음.
    return Date.now()
  }
}
```

## 감시자

* 데이터 변경에 반응하는 방법을 watch 옵션을 통해 제공.
* **대부분의 경우 계산된 속성을 사용하는 것이 유리**
* 아래와 같이 **동기식 혹은 시간이 많이 소요되는 조작을 수행하려는 경우 유용**

```markup
<div>
  <p>
    yes/no 질문을 물어보세요:
    <input v-model="question">
  </p>
  <p>{{ answer }}</p>
</div>
```

```javascript
new Vue({
  data: {
    question: '',
    answer: '질문을 하기 전까지는 대답할 수 없습니다.'
  },
  watch: {
    // 질문이 변경될 때 마다 이 기능이 실행됩니다.
    question: function (newQuestion) {
      this.answer = '입력을 기다리는 중...'
      this.getAnswer()
    }
  },
  methods: {
    getAnswer: _.debounce(
      function () {
        if (this.question.indexOf('?') === -1) {
          this.answer = '질문에는 일반적으로 물음표가 포함 됩니다. ;-)'
          return
        }
        this.answer = '생각중...'
        var vm = this
        axios.get('https://yesno.wtf/api')
          .then(function (response) {
            vm.answer = _.capitalize(response.data.answer)
          })
          .catch(function (error) {
            vm.answer = '에러! API 요청에 오류가 있습니다. ' + error
          })
      },
      500
    )
  }
})
```

