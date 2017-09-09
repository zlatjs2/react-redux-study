# 프알못 오전 스터디

`creact-react-app`으로 만들어보기

## redux, redux-saga

참고 영상
 https://www.youtube.com/watch?v=Bq_Hkj-G-4c

### redux란?
- 어플리케이션의 클라이언트 쪽 `state`를 관리하기 위한 거대한 이벤트 루프
- 클라이언트 앱의 복잡성을 제어하기 위한 하나의 `state` 제어 수단(방법론)
- 클라이언트의 종합적은 `state`를 관리하기 위한 아키텍쳐 방법론
- 액션이벤트를 발생시켜서 리듀서라는 이벤트에 대한 반응을 일으키므로 어플리케이션의 state를 a라는 상태에서 b라는 상태로 만든다.

#### Redux의 원리
- 어플리케이션의 전체에는 store라는 커다란 하나의 state가 존재하고 이것이 어플리케이션의 state를 총괄한다.
- store의 state는 그 자체를 직접 변형할 수 없고, 오직 순수 함수인 리듀서로만 새로운 형태로 갈아치우는 것이 가능
- 리듀서는 type과 payloads를 속성으로 갖는 단순 객체인 `action` 이벤트가 발생했을 때에만 작동하며, `action` 이벤트를 발생시키는 방법은 dispatch라는 함수에 단순 객체인 action을 넣는 것으로 가능하게 함

```
dispatch(action) > 리듀서 작동 > store의 state 변경 > 변경된 state가 state를 subscribe하고 있는 컴포넌트에 전달
```
- 장점
  - state의 변화가 예측가능하게 변함 = 어떠한 액션 이벤트로 부터 변경된 것인지 알 수 있다.
  - time travel degugging이 가능해진다.
  - 순수 함수(외부에 영향을 끼치지 않는 함수, api calling이 없는 함수)이기때문에 test코드를 짤 수 있다.
  - 선언적으로 프로그래밍을 할 수 있다.

#### Redux와 Middleware   
이건 패스


### redux-saga란?
- 리액트/리덕스 애플리케이션의 사이드 이펙트, 예를 들면 데이터 fetching이나 브라우저 캐시에 접근하는 순수하지 않은 비동기 동작들을, 더 쉽고 좋게 만드는 것을 목적으로하는 라이브러리

- redux-saga는 redux 구조에서 ‘비동기 동작’을 수행할 때 운영체제의 프로세스 관리와 같이 비동기 동작을 관리하기 위한 미들웨어

참고

https://redux-saga.js.org/docs/introduction/BeginnerTutorial.html

https://github.com/reactkr/learn-react-in-korean/blob/master/translated/deal-with-async-process-by-redux-saga.md
