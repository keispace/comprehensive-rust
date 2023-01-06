# Summary

[Welcome to Comprehensive Rust 🦀](welcome.md)
- [카고 사용하기: Using Cargo](cargo.md)
  - [러스트 생태계: Rust Ecosystem](cargo/rust-ecosystem.md)
  - [코드 샘플: Code Samples](cargo/code-samples.md)
  - [로컬환경의 카고: Running Cargo Locally](cargo/running-locally.md)
- [강의 구성: Course Structure](structure.md)


# 1일차 오전: Day 1: Morning

----

- [개요: Welcome](welcome-day-1.md)
  - [러스트란?: What is Rust?](welcome-day-1/what-is-rust.md)
- [Hello World!](hello-world.md)
  - [작은 예제: Small Example](hello-world/small-example.md)
- [러스트를 써야하는 이유: Why Rust?](why-rust.md)
  - [컴파일 보증: Compile Time Guarantees](why-rust/compile-time.md)
  - [런타임 보증: Runtime Guarantees](why-rust/runtime.md)
  - [현대적인 특징: Modern Features](why-rust/modern.md)
- [기본 문법: Basic Syntax](basic-syntax.md)
  - [스칼라 타입: Scalar Types](basic-syntax/scalar-types.md)
  - [복합 타입: Compound Types](basic-syntax/compound-types.md)
  - [참조: References](basic-syntax/references.md)
    - [댕글링 참조: Dangling References](basic-syntax/references-dangling.md)
  - [슬라이스: Slices](basic-syntax/slices.md)
    - [`String` vs `str`](basic-syntax/string-slices.md)
  - [함수: Functions](basic-syntax/functions.md)
    - [메서드: Methods](basic-syntax/methods.md)
    - [오버로딩: Overloading](basic-syntax/functions-interlude.md)
- [연습문제: Exercises](exercises/day-1/morning.md)
  - [명시적 형변환: Implicit Conversions](exercises/day-1/implicit-conversions.md)
  - [배열과 `for`반복문: Arrays and `for` Loops](exercises/day-1/for-loops.md)

# 1일차 오후: Day 1: Afternoon

- [변수: Variables](basic-syntax/variables.md)
  - [타입 추론: Type Inference](basic-syntax/type-inference.md)
  - [`static` & `const`](basic-syntax/static-and-const.md))
  - [스코프(범위)와 쉐도잉: Scopes and Shadowing](basic-syntax/scopes-shadowing.md)
- [메모리 관리: Memory Management](memory-management.md)
  - [Stack vs Heap](memory-management/stack-vs-heap.md)
  - [스택 메모리: Stack Memory](memory-management/stack.md)
  - [수동 메모리 관리: Manual Memory Management](memory-management/manual.md)
  - [범위기반 메모리 관리: Scope-Based Memory Management](memory-management/scope-based.md)
  - [가비지 컬렉션: Garbage Collection](memory-management/garbage-collection.md)
  - [러스트의 메모리 관리: Rust Memory Management](memory-management/rust.md)
  - [비교: Comparison](memory-management/comparison.md)
- [소유권: Ownership](ownership.md)
  - [의미 이동: Move Semantics](ownership/move-semantics.md)
  - [러스트의 이동된 문자열: Moved Strings in Rust](ownership/moved-strings-rust.md)
    - [모던C++에서 이중해제 문제: Double Frees in Modern C++](ownership/double-free-modern-cpp.md)
  - [함수호출에서 이동: Moves in Function Calls](ownership/moves-function-calls.md)
  - [복사와 복제: Copying and Cloning](ownership/copy-clone.md)
  - [빌림: Borrowing](ownership/borrowing.md)
    - [공유와 고유 빌림:Shared and Unique Borrows](ownership/shared-unique-borrows.md)
  - [수명: Lifetimes](ownership/lifetimes.md)
  - [함수호출에서의 수명: Lifetimes in Function Calls](ownership/lifetimes-function-calls.md)
  - [자료 구조에서의 수명: Lifetimes in Data Structures](ownership/lifetimes-data-structures.md)
- [연습문제: Exercises](exercises/day-1/afternoon.md)
  - [도서관 설계: Designing a Library](exercises/day-1/book-library.md)
  - [반복자와 소유권: Iterators and Ownership](exercises/day-1/iterators-and-ownership.md)


# 2일차 오전: Day 2: Morning

----

- [개요: Welcome](welcome-day-2.md)
- [구조체: Structs](structs.md)
  - [튜플: Tuple Structs](structs/tuple-structs.md)
  - [필드 할당 단축 문법: Field Shorthand Syntax](structs/field-shorthand.md)
- [열거형: Enums](enums.md)
  - [Variant Payloads](enums/variant-payloads.md)
  - [열거형 크기: Enum Sizes](enums/sizes.md)
- [메서드: Methods](methods.md)
  - [메서드 인자: Method Receiver](methods/receiver.md)
  - [예제: Example](methods/example.md)
- [패턴 매칭: Pattern Matching](pattern-matching.md)
  - [열거형 분해: Destructuring Enums](pattern-matching/destructuring-enums.md)
  - [구조체 분해: Destructuring Structs](pattern-matching/destructuring-structs.md)
  - [배열 분해: Destructuring Arrays](pattern-matching/destructuring-arrays.md)
  - [매치 검사식: Match Guards](pattern-matching/match-guards.md)
- [연습문제: Exercises](exercises/day-2/morning.md)
  - [건강상태 통계: Health Statistics](exercises/day-2/health-statistics.md)
  - [점과 다각형: Points and Polygons](exercises/day-2/points-polygons.md)

# 2일차 오후: Day 2: Afternoon

- [흐름 제어: Control Flow](control-flow.md)
  - [블록: Blocks](control-flow/blocks.md)
  - [if 표현식: `if` expressions](control-flow/if-expressions.md)
  - [if let 표현식: `if let` expressions](control-flow/if-let-expressions.md)
  - [while 표현식: `while` expressions](control-flow/while-expressions.md)
  - [while let 표현식: `while let` expressions](control-flow/while-let-expressions.md)
  - [for 표현식: `for` expressions](control-flow/for-expressions.md)
  - [loop 표현식: `loop` expressions](control-flow/loop-expressions.md)
  - [match 표현식: `match` expressions](control-flow/match-expressions.md)
  - [`break` & `continue`](control-flow/break-continue.md)
- [표준 라이브러리: Standard Library](std.md)
  - [`String`](std/string.md)
  - [`Option` and `Result`](std/option-result.md)
  - [`Vec`](std/vec.md)
  - [`HashMap`](std/hashmap.md)
  - [`Box`](std/box.md)
    - [재귀적 자료구조: `Recursive Data Types`](std/box-recursive.md)
    - [(메모리)적소 최적화`Niche Optimization`](std/box-niche.md)
  - [`Rc`](std/rc.md)
- [모듈: Modules](modules.md)
  - [접근자: Visibility](modules/visibility.md)
  - [경로: Paths](modules/paths.md)
  - [파일시스템 계층: Filesystem Hierarchy](modules/filesystem.md)
- [연습문제: Exercises](exercises/day-2/afternoon.md)
  - [룬 알고리즘: Luhn Algorithm](exercises/day-2/luhn.md)
  - [문자열과 반복자: Strings and Iterators](exercises/day-2/strings-iterators.md)


# 3일차 오전: Day 3: Morning

----

- [개요: Welcome](welcome-day-3.md)
- [트레이트: Traits](traits.md)
  - [파생 트레이트: Deriving Traits](traits/deriving-traits.md)
  - [기본 메서드: Default Methods](traits/default-methods.md)
  - [중요 트레이트: Important Traits](traits/important-traits.md)
    - [`Iterator`](traits/iterator.md)
    - [`From` and `Into`](traits/from-into.md)
    - [`Read` and `Write`](traits/read-write.md)
    - [`Add`, `Mul`, ...](traits/operators.md)
    - [`Drop`](traits/drop.md)
- [제너릭: Generics](generics.md)
  - [제너릭 데이터 타입: Generic Data Types](generics/data-types.md)
  - [제너릭 메서드: Generic Methods](generics/methods.md)
  - [제너릭 타입 제한(트레이트 경계): Trait Bounds](generics/trait-bounds.md)
  - [`impl Trait`](generics/impl-trait.md)
  - [클로저: Closures](generics/closures.md)
  - [단형화: Monomorphization](generics/monomorphization.md)
  - [트레이트 객체: Trait Objects](generics/trait-objects.md)
- [연습문제: Exercises](exercises/day-3/morning.md)
  - [간단한 GUI 라이브러리: A Simple GUI Library](exercises/day-3/simple-gui.md)

# 3일차 오후: Day 3: Afternoon

- [오류처리: Error Handling](error-handling.md)
  - [패닉: Panics](error-handling/panics.md)
    - [스택 해제 추적: Catching Stack Unwinding](error-handling/panic-unwind.md)
  - [구조화된 오류처리: Structured Error Handling](error-handling/result.md)
  - ['?'를 이용한 오류 전파: Propagating Errors with `?`](error-handling/try-operator.md)
    - [오류타입 변환: Converting Error Types](error-handling/converting-error-types.md)
    - [파생 오류 열거형: Deriving Error Enums](error-handling/deriving-error-enums.md)
    - [오류에 상황정보 추가: Adding Context to Errors](error-handling/error-contexts.md)
- [테스트: Testing](testing.md)
  - [단위 테스트: Unit Tests](testing/unit-tests.md)
  - [테스트모듈: Test Modules](testing/test-modules.md)
  - [문서 테스트: Documentation Tests](testing/doc-tests.md)
  - [통합 테스트: Integration Tests](testing/integration-tests.md)
- [안전하지 않은 러스트:Unsafe Rust](unsafe.md)
  - [원시포인트 역참조: Dereferencing Raw Pointers](unsafe/raw-pointers.md)
  - [정적 가변 변수: Mutable Static Variables](unsafe/mutable-static-variables.md)
  - ['안전하지 않은' 함수 호출: Calling Unsafe Functions](unsafe/unsafe-functions.md)
  - [외부(다른언어) 함수들:Extern Functions](unsafe/extern-functions.md)
  - [Unions](unsafe/unions.md)
- [연습문제: Exercises](exercises/day-3/afternoon.md)
  - [FFI래퍼: Safe FFI Wrapper](exercises/day-3/safe-ffi-wrapper.md)


# 4일차 오전: Day 4: Morning

----

- [개요: Welcome](welcome-day-4.md)
- [겂없는 동시성: Concurrency](concurrency.md)
  - [스레드: Threads](concurrency/threads.md)
  - [범위 스레드: Scoped Threads](concurrency/scoped-threads.md)
  - [채널: Channels](concurrency/channels.md)
    - [무경계 채널: Unbounded Channels](concurrency/channels/unbounded.md)
    - [경계 채널: Bounded Channels](concurrency/channels/bounded.md)
  - [상태 공유: Shared State](concurrency/shared_state.md)
    - [`Arc`](concurrency/shared_state/arc.md)
    - [`Mutex`](concurrency/shared_state/mutex.md)
    - [예제: Example](concurrency/shared_state/example.md)
  - [`Send` and `Sync`](concurrency/send-sync.md)
    - [`Send`](concurrency/send-sync/send.md)
    - [`Sync`](concurrency/send-sync/sync.md)
    - [예제: Examples](concurrency/send-sync/examples.md)
- [연습문제: Exercises](exercises/day-4/morning.md)
  - [식사하는 철학자들: Dining Philosophers](exercises/day-4/dining-philosophers.md)
  - [멀티스레드 링크 검사기: Multi-threaded Link Checker](exercises/day-4/link-checker.md)

# 4일차 오후: Day 4: Afternoon

----

- [안드로이드: Android](android.md)
  - [설치: Setup](android/setup.md)
  - [빌드 규칙: Build Rules](android/build-rules.md)
    - [바이너리: Binary](android/build-rules/binary.md)
    - [라이브러리: Library](android/build-rules/library.md)
  - [AIDL](android/aidl.md)
    - [인터페이스: Interface](android/aidl/interface.md)
    - [구현: Implementation](android/aidl/implementation.md)
    - [서버: Server](android/aidl/server.md)
    - [배포: Deploy](android/aidl/deploy.md)
    - [클라이언트:Client](android/aidl/client.md)
    - [API 수정: Changing API](android/aidl/changing.md)
  - [로깅: Logging](android/logging.md)
  - [상호운용성: Interoperability](android/interoperability.md)
    - [With C](android/interoperability/with-c.md)
      - [Bindgen을 사용: Calling C with Bindgen](android/interoperability/with-c/bindgen.md)
      - [C에서 러스트 호출: Calling Rust from C](android/interoperability/with-c/rust.md)
    - [With C++](android/interoperability/cpp.md))
    - [With Java](android/interoperability/java.md)
- [연습문제: Exercises](exercises/day-4/afternoon.md)

# Final Words

- [Thanks!](thanks.md)
- [다른 자료: Other Resources](other-resources.md)
- [Credits](credits.md)

----

# Solutions

----

- [Solutions](exercises/solutions.md)
  - [Day 1 Morning](exercises/day-1/solutions-morning.md)
  - [Day 1 Afternoon](exercises/day-1/solutions-afternoon.md)
  - [Day 2 Morning](exercises/day-2/solutions-morning.md)
  - [Day 2 Afternoon](exercises/day-2/solutions-afternoon.md)
  - [Day 3 Morning](exercises/day-3/solutions-morning.md)
  - [Day 3 Afternoon](exercises/day-3/solutions-afternoon.md)
  - [Day 4 Morning](exercises/day-4/solutions-morning.md)
