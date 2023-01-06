# AIDL Client

마지막으로, 새로운 서비스를 위한 러스트 클라이언트를 만들 수 있습니다.
> Finally, we can create a Rust client for our new service.

*birthday_service/src/client.rs*:

```rust,ignore
{{#include birthday_service/src/client.rs:main}}
```

*birthday_service/Android.bp*:

```javascript
{{#include birthday_service/Android.bp:birthday_client}}
```

클라이언트는 `libbirthdayservice`에 의존하지 않습니다. 

장치에서 빌드, 푸시, 실행합니다: 
> Notice that the client does not depend on `libbirthdayservice`.
> 
> Build, push, and run the client on your device:

```shell
{{#include ../build_all.sh:birthday_client}}
Happy Birthday Charlie, congratulations with the 60 years!
```
