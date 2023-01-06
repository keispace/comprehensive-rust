# Interoperability with C

러스트는 C 호출규약과 함께 객체 파일을 연결하는 것을 완벽하게 지원합니다. 
반대로 러스트 함수를 내보내서 C에서 호출 할 수 있습니다. 

원하는 경우 직접 코딩할 수 있습니다: 

> Rust has full support for linking object files with a C calling convention.
> Similarly, you can export Rust functions and call them from C.
> 
> You can do it by hand if you want:

```rust
extern "C" {
    fn abs(x: i32) -> i32;
}

fn main() {
    let x = -42;
    let abs_x = unsafe { abs(x) };
    println!("{x}, {abs_x}");
}
```
우리는 이미[Safe FFI 래퍼 연습문제](../../exercises/day-3/safe-ffi-wrapper.md)에서 이를 다루었습니다. 

> 이는 대상 플랫폼에 대한 완전한 지식을 전제로 합니다. 실 제품에는 권장하진 않습니다.

다음으로 좀 더 나은 옵션을 살펴보겠습니다.

> We already saw this in the [Safe FFI Wrapper
> exercise](../../exercises/day-3/safe-ffi-wrapper.md).
> 
>> This assumes full knowledge of the target platform. Not recommended for
>> production.
> 
> We will look at better options next.
