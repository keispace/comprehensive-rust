# Code Samples in This Training

이 교육을 위해 우리는 당신의 브라우저에서 실행될 수 있는 예제를 제공할 것입니다. 
이렇게 하면 설치가 훨씬 쉬워지고 모든 사용자가 일관된 환경을 사용할 수 있게됩니다.
> For this training, we will mostly explore the Rust language through examples
> which can be executed through your browser. This makes the setup much easier and
> ensures a consistent experience for everyone.

카고(cargo)를 설치하는 것은 여전히 좋습니다. 이 것은 당신의 연습을 더 쉽게 만들어 줍니다. 
마지막 날 강의에서 당신이 Cargo를 필요로 하는 의존성을 가지고 작업하는 경험을 할 것입니다.
> Installing Cargo is still encouraged: it will make it easier for you to do the
> exercises. On the last day, we will do a larger exercise which shows you how to
> work with dependencies and for that you need Cargo.

이 과정의 코드 블록들은 전부 대화형으로 구성되 있습니다. 
> The code blocks in this course are fully interactive:

```rust,editable
fn main() {
    println!("Edit me!");
}
```
코드 블록에 포커스를 두고 <kbd>Ctrl-Enter</kbd>를 눌러 실행해 볼 수 있습니다. 
> You can use <kbd>Ctrl-Enter</kbd> to execute the code when focus is in the text box.

<details>
<summary>강의 참조 노트</summary>

강의에서 대부분의 코드 샘플은 위와 같이 수정할수 있지만 일부 코드는 다음과 같은 이유로 수정할 수 없습니다: 

* 유닛 테스트는 내장 플레이그라운드에서 실행이 안됩니다. 외부 플레이그라운드 사이트에 붙여넣어 테스트를 실행하시기 바랍니다.
* 페이지에서 이동하면 내장된 플레이그라운드는 state를 잃습니다. 따라서 로컬 환경이나 외부 플레이그라운드 사이트에서 연습문제를 해결하는 것이 좋습니다.

> Most code samples are editable like shown above. A few code samples
> are not editable for various reasons:
> 
> * The embedded playgrounds cannot execute unit tests. Copy-paste the
>   code and open it in the real Playground to demonstrate unit tests.
> 
> * The embedded playgrounds lose their state the moment you navigate
>   away from the page! This is the reason that the students should
>   solve the exercises using a local Rust installation or via the
>   Playground.

</details>

---
역주:
- 저런 블록들은 [과정 사이트](https://google.github.io/comprehensive-rust/cargo/code-samples.html)에서 실행됩니다. 
- 소스단(md)에선 실행안됩니다(..)
