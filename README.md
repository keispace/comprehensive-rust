# Comprehensive Rust 🦀


이 저장소에는 안드로이드 팀에 의해 개발된 4일간의 Comprehensive Rust에 대한 소스 코드가 있습니다.
이 과정은 러스트의 모든 측면을 다룹니다.
기본 구문부터 제네릭 및 오류 처리에 이르기까지 다양한 러스트의 모든 측면을 다룹니다. 
또한 마지막 날에는 안드로이드 관련 콘텐츠까지 다룹니다.
> This repository has the source code for Comprehensive Rust 🦀, a four day Rust
course developed by the Android team. The course covers all aspects of Rust,
from basic syntax to generics and error handling. It also includes
Android-specific content on the last day.

(원본)사이트를 방문해 보세요 **https://google.github.io/comprehensive-rust/**.  
* 원문병기 번역본은 **https://keispace.github.io/comprehensive-rust-kr/**
> Read the course at **https://google.github.io/comprehensive-rust/**.

## Course Format and Target Audience

본 과정은 경험이 풍부한 C/C++이나 자바와 같은 소프트웨어 엔지니어에게 러스트를 가르칠 목적으로 구글 내부에서 사용됩니다.  

이 과정은 교실과 같은 환경에서 진행되며 우리는 러스트를 그들의 팀에게 가르치려는 다른 사람들에게 유용하기를 바랍니다. 
이 과정은 강의실에서 일어나는 토론이 빠져있기 때문에 조금은 덜 유용할 수 있습니다. 
이 과정 가운데 질문이나 답변, 코드샘플의 컴파일 에러와 같은 것들을 확인할 수 없기 때문에 아래 참고 자료를 활용하여 좀 더 (당신의 강의를) 개선하기를 희망합니다.
* [speaker notes](https://github.com/google/comprehensive-rust/issues/53) 
* [publishing videos](https://github.com/google/comprehensive-rust/issues/52)
> The course is used internally at Google when teaching Rust to experienced
> software engineers. They typically have a background in C++ or Java.
> 
> The course is taught in a classroom setting and we hope it will be useful for
> others who want to teach Rust to their team. The course will be less useful for
> self-study since you miss out on the discussions happening in the classroom. You
> don't see the questions and answers and you don't see the compiler errors we
> trigger when going through the code samples. We hope to improve on this via
> [speaker notes](https://github.com/google/comprehensive-rust/issues/53) and by
> [publishing videos](https://github.com/google/comprehensive-rust/issues/52).
> 
## Building


강좌는 [mdBook](https://github.com/rust-lang/mdBook)과 [Svgbob plugin](https://github.com/boozook/mdbook-svgbob)를 사용해서 만들었습니다. 
아래 쉘로 라이브러리를 설치 합니다.
> The course is built using [mdBook](https://github.com/rust-lang/mdBook) and its [Svgbob plugin](https://github.com/boozook/mdbook-svgbob). Install both tools with

```shell
$ cargo install mdbook
$ cargo install mdbook-svgbob
```

실행은 아래와 같이 합니다.
> Then run

```shell
$ mdbook test
```

모든 강의 내용에 대한 테스트는 아래와 같이 실행하세요
> to test all included Rust snippets. Run

```shell
$ mdbook serve
```

<http://localhost:3000>에서 실행된 모든 컨텐츠를 확인할 수 있습니다. 
`mdbook build`을 실행하면 `book/`폴더에서 static 버전이 생성됩니다. 

> to start a web server with the course. You'll find the content on
> <http://localhost:3000>. You can use `mdbook build` to create a static version
> of the course in the `book/` directory.


## Contact

질문이나 의견이 있다면 [Martin Geisler](mailto:mgeisler@google.com)에게 연락을 주시거나 
[discussion on GitHub](https://github.com/google/comprehensive-rust/discussions)에 남겨주세요.

> For questions or comments, please contact [Martin Geisler](mailto:mgeisler@google.com) or start a [discussion on GitHub](https://github.com/google/comprehensive-rust/discussions). We would love to hear from you.

---
## 역자주
스터디 겸 해서 저장소 fork후 번역을 시작했습니다.
mdbook search 기능이 한국어를 지원하지 않아서 찾아봤는데 아직 러스트 실력이 미천해서 mdbook에서 한국어 지원하도록 PR 보낼 수가 없네요(...) 그래서 검색용 영어와 병기해서 번역 합니다.

4일차 오후 강의는 안드로이드 OS에 대한 부분인데 안드로이드 지식이 없어서 되려 이해에 방해 될거 같아서 미번역 or 천천히 번역할 예정입니다.

순서는 [Welcome to Comprehensive Rust 🦀](src/welcome.md)부터 시작하는데 해당 문서의 mdbook을 serve해서 보시거나 본 페이지 [인터넷북](https://keispace.github.io/comprehensive-rust-kr)에서 보시길 추천합니다.(next prev 이동 편의)

## history
- 1차 완료 파트
    - 2022-12-28: 시작 ~ 5.1
    - 2022-12-28: ~ 6.4
    - 2022-12-29: ~ 10.5
    - 2022-12-30: ~ 18.1
    - 2023-01-02: ~ 25(day3 morning)
    - 2023-01-03: ~ 31.4
    - 2023-01-04: 4일차 오후(안드로이드) 제외 전체 완료. 
    - 2023-01-05: 33.1~33.2 작업, 원본 싱크
        - 추가기능으로 강의노트 기능이 포함되었는데 역주의 힌트 같은 부분과 같은 html tag를 사용하기 때문에 해당 기능은 제외했습니다.(book.toml)
    - 2023-01-06: 원본 싱크 후 추가 내용 작업과 목차 번역 진행.
        - 강의노트 예제가 추가되있어서 이부분 추가 작업