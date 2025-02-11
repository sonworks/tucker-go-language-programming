# Chapter 24 고루틴과 동시성 프로그래밍

## 고루틴 사용

### 완성한 코드

복수의 고루틴을 생성하여 문자와 숫자를 출력하는 예제

```go
package main

import (
	"fmt"
	"time"
)

func PrintHangul() {
	hanguls := []rune{'가', '나', '다', '라', '마', '바', '사'}
	for _, v := range hanguls {
		time.Sleep(300 * time.Millisecond)
		fmt.Printf("%c ", v)
	}
}

func PrintNumbers() {
	for i := 1; i <= 5; i++ {
		time.Sleep(400 * time.Millisecond)
		fmt.Printf("%d ", i)
	}
}

func main() {
	// 고루틴 생성
	go PrintHangul()
	go PrintNumbers()

	// 3초간 대기
	time.Sleep(3 * time.Second)
}

// <Result>
// 가 1 나 2 다 3 라 마 4 바 5 사
```

## 동시성 프로그래밍 주의점

### 문제점
동시성 프로그래밍의 문제점은 동일한 메모리 자원에 여러 고루틴이 접근할때 발생한다.

즉, 고루틴은 각 CPU 코어에서 별도로 동작하지만, 같은 메모리 공간에 동시에 접근해서 값을 변경시킬 수 있다.

### 해결 방안

 * 뮤텍스를 이용한 동시성 문제 해결
   - 단, 데드락을 발생할 수 있는 또 다른 문제점이 생김
 * 같은 자원은 여러 고루틴이 접근하지 못하도록 자원을 관리
   - 영역을 나누는 방법
   - 역할을 나누는 방법
