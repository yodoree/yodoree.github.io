---
layout: post
title: 데브로드 프론트엔드 서바이벌 4주차 주간회고
categories: 주간회고
tags: [devroad, frontend, twil, react]
---

`데브노트는 아직도 깊이가 부족하다.`

## 주간 회고

아직 부족하나 데브노트 작성이 전보다는 두렵지 않다.
나의 시간과 지식등이 허락하는 한 최선을 다해 적으면 된다고 생각한다.
비록 최선과는 거리가 조금 있었지만 그래도 차선정도는 작성한 것 같다.
만족하진 않지만 또 한 스텝 밟았다고 생각하고 다음 스텝을 밟으려고 노력해야겠다.

### 강의

약간의 백엔드관련 강의와 React Hooks에 관한 강의가 있던 한주였다.
hook에 관련해서 집중적으로 공부할 수 있던 시간이였다. 

### 과제

3주차 과제에 백엔드를 붙이고 localstorage를 사용해 키오스크처럼 만드는 것이 과제였다.
백엔드 부분은 간단한 작업이라 딱히 어려울 건 없었다.
3주차 부분도 다시 만들라는 주문에 지난주에 했던 기억을 떠올리며 작업을 했지만
막히는 부분이 있어 다시 보고 복붙을 하기도 했다.
특히 category를 모아서 보기위해 reduce를 사용하는 부분은
내가 reduce에 대한 이해도가 확실하지 않은 건지 reduce 함수 자체가 가독성이 낮은 건지 모르겠다.
볼때마다 새로워서 사용하기가 싫지만 뭔가 써야될때가 있는 느낌이라 더 많이 사용해서 일단 익숙하게 만들어놔야겠다.

```ts
export default function selectCategory(
  restaurantsData: Restaurant[],
) : string[] {
  return restaurantsData.reduce((acc: string[], restaurant: Restaurant) => {
    const { category } = restaurant;
    return acc.includes(category) ? acc : [...acc, category];
  }, []);
}
```

또 useLocalstorage라는 hook을 사용해봣는데 원래 localstorage를 사용하면 어디서든 get해올 수 있는데
hook을 사용하면 state처럼 내려줘야 사용 가능해서 조금 불편하게 느껴졌다.

과제의 테스트를 다 통과하긴 했지만 답안을 보니 아직 내 코드에 리팩토링할 부분들이 많이 보였고
다음주중에 다시 만들어볼 생각이다.

### 잘한 것은 무엇인가?

- TIL이 많이 늘어나기 시작했다.
  - 블로그로 정리하는 맛이 쏠쏠하고 내 블로그를 더 풍족하게 만들고 싶다는 마음이 들었다.

### 이번주 할일과 추가된 할 일

- [ ] 깃헙블로그 seo 설정
- [ ] 프레임워크 없는 프론트엔드 개발  책 보기
- [ ] Todolist v4
- [ ] https://overreacted.io/ko/a-complete-guide-to-useeffect/ 읽기
- [ ] MVC 디자인패턴
- [ ] URI
- [ ] 프로토콜
- [ ] 도메인
- [ ] Put vs Patch
- [ ] promise
- [ ] stream api
- [ ] 4주차 과제 리팩토링
- [✅] 4주차 주간회고
- [✅] 4주차 과제
- [✅] Reconciliation
- [✅] target vs currentTarget
- [✅] VirtualDom
- [✅] Thinking in React 읽기
- [✅] 3주차 과제 리팩토링
- [✅] 리액트 라이프사이클
- [✅] 4주차 데브노트 정리
- [✅] autofocus 속성은 페이지가 처음 로드될때만 적용되는 속성이다.
- [✅] Type MouseEvent ->  event.target을 찾을 수 없음

### 잘못한 것은 무엇인가?

- 할 것도 많이 늘었고 한 것도 많이 늘었지만 속마음을 들여다보면 귀찮다고 넘긴 것들도 너무 많았다.
- 이정도면 되겠지 라는 마음으로 넘긴 공부들이 있다.

### 무엇을 배웟는가?

- 아직도 현재에 안주하고자 하는 마음이 가득하다. 스스로를 쫒기게 만들어야 한다.

### 다음주 해결해야 할 것들

- [ ] 깃헙블로그 seo 설정
- [ ] 프레임워크 없는 프론트엔드 개발  책 보기
- [ ] Todolist v4
- [ ] https://overreacted.io/ko/a-complete-guide-to-useeffect/ 읽기
- [ ] MVC 디자인패턴
- [ ] URI
- [ ] 프로토콜
- [ ] 도메인
- [ ] Put vs Patch
- [ ] promise
- [ ] stream api
- [ ] 4주차 과제 리팩토링

다 하려고 하기보단 귀찮다고 넘기지 말자!

### 정리

매주 아직 부족하다고 적을 것 같다.
하지만 언젠가 누가봐도 만족스럽게 했다고 느낄만큼을 할때까지 달릴 것이다.
모르는 것보다 공부하지 않고, 물어보지 않는 것이 부끄러운 것이다.
거침없이 물어보고 공부하도록 해야겠다.
