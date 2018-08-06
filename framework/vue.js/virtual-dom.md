# Virtual DOM

## 특징

* DOM을 추상화한 개념으로 DOM의 복사본을 메모리에 저장 
* DOM 조작을 최소화 하여 성능 향상에 기여 
* 실제 Virtual DOM을 사용하는 경우 성능이 더 느리지만 DOM 조작이 빈번한 단일 페이지 어플리케이션 에서는 대부분 충분히 빠르게 동작한다 

## 브라우저의 동작

![](../../.gitbook/assets/wvbwscn7oadykroobdd3.png)

### References

{% embed data="{\"url\":\"https://hashnode.com/post/the-one-thing-that-no-one-properly-explains-about-react-why-virtual-dom-cisczhfj41bmssp53mvfwmgrq\",\"type\":\"link\",\"title\":\"The one thing that no one properly explains about React — Why Virtual DOM - Hashnode\",\"description\":\"The other day a friend had this React question for me: “Composition through components, one way data binding; I understand all that, but why Virtual DOM?”. I’ve given him the usual answer. \\\"Because, direct DOM manipulation is inefficient, and slow.\\\" ...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://hashnode.com/static/images/favs/apple-touch-icon.png\",\"width\":180,\"height\":180,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn.hashnode.com/res/hashnode/image/upload/w\_800,h\_600,c\_thumb/sklcdp92gqaxbdo97533/1472289870.png\",\"width\":800,\"height\":600,\"aspectRatio\":0.75}}" %}

{% embed data="{\"url\":\"https://velopert.com/3236\",\"type\":\"link\",\"title\":\"\[번역\] 리액트에 대해서 그 누구도 제대로 설명하기 어려운 것  – 왜 Virtual DOM 인가? \| VELOPERT.LOG\",\"description\":\"리액트를 지난 2년간 사용하면서도 막상 말끔하게 설명하라고 하면 어려웠던 주제, 원래 번역글은 잘 안쓰지만 글 자체가 구성이 잘 되어있어서 글을 번역해보았습니다. 원본: https://hashnode.com/post/the-one-thing-that-no-one-properly\",\"icon\":{\"type\":\"icon\",\"url\":\"https://velopert.com/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://velopert.com/wp-content/uploads/2017/03/wvbwscn7oadykroobdd3.png\",\"width\":624,\"height\":289,\"aspectRatio\":0.46314102564102566}}" %}

