# Changing API

API를 확장하여 더 많은 기능을 제공합니다. 클라이언트가 생일 카드에 대한 줄 목록을 지정할 수 있도록 합니다:

> Let us extend the API with more functionality: we want to let clients specify a
l> ist of lines for the birthday card:

```java
package com.example.birthdayservice;

/** Birthday service interface. */
interface IBirthdayService {
    /** Generate a Happy Birthday message. */
    String wishHappyBirthday(String name, int years, in String[] text);
}
```
