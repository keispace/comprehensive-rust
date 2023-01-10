# Scopes and Shadowing

<<<<<<< HEAD
외부 스코프와 동일 스코프 범위의 변수를 가릴 수 있습니다.(변수 쉐도잉)
> You can shadow variables, both those from outer scopes and variables from the same scope:
=======
You can shadow variables, both those from outer scopes and variables from the
same scope:
>>>>>>> bee9cdab92953660ae8c8c1e308df3ce3ee26460

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

<<<<<<< HEAD
---
역주
- after의 경우 inner scope 수명이 다해서 원래 변수인 a가 표시되는 겁니다. 
=======
<details>

* Shadowing looks obscure at first, but is convenient for holding on to values after `.unwrap()`.
* The following code demonstrates why the compiler can't simply reuse memory locations when shadowing an immutable variable in a scope, even if the type does not change.

```rust,editable
fn main() {
    let a = 1;
    let b = &a;
    let a = a + 1;
    println!("{a} {b}");
}
```

</details>
>>>>>>> bee9cdab92953660ae8c8c1e308df3ce3ee26460
