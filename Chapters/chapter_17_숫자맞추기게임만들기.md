# Chapter 17 숫자 맞추기 게임 만들기

## 완성한 코드

```go
package main

import (
    "bufio"
    "fmt"
    "math/rand"
    "os"
    "time"
)

var stdin = bufio.NewReader(os.Stdin)

func InputIntValue() (int, error) {
    var n int
    _, err := fmt.Scanln(&n)
    if err != nil {
        stdin.ReadString('\n')
    }
    return n, err
}
func main() {
    rand.Seed(time.Now().UnixNano())

    r := rand.Intn(20)
    cnt := 1
    for {
        fmt.Printf("숫자값을 입력하세요:")
        n, err := InputIntValue()
        if err != nil {
            fmt.Println("숫자만 입력하세요.")
        } else {
            if n > r {
                fmt.Println("입력하신 숫자가 더 큽니다.")
            } else if n < r {
                fmt.Println("입력하신 숫자가 더 작습니다.")
            } else {
                fmt.Println("숫자를 맞췄습니다. 시도한 횟수:", cnt)
                break
            }
            cnt++
        }
    }
}

// <Result>
// 숫자값을 입력하세요:16
// 입력하신 숫자가 더 큽니다.
// 숫자값을 입력하세요:5
// 입력하신 숫자가 더 작습니다.
// 숫자값을 입력하세요:08
// 숫자만 입력하세요.
// 숫자값을 입력하세요:8
// 입력하신 숫자가 더 작습니다.
// 숫자값을 입력하세요:11
// 입력하신 숫자가 더 작습니다.
// 숫자값을 입력하세요:13
// 입력하신 숫자가 더 작습니다.
// 숫자값을 입력하세요:14
// 입력하신 숫자가 더 작습니다.
// 숫자값을 입력하세요:15
// 숫자를 맞췄습니다. 시도한 횟수: 7
```

