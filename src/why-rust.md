# Why Rust?

러스트만의 독특한 세일즈 포인트(장점):
* 컴파일 시 메모리 안전
* 정의되지 않은 런타임 동작이 없습니다.
* 모던한 언어적 특징
> Some unique selling points of Rust:
> 
> * Compile time memory safety.
> * Lack of undefined runtime behavior.
> * Modern language features.


<details>
<summary>강의 참조 노트</summary>

강의 참여자들에게 프로그래밍 언어 사용 경험을 물어보시기 바랍니다. 경험에 따라 러스트의 다양한 기능을 강조할 수 있습니다:

* C/C++ : 러스트는 '빌림'검사를 통해 전체 클래스의 런타임 에러를 제거합니다. C/C++ 처럼 성능은 확보되지만 메모리 안정성에 대한 문제가 없습니다. 또한, 패턴매칭이나 내장 종속성 관리 같은 현대언어 기능을 가질 수 있습니다. 
* Java, Go, Python, JaveScript : 해당 언어들과 동일한 메모리 안정성과 '하이레벨'언어의 느낌을 느낄 수 있습니다. 또한, GC가 없는 C/C++과 같이 빠르고 예측 가능한 성능을 얻을 수 있고 필요한 경우 하드웨어의 로우레벨까지 접근 할 수 있습니다. 

> Make sure to ask the class which languages they have experience with. Depending
> on the answer you can highlight different features of Rust:
> 
> * Experience with C or C++: Rust eliminates a whole class of _runtime errors_
>   via the borrow checker. You get performance like in C and C++, but you don't
>   have the memory unsafety issues. In addition, you get a modern language with
>   constructs like pattern matching and built-in dependency management.
> 
> * Experience with Java, Go, Python, JavaSript...: You get the same memory safety
>   as in those languages, plus a similar high-level language feeling. In addition
>   you get fast and predictable performance like C and C++ (no garbage collector)
>   as well as access to low-level hardware (should you need it)


</details>
