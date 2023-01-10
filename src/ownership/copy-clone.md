# Copying and Cloning

의미구조(Semantics)가 이동할때, 특정 타입은 기본적으로 복사됩니다:
> While move semantics are the default, certain types are copied by default:

```rust,editable
fn main() {
    let x = 42;
    let y = x;
    println!("x: {x}");
    println!("y: {y}");
}
```

이러한 유형들은 `Copy` 트레이트를 구현합니다. 

직접 만든 타입들도 `Copy`트레이트를 구현하여 의미복사를 할 수 있습니다:
> These types implement the `Copy` trait.
> 
> You can opt-in your own types to use copy semantics:

```rust,editable
#[derive(Copy, Clone, Debug)]
struct Point(i32, i32);

fn main() {
    let p1 = Point(3, 4);
    let p2 = p1;
    println!("p1: {p1:?}");
    println!("p2: {p2:?}");
}
```

* 할당 후, `p1`와 `p2`는 자신의 데이터를 소유합니다.
* 명시적으로 `p1.clone()`를 사용하여 데이터를 복사할 수 있습니다.
> * After the assignment, both `p1` and `p2` own their own data.
> * We can also use `p1.clone()` to explicitly copy the data.


<details>
<summary>강의 참조 노트</summary>

복사와 복제는 같지 않습니다: 

* 복사는 메모리 영역의 비트단위 복사본으로 임의의 객체에서는 동작하지 않습니다. 
* 복제는 보다 일반적인 작업으로 `Clone`트레이트를 구현하여 사용자 지정동작을 허용합니다.
* `Drop` 트레이트를 구현한 타입에서 복사는 동작하지 않습니다.

> Copying and cloning are not the same thing:
> 
> * Copying refers to bitwise copies of memory regions and does not work on arbitrary objects.
> * Cloning is a more general operation and also allows for custom behavior by implementing the `Clone` trait.
> * Copying does not work on types that implement the `Drop` trait.

위의 예시에서 다음을 시도해 보시기 바랍니다: 
* `struct Point` 구조체에 `String`필드를 추가하면 어떻게 됩니까? 
* `derive` 속성에서 `Copy`를 제거해도 동작합니까?
* `Copy`를 제거 한 후, `p1`을 이동해도 여전히 출력 됩니까?

> In the above example, try the following:
> 
> * What happens when you add a `String` field to `struct Point`?
> * Does it work when you remove `Copy` from the `derive` attribute?
> * After removing `Copy`, can you still print `p1` after the move?

</details>

---
역주
- `#[derive(Copy, Clone, Debug)]`를 통해 Point 구조체가 Copy되도록 함
