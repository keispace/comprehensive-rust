# Small Example

러스트로 작성된 작은 예제입니다. 
> Here is a small example program in Rust:

```rust,editable
fn main() {              // 프로그램 진입점(Program entry point)
    let mut x: i32 = 6;  // 가변 변수 할당(Mutable variable binding)
    print!("{x}");       // printf와 같은 출력 매크로(Macro for printing, like printf)
    while x != 1 {       // 표현식에는 괄호 없음(No parenthesis around expression)
        if x % 2 == 0 {  // 수학식 기호는 다른언어와 유사(Math like in other languages)
            x = x / 2;
        } else {
            x = 3 * x + 1;
        }
        print!(" -> {x}");
    }
    println!();
}
```

<details>
<summary>강의 참조 노트</summary>

이 코드는 콜라츠 추측(Collatz conjecture)으로 구현됩니다:  
반복문이 언제나 종료조 것이라고 믿지만 증명된 것은 아닙니다. 코드를 수정하고 실행해 보시기 바랍니다.

키포인트: 
* 모든 변수가 정적으로 입력됨을 설명합니다. `i32`를 삭제하여 유형 추론을 유발해 볼 수 있습니다. `i32`대신 `i8`로 변경하여 런타임 오버플로를 유발해 볼 수 있습니다.
* `let mut x`를 `let x`로 수정하여 컴파일 오류에 대해 토론합니다.
* 인수가 포맷 문자열과 일치하지 않는 경우 `print!`에서의 컴파일 오류가 발생함을 언급하는 것도 좋습니다.
* 단일 변수보다 복잡한 식을 인쇄하려면 {}을(를) 자리 표시자로 사용하는 방법을 보여 줍니다.
* 학생들에게 표준 라이브러리를 보여주고, 미니 언어 형식의 규칙이 있는 std::fmt를 검색하는 방법을 보여줍니다. 학생들이 표준 라이브러리에서 검색하는 것에 익숙해지는 것이 중요합니다.

> The code implements the Collatz conjecture: it is believed that the loop will
> always end, but this is not yet proved. Edit the code and play with different
> inputs.


Key points:
* Explain that all variables are statically typed. Try removing `i32` to trigger
  type inference. Try with `i8` instead and trigger a runtime integer overflow.
* Change `let mut x` to `let x`, discuss the compiler error.
* Show how `print!` gives a compilation error if the arguments don't match the
  format string.
* Show how you need to use `{}` as a placeholder if you want to print an
  expression which is more complex than just a single variable.
* Show the students the standard library, show them how to search for `std::fmt`
  which has the rules of the formatting mini-language. It's important that the
  students become familiar with searching in the standard library.

</details>
