---
layout: post
title: target vs currentTarget
categories: DOM
tags: [DOM, til]
---

`이벤트 핸들러가 부착된 것이 currentTarget이다`

## target vs currentTarget

DOM element에 이벤트 핸들러를 부착할 경우 우리는 콜백함수에서 브라우저가 전달해주는 event 객체를 인자로 전달받는다.
event객체에는 target과 currentTarget이라는 프로퍼티가 있는데 그 차이점을 알아보자

### target

말 그대로 target 이다. 이벤트가 발생했을때 내가 클릭하거나 선택한 element가 나온다.

### currentTarget

currentTarget은 이벤트 핸들러가 부착된 element를 가리킨다.
이벤트 버블링을 통해 이벤트 핸들러가 부착된 element의 자식요소를 선택해도 이벤트가 동작한다
이때 target은 자식요소를 가리키겠지만 currentTarget은 이벤트 핸들러가 부착된 element가 나오게 된다.

### 결론

차이점을 알고 사용할 일이 분명히 있다!
이벤트 버블링과 캡쳐링에 대해서도 공부하면 더욱 좋을 것 같다.