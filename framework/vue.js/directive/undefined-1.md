# 전달인자와 수식어

### 전달인자

콜론\( : \)으로 표시 되며 directive 처리자에 전달되는 데이

```markup
<a v-bind:href="url"> ... </a>
<a v-on:click="doSomething"> ... </a>
```

위의 예에서 href와 click이 전달인자 이다.



### 수식어

점\( . \) 으로 표시되는 특수 접미사로 디렉티브를 특별한 방법으로 바인딩 해야함을 표현.

```markup
<button v-on:click.stop="onClick"> ... </button>
```

위 예제에서 **stop** 이 수식어이며 **event.stopPropagation\(\)**을 호출하도록 디렉티브에 알려준다. 

