# Threads

러스트의 스레드는 다른 언어의 스레드와 유사하게 동작합니다:
> Rust threads work similarly to threads in other languages:

```rust,editable
use std::thread;
use std::time::Duration;

fn main() {
    thread::spawn(|| {
        for i in 1..10 {
            println!("Count in thread: {i}!");
            thread::sleep(Duration::from_millis(5));
        }
    });

    for i in 1..5 {
        println!("Main thread: {i}");
        thread::sleep(Duration::from_millis(5));
    }
}
```

* 스레드는 모두 데몬 스레드[^역주1]입니다. 따라서 주 스레드는 이를 기다리지 않습니다.
* 스레드의 패닉은 서로 독립적으로 발생합니다.
  * (스레드의) 패닉은 (주 스레드에게) 페이로드를 전달하고, 이는 `downcast_ref`로 풀어볼 수 있습니다.
> * Threads are all daemon threads, the main thread does not wait for them.
> * Thread panics are independent of each other.
>   * Panics can carry a payload, which can be unpacked with `downcast_ref`.

<details>
<summary>강의 참조 노트</summary>

키포인트: 
* 주 스레드가 기다리지 않기 때문에 생성된 스레드의 for문은 10까지 가지 않습니다.
* 만약 주 스레드가 스레드 동작을 대기 하기 원한다면 `let handle = thread::spawn(...)`으로 스레드를 선언한 후 `handle.join()`로 연결하여 사용합니다.
* 스레드에서 유발된 패닉(for 강제 종료)이 주 스레드에는 영향이 없음을 확인하시기 바랍니다.
* `handle.join()`사용시 `Result` 반환값을 통해 패닉 페이로드에 접근할 수 있습니다. [`Any`]를 참조하시기 바랍니다.

> Key points:
> 
> * Notice that the thread is stopped before it reaches 10 — the main thread is
>   not waiting.
> 
> * Use `let handle = thread::spawn(...)` and later `handle.join()` to wait for
>   the thread to finish.
> 
> * Trigger a panic in the thread, notice how this doesn't affect `main`.
> 
> * Use the `Result` return value from `handle.join()` to get access to the panic
>   payload. This is a good time to talk about [`Any`].

[`Any`]: https://doc.rust-lang.org/std/any/index.html

</details>

---
역주

- 다른언어의 스레드 === js만 했으면 헬게이트 열리는 장입니다(...)

[^역주1]: 데몬 스레드는 일반 스레드의 보조 스레드로 주 스레드가 종료되면 같이 종료되고, 백그라운드에서 낮은 우선순위로 동작합니다. 
    - 데몬: 사용자가 직접적으로 제어하지 않고 백그라운드에서 동작하는 프로그램.
