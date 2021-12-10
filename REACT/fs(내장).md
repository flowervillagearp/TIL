# fs.readFile(path[, option], callback)

fs.readFile 메소드는 비동기적으로 파일 내용 전체를 읽음. 메소드의 인자는 3개이다.

* path

    path의 인자를 읽는다. string || buffer || url || integer 타입을 path인자로 넣을 수 있다. 

* option

    option 인자는 선택적으로 넣을수 있다. object || string 이 인자로 들어간다.

* callback 

    콜백함수가 인자로 들어간다. 파일을 읽은 후에 비동기적으로 실행된다. 

    이 콜백함수에는 err와 data라는 두가지 파라미터가 들어간다. 

    * err
        
        파일을 읽어올때 에러가 발생한다면 err에 값이 들어오고 에러가 없다면 값은 null이 된다. 

    * data 

        data에는 string이나 buffer라는 객체가 전달된다. option으로 인코딩 방식을 명시하지 않았다면 buffer가 들어옴.

### e.g.

```javascript
    fs.readFile('test.txt', 'utf8', (err, data) => { //test.txt 파일을 읽음, utf8로 인코딩. 
        if (err) {
            throw err; // 파일을 읽을때 에러가 나오면 에러 출력. 아니면 err 값이 null이니까 false.
        }
        console.log(data); // utf8로 인코딩한 값이 출력 -> string
    });
```

# fs.writeFile



fs모듈 더보기(https://nodejs.org/dist/latest-v14.x/docs/api/fs.html#fs_fs_writefile_file_data_options_callback)
