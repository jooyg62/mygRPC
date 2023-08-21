# mygRPC

아래 docs 를 참조하여 튜토리얼을 진행합니다.
https://grpc.io/docs/languages/go/quickstart/

진행시 아래 access error 가 발생했다.
go: could not create module cache: mkdir C:\Program Files\Go\pkg\mod: Access is denied.

Program Files 폴더는 window 보안 때문에 쓰기작업이 되지 않는다.

C:\Go 경로로 파일을 옮기고, 환경 변수를 잡아준뒤 재시작을 해줬다. ( 재시작을 하지 않아도 되는 방법은 없나.. )``
