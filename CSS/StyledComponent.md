# 컴포넌트 기반 CSS작성을 위한 Styled-Component

Styled Component 는 React 의 컴포넌트 기반 개발 환경에서 스타일링을 위한 CSS의 성능 향상을 위한 라이브러리이다.

Styled Component 를 사용하면 기존 CSS 문법으로도 스타일 속성이 추가된 React 컴포넌트를 만들 수 있다.

# 설치 
```javascript
npm install styled-components
```

# 사용법

* 스타일을 정의함과 동시에 해당 스타일을 갖는 컴포넌드 만들기.

    ```javascript
    import styled from "stylled-components";

    const title = styled.h1`
        text-align: center;
        color: red;
    `

    export defualt function App() {
        return <title>HELLO WORLD</title>
    }
    ```

    title이라는 컴포넌트에 tag와 스타일 속성을 한번에 정의해주고 사용할수 있다.

* 속성값으로 사용되는 함수에 props 전달하기

    ```javascript
    import styled from "stylled-components";

    const title = styled.h1`
        background-color: ${(props=>{props.primary? gray: black})}
        text-align: center;
        color: red;
    `

    export defualt function App() {
        return <title primary>HELLO WORLD</title>
    }
    ```

    title의 primary라는 props의 전달 여부에 따라 background-color가 결정된다.

    기존 컴포넌트에 별도로 속성을 추가하고 싶을때는 새로운 컴포넌트에 기존 컴포넌트를 할당해서 사용하면 된다. // . 대신 소괄호() 안에 기존 컴포넌트를 넣어줘야함 

    ```javascript
    import styled from "stylled-components";

    const title = styled.h1`
        background-color: ${(props=>{props.primary? gray: black})}
        text-align: center;
        color: red;
    `

    const titleAnd = styled(title)`
        font-size: 15px;
    `

    export defualt function App() {
        return (
            <title primary>HELLO WORLD</title>
            <titleAnd>add something</titleAnd>
        )
    }
    ```

    titleAnd는 title의 속성은 은 그대로 사용하면서 font-size에 대한 속성이 추가됌.