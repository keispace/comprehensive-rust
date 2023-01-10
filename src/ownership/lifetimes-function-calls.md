# Lifetimes in Function Calls

함수는 인수를 빌리는 것 외에도 빌린 값을 반환할 수 있습니다:
> In addition to borrowing its arguments, a function can return a borrowed value:

```rust,editable
#[derive(Debug)]
struct Point(i32, i32);

fn left_most<'a>(p1: &'a Point, p2: &'a Point) -> &'a Point {
    if p1.0 < p2.0 { p1 } else { p2 }
}

fn main() {
    let p1: Point = Point(10, 10);
    let p2: Point = Point(20, 20);  
    let p3: &Point = left_most(&p1, &p2);
    println!("left-most point: {:?}", p3);
}
```

* `'a`는 제너릭 매개변수로 컴파일러로에 의해 추론됩니다.
* 수명은 `'` 로 표기하며 러스트에서는 일반적으로 `'a` 라고 표현합니다.
* `&'a Point` 는 as  `a`와 동일한 수명을 가지는 빌려온 `Point` 입니다.
  * **중요** : 다른 스코프에 있어도 적용 됩니다.
> * `'a` is a generic parameter, it is inferred by the compiler.
> * Lifetimes start with `'` and `'a` is a typical default name.
> * Read `&'a Point` as "a borrowed `Point` which is valid for at least the lifetime `a`".
> * The _at least_ part is important when parameters are in different scopes.

<details>
<summary>강의 참조 노트</summary>

위 예제에서 다음을 시도해봅니다:
> In the above example, try the following:

*  `p2`와 `p3`를 새로운 범위(`{...}`)로 아래 코드와 같이 이동해 봅니다:
> * Move the declaration of `p2` and `p3` into a a new scope (`{ ... }`), resulting in the following code:
  ```rust,ignore
  #[derive(Debug)]
  struct Point(i32, i32);
  fn left_most<'a>(p1: &'a Point, p2: &'a Point) -> &'a Point {
      if p1.0 < p2.0 { p1 } else { p2 }
  }
  fn main() {
      let p1: Point = Point(10, 10);
      let p3: &Point;
      {
          let p2: Point = Point(20, 20);
          p3 = left_most(&p1, &p2);
      }
      println!("left-most point: {:?}", p3);
  }
  ```
  `p3`가 `p2`보다 오래 지속되기 때문에 이 예제는 컴파일되지 않음을 확인하시기 바랍니다.
>   Note how this does not compile since `p3` outlives `p2`.

* 워크스페이스을 초기화하고 함수 시그니처를 `fn left_most<'a, 'b>(p1:&'a Point, p2:&'a Point) -> &'b Point`로 변경합니다. `'a`와 `'b`의 수명 사이가 불분명하기 때문에 이것은 컴파일되지 않습니다.
> * Reset the workspace and change the function signature to `fn left_most<'a, 'b>(p1: &'a Point, p2: &'a Point) -> &'b Point`. This will not compile because the relationship between the lifetimes `'a` and `'b` is unclear.

</details>

--- 

역주
- left_most함수가 종료되더라도 리턴값 p3은 매개변수인 p1,p2와 동일한 수명이라 main에서도 유효해집니다. 
