---
layout: post
title: autofocus 속성의 문제점
categories: HTML
tags: []
---

`리렌더시 focus가 잡히지 않는다.`

## autofocus

이 속성은 html global attributes로 boolean값을 가지고 있는데, element에 이 속성을 전달하면
페이지가 로드 되었을 때 해당 엘리먼트로 focus를 잡아준다.

### 문제

autofocus는 처음 페이지가 로드될 때만 동작하고 리렌더시 동작하지 않는다.

### 해결방법

리렌더시 함수나 다른 방법으로 포커스를 따로 주어야 원하는 곳에 focus를 전달할 수 있다.