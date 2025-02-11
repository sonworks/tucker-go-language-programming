# Chapter 00 개발 환경 구축

시스템 환경 (2025/2)
 * GO SDK: 1.23.6
 * Visual Studio Code: 1.93.1
   * Go (golang) extension: v0.44.0
 * OS: Windows 11

## 전제

 * Git 설치 완료
 * Visual Studio Code (이하, VScode) 설치 완료
   - Go language 확장팩 설치 완료

## 개발 환경 구축

### Windows
 * GO 언어 설치
   - [GO 언어 공식 사이트 (https://go.dev/)](https://go.dev/) 에서 해당 파일을 다운로드 후 설치
 * 설치 완료 확인 
   - cmd 에서 `go version` 을 입력하여 버전이 표시되는지 확인되면 OK
   - > go version go1.23.6 windows/amd64

## 간단한 코드 실행

```go
// goproject/hello/hello.go
package main

import "fmt"

func main() {
	fmt.Print("Hello World!")
}
```
 * `hello.go` 파일에 소스코드를 입력 후 저장
 * [VScode 메뉴 > Terminal > New Terminal] 을 클릭, 터미널 창을 생성
 * 해당 폴더로 이동
   - `cd hello`
 * Go 모듈 생성
   - `go mod init goproject/hello`
 * Go 실행 파일 생성
   - `go build`
 * 파일 실행, 실행 결과 확인
   - `.\hello.exe`
   - > Hello World!

## 참고
 * [본서 예제 코드 (GitHub)](https://github.com/tuckersGo/musthaveGo)
