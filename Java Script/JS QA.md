JS QA

1. componentDidMount
  React DOM 렌더링
  리액트는 렌더링을 한다. 렌더링이란 무엇인가? 리액트는 브라우저에 보이는 HTML DOM 트리의 다른 버전인 리액트 돔을 갖고 있다.
  어떤 이유에서든 컴포넌트의 상태가 변하면 리액트돔은 이를 감지하고 변경된 부분의 html을 바꿔준다. html이 업데이트되면 우리는 변경된 결과를 눈으로 확인할 수 있다.
  이를 렌더링이라고 한다.

  마운팅
  렌더링이 맨 처음 일어나는 순간, 즉 리액트돔 트리가 존재하지 않는 상태에서 리액트가 처음으로 각 컴포넌트의 render() 함수를 콜해 자신의 돔 트리를 구성하는 과정을 마운팅이라고 한다.
  마운팅 과정에서 생성자와 render() 함수를 부르는데 마운팅을 마친 후 바로 부르는 함수가 하나 더 있다.

  componentDidMount하는 함수다. 우리는 컴포넌트가 렌더링되자마자 API 콜을 하고 그 결과를 리스트로 보여주려고 componentDidMount 함수에 백엔드 API 콜 부분을 구현해야한다.

# 각 Component의 A.constructor B.render 를 호출하여 DOM 트리를 구성하는 과정... 마운팅!
# 마운팅을 마친 후 바로 부르는 함수를 C. componentDidMount


2. fetch
  Promise
  A. pending B. reject C. 



3. HTTP 파이프라인이란 무엇인가?