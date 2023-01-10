# Scopes and Shadowing

외부 스코프와 동일 스코프 범위의 변수를 가릴 수 있습니다.(변수 쉐도잉)
> You can shadow variables, both those from outer scopes and variables from the same scope:

```rust,editable
fn main() {
    let a = 10;
    println!("before: {a}");

    {
        let a = "hello";
        println!("inner scope: {a}");

        let a = true;
        println!("shadowed in inner scope: {a}");
    }

    println!("after: {a}");
}
```

<details>
<summary>강의 참조 노트</summary>

* 쉐도잉은 모호해 보일 수 있지만 `.unwrap()` 이후의 값을 할당하는데 용이합니다. 
* 아래 코드는 컴파일러가 스포크에서 변경되지 않는 변수를 쉐도잉할때 타입이 동일하더라도 메모리 위치를 단순 재사용 할 수 없는 이유를 보여줍니다.(원본 a를 참조한 b와 쉐도잉 된 a(a+1) 둘다 살아있어야 하므로 메모리를 따로 할당합니다.)
> * Shadowing looks obscure at first, but is convenient for holding on to values after `.unwrap()`.
> * The following code demonstrates why the compiler can't simply reuse memory locations when shadowing an immutable variable in a scope, even if the type does not change.

```rust,editable
fn main() {
    let a = 1;
    let b = &a;
    let a = a + 1;
    println!("{a} {b}");
}
```

</details>

---
역주
- after의 경우 inner scope 수명이 다해서 원래 변수인 a가 표시되는 겁니다. 