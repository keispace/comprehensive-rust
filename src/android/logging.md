# Logging

`log`크레이트를 사용하여 `logcat`(장치)나 `stdout`(호스트)에서 자동으로 로그를 기록하도록 합니다:
> You should use the `log` crate to automatically log to `logcat` (on-device) or
> `stdout` (on-host):

_hello_rust_logs/Android.bp_:

```javascript
{{#include logging/Android.bp}}
```

_hello_rust_logs/src/main.rs_:

```rust,ignore
{{#include logging/src/main.rs:main}}
```

장치에서 바이너리를 빌드, 푸시, 실행합니다:
> Build, push, and run the binary on your device:

```shell
{{#include build_all.sh:hello_rust_logs}}
```

`adb logcat`커맨드로 로그를 확인합니다:
> The logs show up in `adb logcat`:

```shell
$ adb logcat -s rust
09-08 08:38:32.454  2420  2420 D rust: hello_rust_logs: Starting program.
09-08 08:38:32.454  2420  2420 I rust: hello_rust_logs: Things are going fine.
09-08 08:38:32.454  2420  2420 E rust: hello_rust_logs: Something went wrong!
```
