# Modern Features

러스트는 지난 40년간의 모든 (프로그래밍 언어들의) 경험으로 만들어졌습니다.
> Rust is built with all the experience gained in the last 40 years.

## Language Features

* 열거형과 패턴 매칭
* 제너릭
* FFI[^역주1] 런타임 오버헤드 없음
> * Enums and pattern matching.
> * Generics.
> * No overhead FFI.

## Tooling

* 엄청난 컴파일러 에러 체커
* 내장 종속성 관리자
* 내장 테스트 지원 툴
> * Great compiler errors.
> * Built-in dependency manager.
> * Built-in support for testing.


<details>
<summary>강의 참조 노트</summary>

키포인트: 

* 오류를 읽어보시기 바랍니다 --- 오랜기간 많은 개발자들이 컴파일러 출력을 무시하는데 익숙해져 있습니다. 러스트 컴파일러는 다른 컴파일러보다 더 수다스럽고, 복사-붙여넣기 할 수 있는 정도의 코드 피드백을 제공하는 경우가 많습니다. 

* 러스트 표준 라이브러리는 Java, Python이나 Go와 같은 언어에 비해서는 규모가 작습니다. 표준이나 기본적이라고 생각되는 아래와 같은 라이브러리가 포함되있지 않습니다: 

  * 난수 생성기, 하지만 [rand]문서를 참조하시기 바랍니다.
  * SSL 또는 TLS지원, 하지만 [rusttls]문서를 참조하시기 바랍니다.
  * JSON 지원, 하지만 [serde_json] 문서를 참조하시기 바랍니다.

이러한 배경에는 표준 라이브러리의 기능은 사라질 수 없어서 매우 안정적이어야 하기 때문입니다. 위의 예시들에서 러스트 커뮤니티는 가장 좋은 방법을 여전히 찾고 있고 그렇기 때문에 여기에 대한 '최상의 솔루션'이 아직 없습니다. 

러스트는 카고라는 패키지 관리자가 내장되어 있고, 서드파티 크레이트를 다운로드, 컴파일 하기 매우 쉽습니다. 이 또한 표준 라이브러리가 작은 이유가 될 수 있습니다. 

좋은 서드파티 크레이트를 찾는 것 자체가 문제가 될 수 있습니다. <https://lib.rs> 와 같은 사이트가 신뢰할수 있는 좋은 크레이트를 비교하여 찾는데 도움을 줄 수 있습니다. 

> Key points:
> 
> * Remind people to read the errors --- many developers have gotten used to
>   ignore lengthly compiler output. The Rust compiler is significantly more
>   talkative than other compilers. It will often provide you with _actionable_
>   feedback, ready to copy-paste into your code.
> 
> * The Rust standard library is small compared to languages like Java, Python,
>   and Go. Rust does not come with several things you might consider standard and
>   essential:
> 
>   * a random number generator, but see [rand].
>   * support for SSL or TLS, but see [rusttls].
>   * support for JSON, but see [serde_json].
> 
>   The reasoning behind this is that functionality in the standard library cannot
>   go away, so it has to be very stable. For the examples above, the Rust
>   community is still working on finding the best solution --- and perhaps there
>   isn't a single "best solution" for some of these things.
> 
>   Rust comes with a built-in package manager in the form of Cargo and this makes
>   it trivial to download and compile third-party crates. A consequence of this
>   is that the standard library can be smaller.
> 
>   Discovering good third-party crates can be a problem. Sites like
>   <https://lib.rs/> help with this by letting you compare health metrics for
>   crates to find a good and trusted one.

[rand]: https://docs.rs/rand/
[rusttls]: https://docs.rs/rustls/
[serde_json]: https://docs.rs/serde_json/

</details>

---
역주
 
[^역주1]: Foreign Function Interface. 타 언어 코드를 호출하기 위한 인터페이스
