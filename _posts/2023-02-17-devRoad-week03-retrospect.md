---
layout: post
title: 데브로드 프론트엔드 서바이벌 3주차 주간회고
categories: 주간회고
tags: [devroad, frontend]
---

`프론트엔드 서바이벌 시작 후 가장 큰 소득이 있었다.`

## 주간 회고

아직도 데브노트가 어렵다. 그래도 이번주를 기반으로 다시 어떻게 적어야 될지 정할 수 있었다.
매주 키워드가 주어지면 각 키워드에 대해 이해가 된 부분과 안된 부분을 나눠서 정리하고자 한다.
키워드에 대한 공부를 하면서 관련된 부분들도 같이 정리하고 학습해야 한다.
또 이해가 안된 부분들은 적어두고 반드시 나중에 다시 학습하거나 이해했을 때 수정해야 한다.
나만 데브노트를 어려워하는 것인지 궁금하긴 하다.
하지만 그것보다 내가 더 성장할 수 있는 것이 중요하기 때문에 계속 적극적으로 부딪치면서 좋은 방향으로 학습해 나가자!

### 강의

아샬님의 컴포넌트와 함수 쪼개기가 굉장히 인상적이였다.
덕분에 코드를 작성하는 부분에서 기존에 내가 생각하던 코드 작성 방식과는 다른 방법들이 보이기 시작했다.
그래서 이것이 `Thinking in React`인가 싶었다.

### 과제

강의에서 진행한 내용을 기반으로 비슷한 작업을 수행하는 것이 과제였다.
선언형으로 작성하는 부분들은 가독성도 좋고 코드가 깔끔해보여 처음으로 스스로의 코드에 조금이나마 만족감이 들었던 것 같기도 하다.
기존의 나라면 명령형의 코드들을 주구장창 적었을 것이 분명하다.
하지만 처음 main.tsx 에서 App 컴포넌트를 렌더하는 부분을 작성할 때 검색해보지 않고 하지 못했다.
아직 이정도도 머릿속에 없다고 생각하자 내 현 위치가 더 뼈저리게 느껴졌고 더 달려야 된다고 생각했다.

두고두고 보면서 잊지 말자

- dom element를 가져와 
- ReactDom을 사용하여 root를 생성
- 그리고 나서 렌더해주면 된다.

```jsx
import ReactDOM from 'react-dom/client';

import App from './App';

function main() {
  // TODO: App 컴포넌트를 render 해주세요.
  const container = document.getElementById('root');
  if (!container) return;

  const root = ReactDOM.createRoot(container);
  root.render(<App />);
}

main();
```

### 잘한 것은 무엇인가?

- 많은 시간 앉아있었고 많은 시간 공부했다고 생각한다.
  - 양보다 질이 중요하지만, 양을 채워야 질이 좋아질 수 있다.
- 해야되는 것을 체크리스트로 만들고 하다가 부족하거나 더 공부를 해야하는 부분들을 지속적으로 정리했다.
  - 해야할 것들이 점점 늘어갔지만, 그것은 내가 부족하다는 것이고 할 것이 많아져서 더 많은 시간을 투자할 수 있었다.
- TIL을 작성해 보았다. 사실 과거에 한번 시도해 보긴 했는데 하루에 공부를 하고 한 것을 다시 정리하여 매일 올리는 것은 꽤나 힘든 일이였다.
그래서 미뤄두고 있었는 데 이번에 다시 시작했다.
  - 하루에 공부한 것을 모두 정리하는 것보다 개념별로 한가지씩이라도 정리해서 올리려고 한다.
  - [useRef](https://yodoree.github.io/react/2023/02/16/useRef.html)에 대한 학습 및 정리
- 데브로드 시작하면서 나만의 환경설정을 꾸준히 세팅하기로 마음먹었다.
  - 이번주에 레포를 만들어 아샬님이 최신 리액트 세팅을 참고해서 작성해보았다.
  - 사실 거의 비슷해서 그대로 옮겨놓은 수준이지만 하나하나 어떤것에 필요한지 정확하게 이해하고자 했다.
  - [나만의 환경설정 레포](https://github.com/yodoree/environment-configuration)

### 이번주 할일과 추가된 할 일

- [ ] 깃헙블로그 seo 설정
- [ ] Thinking in React 읽기
- [ ] 3주차 주간회고
- [ ] VirtualDom
- [ ] Reconciliation
- [ ] 프레임워크 없는 프론트엔드 개발 책 보기
- [ ] Todolist v4
- [ ] MVC 디자인패턴
- [ ] Type MouseEvent ->  event.target을 찾을 수 없음
- [ ] 3주차 과제 리팩토링
- ✅ 3주차 과제
- ✅ useRef
- ✅ Todolist v3
- ✅ 최신 환경 설정
- ✅ 데브노트 정리

귀찮다고 시작하지 못한 부분들이 있지만 그래도 차근차근 하나씩 해나가고 있고 계속 적어두면서 시간이 될때마다 해결할 것이다.

### 잘못한 것은 무엇인가?

- 데브노트를 정리하면서 모르는 개념들에 대해 더 시간을 투자해서 이해하지 않고 그냥 적어둔 부분들이 거슬린다.
- 반드시 다 머리속에 집어넣을 것이다.

### 무엇을 배웟는가?

- 스스로 학습하는 법
  - 항상 누군가가 정해준 것만 해결하면 만사 ok 였던 성격을 고치기보다 스스로 할 것을 많이 부여하기로 했다. 
  - 학습해야겠다고 느껴지면 '나중에 하자' 하고 넘겼던 부분들을 적어두기 시작했고 바로바로 하진 않지만 하나씩 해나가고 있다.
- 컴포넌트, 함수 쪼개기
  - 아직 단일 책임, 재사용 가능하게 만들기 등은 생각하면서 만들기가 조금 어렵다.
  - 그치만 일단 쪼개보기로 했다. 많은 양을 쪼개다보면 조금씩 보일 것이라고 생각한다.

### 다음주 해결해야 할 것들

- [ ] 깃헙블로그 seo 설정
- [ ] Thinking in React 읽기
- [ ] 3주차 주간회고
- [ ] VirtualDom
- [ ] Reconciliation
- [ ] 프레임워크 없는 프론트엔드 개발 책 보기
- [ ] Todolist v4
- [ ] MVC 디자인패턴
- [ ] autofocus 속성은 페이지가 처음 로드될때만 적용되는 속성이다.
- [ ] Type MouseEvent -> event.target을 찾을 수 없음
- [ ] 3주차 과제 리팩토링

비록 다 하진 못하겠지만 최소 이번주처럼 학습하고 하나씩 천천히 해결해 나가자

### 정리

아직 많이 부족하지만 그래도 많은 것을 얻은 주간이였다.
스스로 학습할 수 있는 방법을 얻은 것이 가장 큰 소득이였다.
나의 개발자 인생에 있어 끝까지 가지고 갈 좋은 습관들을 만들 기회다.
나태해지지 말고 돌아가지 말고 천천히 직진해보자.