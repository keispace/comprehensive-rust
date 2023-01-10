# Runtime Guarantees

런타임 시 정의되지 않음(undefined) 동작 없음: 
* 배열 접근시 경계 체크
* 정수형의 오버플로우가 정의되어있습니다. 

> No undefined behavior at runtime:
> 
> * Array access is bounds checked.
> * Integer overflow is defined.

<details>
<summary>강의 참조 노트</summary>

키포인트: 
* 정수형 오버플로우는 컴파일 타임 플레그를 통해 정의됩니다. 옵션은 패닉(프로그램 크레시) 혹은 wrap-around semantics입니다. 기본적으로 디버그 모드(`cargo build`)에서는 패닉이, 릴리즈 모드(`cargo build --release`)에서는 wrap-around이 발생합니다. 
* 컴파일 플레그를 사용하여 경계체크를 무력화 할 수 없습니다. `unsafe`를 사용하더라도 마찬가지입니다. 하지만 `unsafe`에서 호출 가능한 `slice::get_unchecked`같은 함수는 경계 검사를 수행하지 않습니다.

> Key points:
> 
> * Integer overflow is defined via a compile-time flag. The options are
>   either a panic (a controlled crash of the program) or wrap-around
>   semantics. By default, you get panics in debug mode (`cargo build`)
>   and wrap-around in release mode (`cargo build --release`).
> 
> * Bounds checking cannot be disabled with a compiler flag. It can also
>   not be disabled directly with the `unsafe` keyword. However,
>   `unsafe` allows you to call functions such as `slice::get_unchecked`
>   which does not do bounds checking.

</details>