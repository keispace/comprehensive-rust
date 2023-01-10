# Day 1 Morning Exercises

## Arrays and `for` Loops

([back to exercise](for-loops.md))

```rust
{{#include for-loops.rs}}
```
### Bonus question

사실 잘 동작하진 않습니다. slice-of-slices (`&[&[i32]]`)을 입력 타입으로 사용하여 모든 크기의 행렬을 처리할 수 있습니다. 하지만 리턴 값을 소유해야 하기때문에 `&[&[i32]]` 타입을 사용할 순 없습니다. 

`Vec<Vec<i32>>`와 같은 타입을 사용하려고 시도할 수도 있지만 역시 잘 동작하진 않습니다:  `Vec<Vec<i32>>` 타입을 `&[&[i32]]`로 변환하는 것이 어렵기 때문에 `pretty_print`을 사용하는데 어려움이 있습니다.

> It honestly doesn't work so well. It might seem that we could use a slice-of-slices (`&[&[i32]]`) as the input type to transpose and thus make our function handle any size of matrix. However, this quickly breaks down: the return type cannot be `&[&[i32]]` since it needs to own the data you return.
> 
> You can attempt to use something like `Vec<Vec<i32>>`, but this doesn't work very well either: it's hard to convert from `Vec<Vec<i32>>` to `&[&[i32]]` so now you cannot easily use `pretty_print` either.