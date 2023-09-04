---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
transition: slide-left
title: Welcome to Slidev
---
# Vue와 React: 웹 개발을 위한 첫 단계

Presentation slides for developers
<common-slide/>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---

# What is vue?

Vue.js는 웹 인터페이스를 구축하기 위한 프로그레시브 프레임워크입니다. 중요한 특징 중 하나는 점진적으로 채택할 수 있다는 것으로, 핵심 라이브러리는 뷰 중심의 애플리케이션에 초점을 맞추지만, 현대적인 도구 및 지원하는 라이브러리와 함께 사용하면 복잡한 싱글 페이지 애플리케이션을 쉽게 구축할 수 있습니다.

### history
- 2013년: Evan You가 Vue.js를 처음으로 공개합니다. 그는 이전에 AngularJS 프로젝트에서 일했으며, Angular의 개념을 더 간단하게 만들려는 목적으로 Vue를 개발하게 되었습니다.
- 2016년: Vue 2.0이 발표되었으며, 이 버전에서는 가상 DOM, 서버 사이드 렌더링 등의 주요 기능이 도입되었습니다.
- 2020년: Vue 3.0이 발표되었으며, Composition API, 가상 DOM의 개선, TypeScript의 향상된 지원 등 다양한 새로운 기능과 최적화가 이루어졌습니다.

<br>

<common-slide/>


---
transition: fade-out
---
<!--
Here is another comment.
-->

# vue2.0의 지원 종료와 그 의미 

### Vue 2.0의 지원 종료:
- Vue 2.0의 공식 지원 종료는 Vue 3.0의 안정적인 출시와 함께 시작됩니다. 이는 개발자 커뮤니티에게 Vue 3.0의 새로운 기능과 최적화를 채택하도록 권장하는 것을 의미합니다.
- 지원 종료는 보안 패치 및 버그 수정이 더 이상 제공되지 않는다는 것을 의미합니다. 따라서, 기존의 Vue 2.0 프로젝트는 시간이 지남에 따라 보안 및 안정성 문제에 직면할 수 있습니다.

### 지원 종료의 의미 
- 업그레이드의 필요성: Vue 2.0을 사용하는 프로젝트를 유지 및 운영하는 개발자나 팀은 점차 Vue 3.0으로 마이그레이션을 고려해야 합니다.
- 새로운 기능: Vue 3.0은 **Composition API**, 더 나은 성능, 트리 쉐이킹 지원 등 많은 새로운 기능과 개선 사항을 제공합니다.
- Vue3.0의 가장 중요한 기능 일부를 최신 마이너 버전인 2.7에서 사용할 수 있게 백포트 했습니다. 하지만 모든 기능을 지원하지 않고 앞으로 업데이트 예정도 없습니다.
https://v2.vuejs.org/v2/guide/migration-vue-2-7
<common-slide/>
---
transition: fade-out
---

# Vue 3.0으로의 마이그레이션 이점
Vue 3.0은 Vue 2.0보다 많은 특징과 개선 사항을 제공하므로, 이를 활용하여 프로젝트의 품질과 성능을 향상시킬 수 있습니다.

- Composition API: Vue 3.0의 가장 큰 변화 중 하나는 Composition API를 도입한 것입니다. 이를 통해 개발자들은 코드의 재사용성과 가독성을 더욱 향상시킬 수 있습니다.

- 성능 향상: Vue 3.0은 더 나은 성능을 제공합니다. 이는 더 빠른 렌더링 시간과 효율적인 메모리 사용 덕분입니다.

- 트리 쉐이킹 지원: Vue 3.0은 트리 쉐이킹을 지원하여 불필요한 코드를 제거하는 것을 도와줍니다. 이는 최종 번들의 크기를 줄여주어 웹사이트의 로딩 속도를 개선할 수 있습니다.
<common-slide/>
---
transition: fade-out
---


# Vue2.0에서 3.0으로의 전환 

## CompositionAPI
- Vue 3.0의 가장 큰 변화 중 하나는 Composition API의 도입입니다.
- 이전의 Options API는 컴포넌트의 로직을 옵션 별로 분리했지만, Composition API는 기능 별로 로직을 재사용하고 구성할 수 있게 해줍니다.
- 이로 인해 컴포넌트의 가독성과 재사용성이 향상되었습니다.

<common-slide/>
---
transition: fade-out
---

# 기존 Optional API와의 비교 
<br>
<img src = "https://velog.velcdn.com/images/buddle6091/post/a82ee5b3-8c6d-4a06-bacd-fb49d8b10f5c/image.png"  style="width: 80%; height:80%;">


<br>
<common-slide/>

---
transition: fade-out
---

# 기존 Optional API와의 비교 
<br>
### Composition API와 재사용성
Composition API는 Vue 3에서 도입된 새로운 API로, 복잡한 컴포넌트 로직을 쉽게 구성하고 재사용할 수 있게 해줍니다.

- 문제점:
기존 Option API의 mixins는 로직 재사용의 한 방법이었지만, 여러 가지 문제점이 있었습니다. 예를 들면, 충돌 위험, 출처가 불명확한 속성 등이 있습니다.
- 해결:
Composition API는 reactive와 ref를 사용하여 반응성 있는 데이터를 만들고, setup() 함수 내에서 로직을 구성하여 문제점을 해결합니다.
커스텀 훅을 쉽게 만들어 로직을 재사용할 수 있습니다.

<br>
<common-slide/>

---
transition: fade-out
---

# 기존 Optional API와의 비교 

### Mixin 사용법
```
const myMixin = {
  data() {
    return {
      message: "Hello from mixin!"
    };
  },
  created() {
    console.log(this.message);
  }
};
```
### Mixin 사용하기
```
new Vue({
  mixins: [myMixin],
  created() {
    console.log('Component created!');
  }
})
```
#### 출력 
```
Hello from mixin!
Component created!
```

<br>
<common-slide/>

---
transition: fade-out
---

# 기존 Optional API와의 비교 

### Mixin 의 속성충돌

```
new Vue({
  mixins: [myMixin],
  data() {
    return {
      message: "Hello from component!"
    };
  },
  created() {
    console.log(this.message);
  }
}).$mount("#app");
```
을 실행하면 
```
Hello from component!
Hello from component!
```
- 두 개의 created 훅이 모두 실행되지만, message 데이터 속성의 값은 컴포넌트의 것이 mixin의 것보다 우선적으로 사용됩니다. 따라서 "Hello from component!"가 두 번 출력됩니다.
<br>
<common-slide/>

---
transition: fade-out
---

# 기존 Optional API와의 비교 
<br>
 ### 본격적인 타입 추론
Vue 3는 Typescript와의 호환성을 크게 향상시켰습니다.
Options API의 경우에도 타입스크립트 특유의 타입 추론을 구현하기 위해 매우 [비효율적인 방법](https://github.com/vuejs/core/blob/44b95276f5c086e1d88fa3c686a5f39eb5bb7821/packages/runtime-core/src/componentPublicInstance.ts#L132-L165)을 사용하고 있다고 공식 문서에서는 설명하고 있습니다.

  - 특징:
    Composition API는 타입 추론을 자동화하기 위한 구조를 가지고 있습니다.
    Vue 3의 내부 코드도 Typescript로 작성되었기 때문에, Typescript와의 통합이 더욱 원활해졌습니다.

### 더 작은 생산 번들 및 더 적은 오버헤드
- Vue 3는 `<script setup>` 태그를 도입하여 컴포넌트 로직을 더 간결하게 작성할 수 있게 되었습니다.

- 특징:
`<script setup>`을 사용하면, 컴포넌트의 템플릿이 코드와 동일한 범위에서 인라인 함수로 컴파일됩니다.
이로 인해, 기존 Option API에서 this를 사용하여 데이터에 접근하는 것을 줄일 수 있습니다.
변수 이름이 안전하게 단축될 수 있으므로, 번들 크기가 줄어들고, 더 나은 성능을 제공합니다.

<br>
<common-slide/>

---
transition: fade-out
---

# What is React?

React는 사용자 인터페이스를 구축하기 위한 JavaScript 라이브러리입니다. 주요 특징은 컴포넌트 기반 아키텍처와 가상 DOM을 사용하여 효율적인 업데이트와 렌더링을 제공한다는 것입니다.


### history
- 2013년: Facebook에서 React를 공개합니다. 원래는 Facebook의 뉴스 피드에 대한 상호 작용성 향상을 목적으로 개발되었습니다.
- 2015년: React Native가 발표되어 모바일 애플리케이션 개발에도 React를 사용할 수 있게 되었습니다.
- 2017년: React 16 (React Fiber)가 발표되었으며, 이 버전에서는 코어 알고리즘의 완전한 재작성이 이루어졌습니다.
- 2019년: Hooks가 도입되어 함수 컴포넌트에서도 상태 관리와 생명주기 메서드를 사용할 수 있게 되었습니다.

<br>
<common-slide/>

---
transition: fade-out
---

# 리액트의 주요특징
<br>

- 컴포넌트 기반 아키텍처: React는 모든 것을 컴포넌트로 보고, 이 컴포넌트들을 조합하여 사용자 인터페이스를 구축합니다. 이는 코드의 재사용성을 높이고, 가독성을 증가시키며, 유지 보수를 쉽게 해줍니다.

- 가상 DOM: React는 '가상 DOM'이라는 개념을 도입하여 브라우저에 렌더링하는 과정을 최적화합니다. 이를 통해, 사용자 인터페이스가 효율적으로 업데이트됩니다.

- 단방향 데이터 흐름: React는 데이터가 위에서 아래로 (부모에서 자식으로) 흐르는 단방향 데이터 흐름을 따릅니다. 이는 애플리케이션 상태를 쉽게 추적하고 이해하는데 도움이 됩니다.

- JSX: React는 JavaScript XML(JSX)이라는 문법을 사용합니다. JSX는 JavaScript 내에서 HTML을 작성할 수 있게 해주는 문법입니다. 이를 통해 개발자는 UI 구조와 동작을 한 곳에서 관리할 수 있습니다.

<br>
<common-slide/>

---
transition: fade-out
---

# React 기초 개념 

### jsx
JSX는 JavaScript XML의 줄임말로, React요소를 생성하는 JavaScript의 구문 확장입니다. JavaScript내에서 HTML과 같은 마크업 문법을 사용할 수 있게 해주며, UI 구조와 관련된 로직을 하나의 공간에서 처리할 수 있게 도와줍니다.
```
// html 
<body>
  <script src="script.js"></script> 
</body>
// js
const element = document.createElement("h1");
element.textContent = "Hello, world!";

//jsx
const element = <h1>Hello, world!</h1>;
```

<br>
<br>
<common-slide/>

---
transition: fade-out
---

# React 기초 개념 

### 컴포넌트와 Props
- 컴포넌트 
React는 UI를 독립적이고 재사용 가능한 작은 부분들인 "컴포넌트"로 나누어 관리합니다. 컴포넌트는 JavaScript 함수나 클래스로 표현되며, React 요소를 반환합니다. 간단한 컴포넌트는 다음과 같습니다

```
// Welcome이라는 컴포넌트 정의
const Welcome = (props) => {
  return <h1>Hello, {props.name}</h1>;
}

// 컴포넌트 사용 
<Welcome name="React" />;
// H1 태그를 사용하여 Hello, React를 출력 
```

<br>
<common-slide/>

---
transition: fade-out
---

# React 기초 개념 

### 컴포넌트와 Props
- props 
  - Props는 컴포넌트에 전달되는 데이터를 의미합니다. 컴포넌트의 재사용성을 높이며, 데이터를 통해 컴포넌트의 동작과 출력을 제어할 수 있습니다.
    - Props의 컴포넌트 재사용성에 대해 좀 더 구체적으로 설명하면 같은 컴포넌트를 다른 props로 여러 번 사용하거나, 상황에 따라 다른 컴포넌트를 렌더링하는 등의 작업이 가능합니다.

```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return (
    <div>
      <Welcome name="Sara" />
      <Welcome name="Cahal" />
      <Welcome name="Edite" />
    </div>
  );
}

```

<br>
<common-slide/>

---
transition: fade-out
---
### State 와 LifeCycle
- State
    - State는 컴포넌트에서 관리되는 데이터를 의미합니다. 이 데이터는 컴포넌트가 렌더링될 때 사용되며, 상태가 변경되면 컴포넌트는 다시 렌더링됩니다.
    - State는 컴포넌트 내에서만 접근 가능하며, **`setState`** 메서드를 통해 업데이트 될 수 있습니다.
    - State가 변경되면, 컴포넌트는 재렌더링됩니다.
```
import React, { useState } from 'react';

const Counter = () => {
  const [count, setCount] = useState(0); 
  return (
    <div>
      <p>You clicked {count} times</p>
       <button onClick={() => setCount(prevCount => prevCount + 1)}>
        Click me
      </button>
    </div>
  );
}

export default Counter;
```

<br>
<common-slide/>

---
transition: fade-out
---

# LifeCycle
- 라이프사이클은 컴포넌트가 생성되어 소멸될 때까지의 여러 단계를 설명합니다. 각 단계마다 특정 메서드가 호출되고 이러한 메서드를 라이프사이클 메서드라고 합니다.
- 마운트(Mounting):
  - constructor(): 컴포넌트가 처음 생성될 때 호출.
  - render(): 렌더링.
  - componentDidMount(): 컴포넌트가 DOM에 추가된 후에 호출. 데이터를 가져오거나 초기화하는 데 적합.
- 업데이트(Updating):
  - render(): 렌더링.
  - componentDidUpdate(): 컴포넌트가 업데이트 된 후에 호출. 상태나 속성의 변화에 대응하여 처리하는 데 사용.
- 언마운트(Unmounting):
  - componentWillUnmount(): 컴포넌트가 DOM에서 제거되기 전에 호출. 리소스를 해제하거나 정리하는 등의 작업에 사용.

<br>
<common-slide/>

---
transition: fade-out
---

# LifeCycle
- React 컴포넌트의 라이프사이클 접근 방식이 바뀌었습니다. 클래스 컴포넌트의 고전적인 라이프사이클 메서드를 대체하기 위해, Hooks가 도입되었습니다. Hooks를 사용하면 함수 컴포넌트에서도 상태 관리나 라이프사이클 처리를 할 수 있게 되었습니다.
- useState: 상태를 관리하기 위한 훅입니다. 클래스 컴포넌트의 this.state와 같이 상태를 관리할 수 있습니다.
- useEffect: 마운트, 업데이트, 언마운트 시 특정 처리를 위한 훅입니다. 클래스 컴포넌트의 componentDidMount, componentDidUpdate, componentWillUnmount에 대응됩니다.
- useContext: 컨텍스트를 사용하기 위한 훅으로, 컨텍스트 내의 값에 접근할 수 있습니다.
- useReducer: useState와 유사하게 상태를 관리하기 위한 훅이지만, 복잡한 상태 로직이나 액션을 관리하기 위해 사용됩니다.
- useMemo: 계산 결과를 메모이제이션하기 위한 훅으로, 컴포넌트가 다시 렌더링되도 계산을 최적화합니다.
- useCallback: 콜백 함수를 메모이제이션하기 위한 훅으로, 컴포넌트의 재렌더링 시 불필요한 재생성을 방지합니다.
- useRef: 참조를 관리하기 위한 훅으로, DOM 요소에 접근하거나 변수를 유지하는 데 사용됩니다.

<br>
<common-slide/>

---
transition: fade-out
---


# React vs Vue

- Reactivity System:
  - Vue: 선언적 데이터 바인딩을 사용합니다. data 객체의 속성이 변경되면 자동으로 뷰가 업데이트됩니다.
  - React: setState 또는 useState 훅을 사용하여 상태 변경을 알리고 컴포넌트를 재렌더링합니다.

- 템플릿 vs JSX:
  - Vue: HTML 기반의 템플릿을 사용하여 UI를 선언적으로 정의합니다. 선택적으로 JSX를 사용할 수도 있습니다.
  - React: JSX (JavaScript XML)를 사용하여 UI를 정의합니다.   
<br>
<common-slide/>

---
transition: fade-out
---

# React vs Vue

- 스타일링:
  - Vue: Single File Components에서 `<style>` 태그 내에 CSS를 포함시킬 수 있습니다. 스코프 된 CSS나 CSS 모듈도 지원됩니다.
  - React: CSS-in-JS 라이브러리 (예: styled-components, emotion)를 사용하거나 전통적인 CSS 및 CSS 모듈을 사용할 수 있습니다.

- API & 디자인 패러다임:
  - Vue: Options API와 Vue 3에서 도입된 Composition API를 제공합니다.
  - React: 함수형 컴포넌트와 훅을 사용합니다. 클래스 컴포넌트도 지원되지만, 최근에는 함수형 컴포넌트가 권장됩니다.  

<br>
<common-slide/>
---
transition: fade-out
---

# React vs Vue

- 타입스크립트 지원:
  - Vue: Vue 3에서 타입스크립트 지원이 향상되었습니다.
  - React: 타입스크립트와의 호환성이 뛰어나며, 많은 커뮤니티 지원이 있습니다.

<br>

<common-slide/>

---
transition: fade-out
---

### React vs Vue

- 리액트 vs Composition API vs options API

<a href="https://ibb.co/bz92Qw5"><img src="https://i.ibb.co/jgXWb0k/1.png" alt="1" ></a>
<br>
<common-slide/>

---
transition: fade-out
---

# Thank you