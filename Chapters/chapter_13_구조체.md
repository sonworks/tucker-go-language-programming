# Chapter 13 구조체

## 선언 및 기본 사용

### 선언
```go
/* // 예시
type 타입명 struct {
    필드명 타입
    ...
    필드명 타입
}
*/

type Student struct {
    Name string
    Class int
    No int
    Score float64
}
```

### 구조체 변수 초기화

```go
type House struct {
    Address string
    Size int
    Price float64
    Type string
}
func main() {
    // 초기값 생략 선언 방식
    var house1 House
    house1.Address = "서울시 강동구 ..."
    house1.Size = 28
    house1.Price = 9.8
    house1.Type = "아파트"

    // 모든 필드 초기화 선언 방식
    var house2 House = House {
        "서울시 강동구 ...",
        28,
        9.8,
        "아파트",
    }
}
```

## 프로그래밍에서 구조체의 역할

객체 간 결합도(객체간 의존관계)는 낮추고 연관있는 데이터 간 응집도를 올려준다.

> 결합도(Coupling): 모듈간 상호 의존관계를 형성해서 서로 강하게 결합되어 있는 정도를 나타내는 용어로 '의존성'이라고 말하기도 함
>
> 응집도(Cohesion): 모듈의 완성도를 말하는 것으로 모듈 내부의 모든 기능이 단일 목적에 충실하게 보여있는지는 나타내는 용어
