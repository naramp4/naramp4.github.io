---
title: "react에서 원하는 Props를 받고 있는지 체크하는 방법"
category:
    - node.js
tags:
    - web
    - node.js
---

상위 component로 부터 전달받은 props가 우리가 예상한 props인지 확인 하기 위해 PropTypes를 사용하겠다.

---

# 설치

powershell에서 아래를 입력하여 설치를 해준다.

```powershell
npm i prop-types
```

---

# 사용방법

## import

```jsx
import PropTypes form "prop-types"
```

## prop 타입 정의

```jsx
class Greeting extends React.Component {
  render() {
    return (
      <h1>Hello, {this.props.name}</h1>
    );
  }
}

Greeting.propTypes = {
  name: PropTypes.string
};
```

`Greeting.propTypes`를 통하여 name이 스트링인지 확인을 할 수 있으며 필수 값으로 설정하고자 하면 `PropTypes.string.isRequired`와 같이 입력을 해주면 된다.

해당 경고문은 javascript 콘솔을 통해 확인할 수 있다.

---
# 출처

[React 공식 홈페이지 - PropTypes와 함께 하는 타입 확인](https://ko.reactjs.org/docs/typechecking-with-proptypes.html){: target="_blank"}