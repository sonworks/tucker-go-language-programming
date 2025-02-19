# Tucker 노트 A - Go 문법 보충 수업

## 알아두면 유용한 go 명령어

Go 언어에서 제공하는 유용한 도구(명령어)는 go 뒤에 원하는 명령어를 써주면 된다.

예를 들면, 빌드를 수행하는 도구인 build 명령은 다음과 같다.
```cmd
> go build
```

### 유용한 go 명령어
| 명령어 | 설명 |
| --- | --- |
| bug | Go 언어 자체의 버그 리포트할 수 있는 사이트를 브라우저로 접속한다 |
| build | 패키지를 컴파일한다 |
| clean | 컴파일 시 생성되는 패키지 목적 파일(object files)들을 삭제한다 |
| doc | 패키지 문서를 출력한다 (ex, go doc) |
| env | Go 환결 설정을 출력한다 |
| fix | 오래된 API를 사용하는 Go프로그램을 찾아 새로운 API로 업데이트한다 |
| fmt | 패키지를 리포멧하는 gofmt 툴을 실행한다. Go 코딩 규약에 맞춰 소스코드를 수정해 준다 |
| generate | 패키지 안에 생성절차가 정의되어 있는 경우 그에 따라서 go 파일을 생성한다 |
| get | 현재 모듈 패키지 목록에 패키지를 추가하고 다운 받는다 |
| install | 컴파일한 뒤 결과를 GOPATH/bin 경로에 설치한다 |
| list | 패키지나 모듈 목록을 출력한다 |
| mod | 새로운 모듈을 만들거나 관리한다 |
| run | 컴파일한 뒤 결과 프로그램을 실행한다. (실행 파일을 생성하지 않는다) |
