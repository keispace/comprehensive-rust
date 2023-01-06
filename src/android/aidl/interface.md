# AIDL Interfaces

AIDL 인터페이스를 이용해서 서비스의 API를 선언합니다: 
> You declare the API of your service using an AIDL interface:

*birthday_service/aidl/com/example/birthdayservice/IBirthdayService.aidl*:

```java
{{#include birthday_service/aidl/com/example/birthdayservice/IBirthdayService.aidl:IBirthdayService}}
```

*birthday_service/aidl/Android.bp*:

```javascript
{{#include birthday_service/aidl/Android.bp}}
```

AIDL 파일이 벤더 파티션의 바이너리에서 사용되는 경우 `vendor_available: true`를 추가합니다.
> Add `vendor_available: true` if your AIDL file is used by a binary in the vendor
> partition.
