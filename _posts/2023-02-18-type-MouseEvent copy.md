---
layout: post
title: Typescript MouseEvent 
categories: typescript
tags: [typescript, react, til]
---

`MouseEvent의 Type`

## MouseEvent

MouseEvent에는 e.target.id, value 등의 속성들의 타입이 지정되어 있지 않아서
value 등을 가져오려고 하면 typescript에서 없다고 오류를 보여준다.
이는 typescript 오류라 동작하는데 문제는 없지만 코드에 빨간줄이 그어져 있는 모습을 참을 수 있는 개발자는 많지 않을 것이다.

### 원인 

브라우저마다 MouseEvent가 가지고 있는 속성이 달라서 typescript에서 공통적으로 만들어 놓기 어려워서 생긴 문제라고 한다.

### 해결방법

`e.currentTarget.value` 로 지정하면 오류없이 가져올 수 있다.

꼭 마우스로 핸들링해야 되는 이벤트가 아니라면 ChangeEvent를 사용하면 익숙한 target을 그대로 사용할 수 있다.