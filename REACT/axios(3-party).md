# axios

브라우저, Node.js를 위한 http 비동기 라이브러리이다. fetch와 비슷한 역할을 하지만 자동으로 JSON으로 변환해주거나 더 많은 브라우저에서 작동된다는 장점이 있다. 

## 시작하기 
---

    npm install axios

```js
const axios = require('axios').default; // axios.메소드 로 사용
```

* get request

    axios.get(url[, config]) 

    ```js
    axios.get('url')
    ```

    axios.get(config)

    ```js
    axios({
        method: 'post',
        url: '/user/12345',
        data: {
            firstName: 'Fred',
            lastName: 'Flintstone'
        }
    });
    ```

    