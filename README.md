# mygRPC

아래 docs 를 참조하여 튜토리얼을 진행합니다.
https://grpc.io/docs/languages/go/quickstart/

진행시 아래 access error 가 발생했다.
go: could not create module cache: mkdir C:\Program Files\Go\pkg\mod: Access is denied.

Program Files 폴더는 window 보안 때문에 쓰기작업이 되지 않는다.

C:\Go 경로로 파일을 옮기고, 환경 변수를 잡아준뒤 재시작을 해줬다. ( 재시작을 하지 않아도 되는 방법은 없나.. )``

순간적으로 퍼포먼스를 내야하는 서비스를 개선하기 위해 gRPC 를 알아보고 있다.

알아보던 중 깨달은 점은 나는 항상 통신을 위해 JSON 형식만을 별 고려없이 사용해 왔다는 것이다.

Proto buffer 라는 포맷이 있다는 것도 알게 되어, 생각의 틀이 깨지고 더 넓은 시야를 갖게 된 느낌이였다.

우리는 항상 가독성과 디버깅이 용이한 High level 수준의 JSON 포맷으로된 통신을 사용해왔던 것이다.

High level 형식은 우리가 읽기 편하게 만들어져 있기 때문에 분량도 커지고, 데이터를 직렬화할때 오버헤드가 발생하게 된다.

통신 속도를 생각한다면 low level 형식이 좋은데 회사에서 필요한 서비스가 있는데 이곳에 한번 써보면 좋겠다 생각했다 ㅎㅎ

긴 장문 내용 데이터를 많이 통신해야되서 딱일것 같다.

또한, proto 파일에 "우리 이렇게 통신하자!" 약속을 적어두고, 각자 언어에 맞게 서버용, 클라용 파일을 생성하여 메소드로 만들어

사용한다는 점이 참 재미있다고 생각했다.

아직은 공식문서의 Quick Start 만 따라해봤고, 실무에 적용할 수 있게 좀 더 알아봐야겠다.
