---
layout: post
title: React Reconciliation
categories: react
tags: [react, reconciliation, diff, til]
---

[공식문서](https://ko.reactjs.org/docs/reconciliation.html)

## Reconciliation

재조정, 즉 리액트에서 상태나 UI 등이 변화할 때 diff 알고리즘을 사용하여 DOM과 Virtual Dom의 루트 엘리먼트 부터 비교한다.
비교해서 다른 부분들은 DOM 트리에서 제거되고 새로운 DOM 노드들이 추가 된다.
가장 중요한 부분은 변경된 부분만을 건드린다는 것이다.
