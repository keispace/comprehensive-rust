# AIDL Server

마지막으로 서비스를 제공하는 서버를 만들 수 있습니다:
> Finally, we can create a server which exposes the service:

*birthday_service/src/server.rs*:

```rust,ignore
{{#include birthday_service/src/server.rs:main}}
```

*birthday_service/Android.bp*:

```javascript
{{#include birthday_service/Android.bp:birthday_server}}
```
