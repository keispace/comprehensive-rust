# Service Implementation

이제 AIDL서비스를 구현할 수 있습니다:
> We can now implement the AIDL service:

*birthday_service/src/lib.rs*:

```rust,ignore
{{#include birthday_service/src/lib.rs:IBirthdayService}}
```

*birthday_service/Android.bp*:

```javascript
{{#include birthday_service/Android.bp:libbirthdayservice}}
```
