# HTTPS(Hyper Text Transfer Protocol Secure Socket layer )

https는 http요청을 SSL이나 TLS 알고리즘으로 암호화 해서 전송. 이 암호는 정확한 키가 없다면 내용을 알 수 없다.

http요청을 암호화 하기 위해서는 인증서, CA, 비대칭 키 암호화를 알아야 한다.

## 인증서 

데이터를 제공한 서버가 테이터를 보내준 서버인지 인증, 확인 하는 용도이다.

요청을 받은 서버는 인증서와 함께 응답을 클라이언트로 전달, 클라이언트는 인증서에 명시된 도메인과 응답을 준 도메인을 비교한다.

* mkcert로 인증서 발급하기

        $ brew install mkcert //mkcert 설치

        $ mkcert -install //로컬을 인증된 발급기관으로 추가

        $ mkcert -key-file key.pem -cert-file cert.pem localhost 127.0.0.1 ::1 //localhost, 127.0.0.1(IPv4), ::1(IPv6)에서 사용하는 인증서 발급

    발급받은 인증서(cert.pem, key.pem)는 프로젝트를 진행하는 폴더에 넣어서 쓸수 있다.

## CA(Certificate Authority)

위 인증서를 발급해주는 기관

## 비대칭 키(공개키 라고도 함)

키는 어떤 문자열이고 이 키로 값을 암호화, 복호화 해주는 알고리즘이 존재하는데 비태칭키는 하나의 키를 클라이언트에 공개하고 다른 하나의 키를 숨겨서 서버에서만 데이터들을 다룰수 있다.

a키로 암호화를 한다면 b키로만 복호화를 할 수 있고 b키로 암호화를 한다면 a키로만 복호화가 가능하다. 클라이언트에서 a키로 암호화 한 데이터는 b키를 가지고 있는 서버에서만 볼수 있고 다른 클라이언트들은 볼수 없게 된다.



