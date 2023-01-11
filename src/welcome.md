# Welcome to Comprehensive Rust 🦀

## 현재 구글 사이트에 번역 통합 작업 중으로 현재 버전은 archived 되었습니다.(23-01-10)
## 더이상 업데이트는 되지 않고 최종 반영 되면 사라질 예정입니다. 
## 자세한 사항은 [원문](https://github.com/google/comprehensive-rust/pull/130)을 참조 하세요


이것은 안드로이드 팀에 의해 개발된 4일간의 러스트 강좌입니다. 
기본 문법부터 제너릭, 에러 핸들링과 같은 고급주제까지 러스트의 모든 것을 포함합니다.
마지막 날에는 안드로이드에 대한 것 까지 다룹니다.
> This is a four day Rust course developed by the Android team. The course covers
> the full spectrum of Rust, from basic syntax to advanced topics like generics
> and error handling. It also includes Android-specific content on the last day.

강의는 당신이 러스트에 대해서 아무것도 모른다고 가정하고 아래의 목표를 가지고 있습니다. 
* 러스트 구문과 언어에 대한 포괄적인 이해를 제공합니다.
* 기존 프로그램을 수정하고 러스트에서 새 프로그램을 작성할 수 있습니다.
* 일반적인 러스트 관용구를 보여줍니다.
> The goal of the course is to teach you Rust. We assume you don't know anything
> about Rust and hope to:
> * Give you a comprehensive understanding of the Rust syntax and language.
> * Enable you to modify existing programs and write new programs in Rust.
> * Show you common Rust idioms.

4일차 강의에 우리는 아래와 같은 안드로이드 특유의 것들도 설명합니다.
* 러스트에서 Android 구성 요소를 구축.
* AIDL 서버 및 클라이언트.
* C, C++ 및 Java와의 상호 운용성.
> On Day 4, we will cover Android-specific things such as:
> * Building Android components in Rust.
> * AIDL servers and clients.
> * Interoperability with C, C++, and Java.

이 과정은 러스트로 안드로이드 **어플리케이션**을 개발하는 것은 다루는 것이 아니라,
안드로이드 OS에서의 러스트 코드 작성을 다룹니다.
> It is important to note that this course does not cover Android **application** 
> development in Rust, and that the Android-specific parts are specifically about
> writing code for Android itself, the operating system. 

## Non-Goals

러스트는 몇일만에 모든 것을 다루기에는 너무 큰 언어입니다. 그래서 아래와 같은것을 목표로 하지 않습니다.
> Rust is a large language and we won't be able to cover all of it in a few days.
> Some non-goals of this course are:

* 비동기적 러스트 사용법 --- 간단하게 언급정도는 하겠지만 좀 더 자세한 내용은 [Asynchronous
  Programming in Rust](https://rust-lang.github.io/async-book/)를 참조해주세요
> * Learn how to use async Rust --- we'll only mention about async Rust when
>   covering traditional concurrency primitives. Please see [Asynchronous
>   Programming in Rust](https://rust-lang.github.io/async-book/) instead for
>   details on this topic.

* 매크로를 개발하는 방법. [Chapter 19.5 in the Rust Book](https://doc.rust-lang.org/book/ch19-06-macros.html)와 [Rust by Example](https://doc.rust-lang.org/rust-by-example/macros.html)를 참조하세요
> * Learn how to develop macros, please see [Chapter 19.5 in the Rust
>   Book](https://doc.rust-lang.org/book/ch19-06-macros.html) and [Rust by
>   Example](https://doc.rust-lang.org/rust-by-example/macros.html) instead.

## Assumptions

본 강좌는 당신이 프로그래밍 자체에 대해서는 알고 있다고 가정합니다. 
러스트는 정적타입 언어이며, 강좌에서는 C와 C++과 비교, 대조를 통해 러스트를 설명할 것입니다.
> The course assumes that you already know how to program. Rust is a statically
> typed language and we will sometimes make comparisons with C and C++ to better
> explain or contrast the Rust approach.

만일 당신이 동적 타입 언어(Python이나 JavaScript)로 프로그래밍 하는 방법을 알고 있다면 잘 따라올 수 있을 것입니다. 
> If you know how to program in a dynamically typed language such as Python or
> JavaScript, then you will be able to follow along just fine too.

<details>
<summary>강의 참조 노트</summary>

이것은 _speaker note_의 예제입니다. 이 부분을 이용해서 추가 정보를 제공합니다. 
주로 강의실에서 제기되는 일반적인 질문에 대한 답변과 강사가 다루어야 할 주요 요점일 수 있습니다. 

> This is an example of a _speaker note_. We will use these to add additional
> information to the slides. This could be key points which the instructor should
> cover as well as answers to typical questions which come up in class.

--- 
역주 

*  해당기능은 새 창으로 노트 부분을 따로 띄우는 ppt 발표용 프레젠테이션과 유사한 기능입니다만  역주에서 일부 hint 등으로접기 기능을 사용하고 있어서 원문의 _speaker note_ 기능은 의도적으로 꺼 높은 상태입니다.
* 접기 제목(summary)으로 `강의 참조 노트`라고 된 부분이 해당 발표자료입니다. 
</details>
