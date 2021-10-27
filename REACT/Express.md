# Express.js
Express.js는 Node.js 환경에서 웹 서버, 또는 API 서버를 제작하기 위해 사용되는 인기 있는 프레임워크이다.
# 사용법
메소드와 URL로 편리하게 라우팅 할 수 있다.
```javascript
const router = express.Router()

router.get('/lower', (req, res) =>{
  res.send(data)
})

router.post('/lower', (req, res) =>{
  // do something
})
```