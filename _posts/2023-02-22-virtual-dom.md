---
layout: post
title: Virtual DOM
categories: react
tags: [react, DOM, virtual, til]
---

`꼭 Dom이 느리다고 할 수는 없다.`

## Virtual Dom

말그대로 가상의 DOM(Document Object Model)이다.
가상의 문서 객체 모델이며, 실제 DOM 내용에 기반하여 만들어진다.

### 왜 사용하나?

실제 DOM 에는 브라우저가 화면을 그리는데 필요한 모든 정보가 들어있어 실제 DOM을 조작하는 작업이 무겁다.

만약 작고 정적인 웹이라면 일반 DOM이 성능이 더 좋을 수 있다.
하지만 복잡한 대규모 SPA에서는 DOM조작이 빈번하게 일어나므로 Virtual DOM을 사용하는 것이 효과적이다.

### Virtual DOM의 처리 과정

실제 DOM에 접근하는 대신, 이를 추상화한 자바스크립트 객체를 구성하며 메모리에 저장하고 변경된 부분만 찾아서 해당 부분만 변경한다.
이 과정에서 diff 알고리즘을 사용하는데 이는 추후에 알아보자.

실제 DOM은 변경시 전체 DOM을 렌더링한다.
하지만 리액트에서 Virtual DOM 은 diff알고리즘을 사용하여 상태나, UI가 변경되는 부분만 찾아서 변경한다.
이는 콘솔창을 열어서 확인해 볼 수 있다. 변경되는 element부분만 깜빡깜빡 거릴 것이다.

