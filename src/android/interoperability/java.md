# Interoperability with Java

자바는 [Java Native Interface(JNI)](https://en.wikipedia.org/wiki/Java_Native_Interface)를 통해 공유 객체를 로드할 수 있습니다. [`jni` 크레이트](https://docs.rs/jni/)를 사용하여 호환 라이브러리를 만들 수 있습니다.

> Java can load shared objects via [Java Native Interface
> (JNI)](https://en.wikipedia.org/wiki/Java_Native_Interface). The [`jni`
> crate](https://docs.rs/jni/) allows you to create a compatible library.

먼저, 자바로 내보낼 러스트 함수를 생성합니다: 
> First, we create a Rust function to export to Java:

_interoperability/java/src/lib.rs_:

```rust,compile_fail
{{#include java/src/lib.rs:hello}}
```

_interoperability/java/Android.bp_:

```javascript
{{#include java/Android.bp:libhello_jni}}
```

마침내, 자바에서 이 함수를 호출 할 수 있습니다: 
> Finally, we can call this function from Java:

_interoperability/java/HelloWorld.java_:

```java
{{#include java/HelloWorld.java:HelloWorld}}
```

_interoperability/java/Android.bp_:

```javascript
{{#include java/Android.bp:helloworld_jni}}
```

마지막으로 바이너리를 빌드, 싱크, 실행합니다: 
> Finally, you can build, sync, and run the binary:

```shell
{{#include ../build_all.sh:helloworld_jni}}
```
