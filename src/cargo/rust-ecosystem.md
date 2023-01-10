# The Rust Ecosystem

러스트의 생태계는 여러가지 도구들로 구성되어 있으며, 그 중 중요한 것들은 아래와 같습니다. 
> The Rust ecosystem consists of a number of tools, of which the main ones are:
* `rustc`: `.rs`확장자 파일을 바이너리 혹은 다른 중간자 형식으로 변환해주는 Rust 컴파일러입니다.
> * `rustc`: the Rust compiler which turns `.rs` files into binaries and other
>   intermediate formats.

* `cargo`: 러스트 종속성 관리자 및 빌드도구 입니다. <https://crates.io>에서 호스팅되는 여러 종속성을 다운로드하고 `rustc`가 당신의 프로젝트를 빌드할 때 이를 전달합니다. 
  또한 유닛 테스트를 실행하는 테스트 툴을 내장하고 있습니다.
> * `cargo`: the Rust dependency manager and build tool. Cargo knows how to
>   download dependencies hosted on <https://crates.io> and it will pass them to
>   `rustc` when building your project. Cargo also comes with a built-in test
>   runner which is used to execute unit tests.

* `rustup`: 러스트 툴체인 설치 프로그램 및 업데이트 프로그램. 
  이 도구는 새 버전의 러스트가 출시될 때 `rustc` 및 `cargo` 설치하고 업데이트하는 데 사용됩니다. 
  또한 `rustup`은 표준 라이브러리에 대한 문서를 다운로드할 수도 있습니다. 
  한 번에 여러 버전의 러스트를 설치할 수 있으며 `rustup`을 통해 필요에 따라 이들 버전을 전환할 수 있습니다
> * `rustup`: the Rust toolchain installer and updater. This tool is used to
>   install and update `rustc` and `cargo` when new versions of Rust is released.
>   In addition, `rustup` can also download documentation for the standard
>   library. You can have multiple versions of Rust installed at once and `rustup`
>   will let you switch between them as needed.


<details>
<summary>강의 참조 노트</summary>

키포인트: 

* 러스트는 6주마다 새로운 릴리즈가 발표되며 이전 릴리즈와의 호환성을 유지하고 있습니다.
* 릴리즈는 3가지 버전으로 제공됩니다: "stable", "beta" 그리고 "nightly".
* 새로운 기능은 "nightly" -> "beta" -(6주 후)-> "stable" 로 변경됩니다.
* 러스트는 [editions]으로 으로 진행됩니다: 현재는 Rust 2021 에디션입니다. 그전에는 Rust 2015와 Rust 2018입니다. 
  * 에디션은 이전 에디션과 호환이 되지 않을 수 있습니다.
  * 프로그램 붕괴를 방지하기 위해 에디션은 옵션입니다.: `Cargo.toml`에서 지정할 수 있습니다.
  * 생태계가 분열되는 것을 막기 위해 러스트 컴파일러는 다른 에디션에서 작성된 코드의 혼합이 가능합니다.

> Key points:
> * Rust has a rapid release schedule with a new release coming out
>   every six weeks. New releases maintain backwards compatibility with
>   old releases --- plus they enable new functionality.
> 
> * There are three release channels: "stable", "beta", and "nightly".
> 
> * New features are being tested on "nightly", "beta" is what becomes
>   "stable" every six weeks.
> 
> * Rust also has [editions]: the current edition is Rust 2021. Previous
>   editions were Rust 2015 and Rust 2018.
> 
>   * The editions are allowed to make backwards incompatible changes to
>     the language.
> 
>   * To prevent breaking code, editions are opt-in: you select the
>     edition for your crate via the `Cargo.toml` file.
> 
>   * To avoid splitting the ecosystem, Rust compilers can mix code
>     written for different editions.

[editions]: https://doc.rust-lang.org/edition-guide/

</details>