# Chapter 07 함수

## 함수 정의

```go
// 예시
 (1) (2)  (3)          (4) (5)
func Add(a int, b int) int {
    return a + b
}

```

 * (1): 함수 정의 키워드
 * (2): 함수명
 * (3): 매개변수
 * (4): 반환 타입
 * (5): 함수 코드 블록

## 멀티 반환 함수

함수는 값을 여러개 반환할 수 있으며, 반환값이 여럿일 때는 반환 타입들을 소괄호로 묶어서 표현한다.

```go
package main

import "fmt"

func Divide(a, b int) (int, bool) {
    if b == 0 {
        return 0, false
    }
    return a / b, true
}

func main() {
    c, success := Divide(9, 3)
    fmt.Println(c, success)
    d, success := Divide(9, 0)
    fmt.Println(d, success)
}

// <Result>
// 3 true
// 0 false
```

## 재귀 호출

함수 안에서 자기 자신 함수를 다시 호출하는 것을 말한다.

```go
// package , import 생략
func printNo(n int) {
    if n == 0 { // 재귀 호출 탈출 조건
        return
    }
    fmt.Println(n)
    printNo(n-1) // 재귀 호출
    fmt.Println("After", n) // 재귀 호출 이후 출력
}
func main() {
    printNo(3)
}

// <Result>
// 3
// 2
// 1
// After 1
// After 2
// After 3
```