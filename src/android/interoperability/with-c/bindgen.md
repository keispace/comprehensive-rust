# Using Bindgen

[bindgen](https://rust-lang.github.io/rust-bindgen/introduction.html)는 C 헤더파일에서 자동으로 생성하는 도구입니다.
> The [bindgen](https://rust-lang.github.io/rust-bindgen/introduction.html) tool
can auto-generate bindings from a C header file.

작은 C라이브러리를 생성합니다: 
> First create a small C library:

_interoperability/bindgen/libbirthday.h_:

```c
{{#include bindgen/libbirthday.h:card}}
```

_interoperability/bindgen/libbirthday.c_:

```c
{{#include bindgen/libbirthday.c:print_card}}
```

`Android.bp` 파일에 아래를 추가합니다:
> Add this to your `Android.bp` file:

_interoperability/bindgen/Android.bp_:

```javascript
{{#include bindgen/Android.bp:libbirthday}}
```

라이브러리에 대한 래퍼 헤더 파일을 만듭니다(이 예시에서는 필요하지 않습니다):
> Create a wrapper header file for the library (not strictly needed in this
> example):

_interoperability/bindgen/libbirthday_wrapper.h_:

```c
{{#include bindgen/libbirthday_wrapper.h:include}}
```

이제 바인딩을 자동으로 생성할 수 있습니다:
> You can now auto-generate the bindings:

_interoperability/bindgen/Android.bp_:

```javascript
{{#include bindgen/Android.bp:libbirthday_bindgen}}
```

마침내, 러스트 프로그램에서 바인딩을 사용할 수 있습니다:
> Finally, we can use the bindings in our Rust program:

_interoperability/bindgen/Android.bp_:

```javascript
{{#include bindgen/Android.bp:print_birthday_card}}
```

_interoperability/bindgen/main.rs_:

```rust,compile_fail
{{#include bindgen/main.rs:main}}
```

Build, push, and run the binary on your device:

```shell
{{#include ../../build_all.sh:print_birthday_card}}
```

마지막으로, 바인딩이 작동하는지 자동생성 테스트를 실행할 수 있습니다:
> Finally, we can run auto-generated tests to ensure the bindings work:

_interoperability/bindgen/Android.bp_:

```javascript
{{#include bindgen/Android.bp:libbirthday_bindgen_test}}
```

```shell
{{#include ../../build_all.sh:libbirthday_bindgen_test}}
```
