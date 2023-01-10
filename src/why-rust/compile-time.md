# Compile Time Guarantees

컴파일 시 정적 메모리 관리:

* 초기화되지 않는 변수가 없습니다.
* 메모리 누수 없음(_거의_. 강의참조노트 참고.)
* 메모리 이중 해제는 안됩니다. 
* 메모리 해제 후 사용 안됩니다.
* `NULL`포인터는 없습니다.
* 잠긴 뮤텍스를 잊을 수 없습니다.
* 스레드간 데이터레이스가 없습니다. 
* 이터레이터(반복자, iterator) 무효화가 없습니다.

> Static memory management at compile time:
> * No uninitialized variables.
> * No memory leaks (_mostly_, see notes).
> * No double-frees.
> * No use-after-free.
> * No `NULL` pointers.
> * No forgotten locked mutexes.
> * No data races between threads.
> * No iterator invalidation.

<details>
<summary>강의 참조 노트</summary>

안전한 러스트에서도 메모리 누수가 발생하는 몇가지 예는 다음과 같습니다:

* [`Box::leak`]을 사용하여 런타임 초기화 및 런타임 크기 정적 변수를 가져올 수 있습니다. 이를 통해 포인터 누수를 발생시킬 수 있습니다. 
* [`std::mem::forget`]을 사용하여 컴파일러가 값에 대해 "잊도록" 만들 수 있습니다(소멸자가 실행되지 않음을 의미합니다).
* `Rc` 또는 `Arc`를 사용하여 실수로 [reference cycle]을 생성할 수도 있습니다.

본 코스에서는 "메모리 누출 없음"을 "우발적인 메모리 누출 없음"으로 이해해야 합니다.

> It is possible to produce memory leaks in (safe) Rust. Some examples
are:
> 
> * You can for use [`Box::leak`] to leak a pointer. A use of this could
>   be to get runtime-initialized and runtime-sized static variables
> * You can use [`std::mem::forget`] to make the compiler "forget" about
>   a value (meaning the destructor is never run).
> * You can also accidentally create a [reference cycle] with `Rc` or
>   `Arc`.
> 
> For the purpose of this course, "No memory leaks" should be understood
> as "Pretty much no *accidental* memory leaks".

[`Box::leak`]: https://doc.rust-lang.org/std/boxed/struct.Box.html#method.leak
[`std::mem::forget`]: https://doc.rust-lang.org/std/mem/fn.forget.html
[reference cycle]: https://doc.rust-lang.org/book/ch15-06-reference-cycles.html

</details>

---
역자주
* mutexes : 멀티스레딩에서 자원을 선점한 작업자가 잠그면(lock) 다른 작업자들은 lock이 해제될때까지 자원에 대해 접근을 할 수 없도록 막는 방식. 
    * cf. semaphore: 자원에 접근 할 수 있는 작업자(스레드,프로세스)의 수를 나타내는 값을 둬서 상호 배제하는 방식.
