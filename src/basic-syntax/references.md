# References

C++과 마찬가지로 러스트도 참조형을 갖습니다:
> Like C++, Rust has references:

```rust,editable
fn main() {
    let mut x: i32 = 10;
    let ref_x: &mut i32 = &mut x;
    *ref_x = 20;
    println!("x: {x}");
    
}
```

C++과의 차이점:
* C포인터와 유사하게 `ref_x`에 할당할 경우 참조를 해제해야 합니다. 
* 러스트는 특정한 경우(메서드 호출)에 자동으로 참조 해제를 합니다.
* `mut`로 선언된 참조는 수명에 따라 다른 값으로 할당될 수 있습니다.

> Some differences from C++:
> 
> * We must dereference `ref_x` when assigning to it, similar to C pointers,
> * Rust will auto-dereference in some cases, in particular when invoking
>   methods (try `count_ones`).
> * References that are declared as `mut` can be bound to different values over their lifetime.


---
역주 
- count_ones 메서드를 만들어서 테스트해보세요
